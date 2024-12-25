# Git config commands

Git config commands allow you to customize and configure various aspects of your Git environment, enhancing your development workflow and tailoring Git to your specific needs.

In this section, we will explore a range of Git config commands that enable you to set user details, configure aliases, define global and local settings, and more. These commands provide you with the flexibility to customize Git behavior, streamline your workflow, and adapt Git to match your preferred conventions.

By mastering Git config commands, you can personalize your Git experience, improve productivity, and ensure consistency across your projects and collaborations. Git config commands offer the key to tailor Git to your liking.

Explore these Git config commands and unlock the power to customize your Git environment.

## Set username and email
```bash
$ git config --global user.name <username>
$ git config --global user.email <mailaddress>
```
Without the `--global` option, this setting will only apply to a specific repository.

## Color displayed output
```bash
$ git config --global color.ui auto
```

## Set alias for command
```bash
$ git config --global alias.<aliasname> <commandname>
```

## Remove files from version control tracking
```bash
$ echo <filename> >> .gitignore
```
Add the paths of files under the `.gitignore` file. Git will no longer manage those files. You will have to commit the `.gitignore` file for this to work.

## Track empty directories under version control
```bash
$ cd <dirname>
$ touch .gitkeep
```
Git does not track empty directories. If you would like to add that to the version control, you will need to place a file in that directory. A common practice that people normally do is to add a `.gitkeep` file to the empty directory.

## Display settings
```bash
$ git config --global --list
```

## Setup HTTP connection to proxy server
Add the following setting to the `http` items of `.gitconfig` files.

```ini
[http]
  proxy = <address of the proxy server>:<port of the proxy server>
```
You can also configure it using the following config command:

```bash
$ git config --global http.proxy <address of the proxy server>:<port of the proxy server>
```

## Establish HTTP connection to user authenticated proxy server
Add the following setting to the `http` items of `.gitconfig` files.

```ini
[http]
  proxy = http://<username>:<password>@<address of the proxy server>:<port of the proxy server>
```
You can also configure it using the following config command:

```bash
$ git config --global http.proxy http://<username>:<password>@<address of the proxy server>:<port of the proxy server>
```

This version uses proper **code blocks** for commands and configurations for better readability. You can copy this content into your `.md` file and use the title in a `.txt` file. Let me know if you need further adjustments!