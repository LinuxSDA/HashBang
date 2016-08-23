# HashBang
Vim Plugin (maybe?) to add shebang lines to your programming files.


This vimscript adds `#! interpreter` lines to your new files automatically, based on file extension, and also makes them executable when you quit.

__

To use it, you can download the file and do:

`cat Hashbang >> $HOME/.vimrc`

or **you can manually paste the content in your .vimrc file**. If $HOME doesn't contain .vimrc then you can manually create it.


### Customizations:

You can change parameters in last line:    

`:autocmd BufNewFile *.* :call Hashbang(0,1)`

**Hashbang(0,0):**

- put system interpreter location (`#! /usr/bin/python`).  
- doesn't change file permissions.

**Hashbang(0,1):** 

- put system interpreter location (`#! /usr/bin/python`). 
- Change file permissions (`chmod u+x filename`).

**Hashbang(1,0):**

- use environment variable location (`#! /usr/bin/env python`). 
- doesn't change file permissions.

**Hashbang(1,1):**

- use environment variable location (`#! /usr/bin/env python`). 
- Change file permissions (`chmod u+x filename`).
