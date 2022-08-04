# txtbrowser
Browse plain text easily(show the title tag and syntax highlight)
TxtBrowser : Browse plain text easily(show the title tag and syntax highlight)

 script karma  	Rating 39/15, Downloaded by 895 	 Comments, bugs, improvements  	Vim wiki

created by
yp guo
 
script type
syntax
 
description

The "TxtBrowser" plugin works along with taglist(vimscript #273: taglist.vim),
It generate the document outline automatically for .txt and .rst files. Meanwhile it highlight the .txt and .rst files for you:

1) Use ":Tlist" command to open the outline of a .txt/.rst file in the taglist
window.

2) Use ":TlistUpdate" to update the outline after modification.

3) Syntax highlight: highlight the key element in your plain text. This include
the title, URLs, keywords you defined(default is TODO, ERROR, etc), Words in
bracket, etc. Syntax hightlight would be auto loaded after install. Snapshot of
feature 1 and 2 are available at:

http://guoyoooping.blog.163.com/album/edit/#m=1&aid=193892890

4) Browser Utilities(use ":help txtbrowser" for details):

<Leader>s: Search text under cursor(or selected) through search engine(google).
<Leader>f: Find text under cursor(or selected) through web dictionary(www.dict.cn).
<Leader>g: Goto the URL under cursor(or selected).
 
install Steps

1) Please make sure universal-ctags(https://github.com/universal-ctags/ctags) has been installed(Exuberant Ctags doesn't work for .rst files).

2) Please make sure taglist(vimscript #273: taglist.vim) has been installed.

3) Download the txtbrowser file and uncompress the files to your .vim directory:

    $ tar xvf txtbrowser-1.3.6.tar.bz2 -C ~/
    .vim/
    .vim/doc/
    .vim/doc/txtbrowser.cnx
    .vim/doc/txtbrowser.txt
    .vim/ftplugin/
    .vim/ftplugin/gdb.vim
    .vim/ftplugin/rst.vim
    .vim/ftplugin/txt.vim
    .vim/plugin/
    .vim/plugin/txtbrowser.vim
    .vim/syntax/
    .vim/syntax/txt.vim

4) open the .vim/doc/txtbrowser.txt Install the helptags using ":helptags ."

5) Add the following line into your .vimrc file and restart your vim.

    syntax on "syntax highlighting on
    filetype plugin on
    au BufRead,BufNewFile *.txt setlocal ft=txt
    au BufRead,BufNewFile *.rst setlocal ft=rst

