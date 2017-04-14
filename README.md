# Beautify Git in Your MacOS or OSX Terminal

This set of config files can help transform your command line from something ugly and painful to something delightful and easy-to-read.

![](screenshot.png)

## Setup
First things first, you'll want to install a nice color theme for your terminal. The one in the screenshot above is called TupeloHoney, and you'll find it included in the repo. I based it off of the most excellent [Flat](https://github.com/ahmetsulek/flat-terminal) theme.

Load the theme by opening up your mac terminal and navigating to **Preferences > Profiles > Import**. Don't expect things to suddenly look like they do above—*we still have work to do*.

With that out of the way, log into your bash terminal and punch in the following git config commands. You should be able to copy & paste them as a full block and then just hit return. This tells git that we want color in our UI, and sets specific colors for specific file status types.

**MacOS & OS X:**

```sh
git config --global color.ui true
git config --global color.status.changed "blue normal"
git config --global color.status.untracked "red normal"
git config --global color.status.added "magenta normal"
git config --global color.status.updated "green normal"
git config --global color.status.branch "yellow normal bold"
git config --global color.status.header "white normal bold"
```
The final step is to update your .bash_profile with the contents of the bash_profile file included in the repo. The easiest way to do this will be to first show all hidden files on your system, so that you can find that invisible .bash_profile file. You can do this by pasting the following command into your terminal.

```sh
defaults write com.apple.finder AppleShowAllFiles YES; killall Finder /System/Library/CoreServices/Finder.app
```
Once your finder reloads, you should be able to see all hidden files (files with names that start with a '.') Now navigate to **Users/YourUserNameHere**, and you should see .bash_profile in the directory. If you don't, you simply have to create one (you can do this by just placing an empty text file there and naming it .bash_profile.)

Either way, open your .bash_profile and paste in the contents of the bash_profile file included in this repo (paste it beneath any other content that's already in there.) Now save the file.

**Congratulations!** Your .bash_profile now includes all the code that your terminal needs to display it's UI in color, including a nicely colorized bash -ls command, a customized command prompt, and aliases for a number of highly-readable git log formats. You can customize these to your heart's content, but hopefully this will give you a solid jumping-off point.

Now let's hide those invisible files again, by pasting the following command into the terminal.

```sh
defaults write com.apple.finder AppleShowAllFiles NO; killall Finder /System/Library/CoreServices/Finder.app
```
Restart the terminal app, and you're ready to go!

## Usage

With any luck, you should now have a nice looking command line terminal running on your Mac. Navigate to one of your git repositories as you nomrally would and take a few of the included git log aliases for a ride.

```sh
log
```
Type in 'log' and hit return, and you should get a nicely formatted basic log, starting with a list of refs on top, followed by all your commits.

Now explore the other log aliases if you like:
- 'log' displays a basic git log with single-line commit messages only (this is the one I use most often.)
- 'logv' displays a more verbose log, including email addresses for commit authors. 
- 'logg' displays an ascii graph of your branches, along with basic log info.
- 'loggv' displays an ascii graph of your branches, along with more verbose log info.
- 'logm' displays multi-line commit messages.

## Release History

* 0.0.1
    * Work in progress

##

### Contact
- Email: cary.a.miller@gmail.com

### Social Media
- Twitter: [@vintageD18](https://twitter.com/vintageD18)
- GitHub: [https://github.com/cmilr/](https://github.com/cmilr/)

### License
Distributed under the MIT license. See ``LICENSE`` for more information.

# Thanks for stopping by!