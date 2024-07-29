# HashBang

### This vimscript adds `#! interpreter` lines to your new files automatically, based on file extension (removable), and also makes them executable when you quit.

----

To use it, you can download the file and do:

`cat Hashbang >> $HOME/.vimrc`

or **you can manually paste the content in your .vimrc file**. If $HOME doesn't contain .vimrc then you can manually create it.


### Customizations:

You can change parameters in last line:    

`:autocmd BufNewFile *.* :call Hashbang(1,1,0)`

**1st Parameter** :

`0` : use system interpreter location (`#! /usr/bin/python`).

`1` : use environment variable location (`#! /usr/bin/env python`).

**2nd Parameter** :

`0` : Do not change file permissions.

`1` : Change file permissions.  (`chmod u+x filename`).

**3rd Parameter** :

`0` : Do not remove extension.

`1` : Remove extension.
