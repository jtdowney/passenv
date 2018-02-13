# passenv

This is a simple wrapper script that is inspired by [envchain](https://github.com/sorah/envchain), a fantastic tool I use on my macOS laptop. I found myself wanting the functionality of envchain but on a home Linux server without X11/Gnome.

The script is backed by [pass](https://www.passwordstore.org/) and is loosely modeled on the example dmenu script.

## Usage

1. Setup pass like normal
2. Insert new environment variable
```
$ pass insert myaws/AWS_SECRET_ACCESS_KEY
mkdir: created directory '/home/jtdowney/.password-store/myaws'
Enter password for myaws/AWS_SECRET_ACCESS_KEY:
Retype password for myaws/AWS_SECRET_ACCESS_KEY:
```

3. Use the environment variables with a command
```
$ passenv myaws env
...
AWS_SECRET_ACCESS_KEY=secretvalue
...
```
