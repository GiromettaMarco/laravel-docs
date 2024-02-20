# How to set up a sail command alias

In order to run a sail command from the root of your project, you are supposed to type

```
./vendor/bin/sail
```

You can replace ```./vendor/bin/sail``` with ```sail``` by adding an alias to your enviroment shell configuration.

## Shell configuration file

Open your shell configuration file. For example:

```
nano ~/.bashrc
```

or

```
gnome-text-editor ~/.bashrc
```

Add the following line at the end and save:

```
alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)'
```

Restart your shell or source the bashrc file with:

```
source ~/.bashrc
```

## Notes

This operation makes the alias always available in your environment for the current user.
If you want the alias to be available globally add it to ```/etc/bash.bashrc```.
