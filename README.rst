==============
VIM MetaWeblog
==============
:Author: Yugang LIU <liuyug # gmail.com>
:URL: https://github.com/liuyug/vim-metaweblog

Submit your **RST** article in VIM with metaweblog interface. 

Feature:

+ direct submit **RST** article to Blog.
+ support **HTML** article
+ automatic upload image resource and fix link for **RST** when new post
+ browse recent blogs
+ delete blog
+ upload file manually

Install
=======
0. Please install Docutils_ as RST tools, and Pygments_ for syntax highlight

.. _Docutils: http://docutils.sourceforge.net/
.. _Pygments: http://pygments.org/

1. install VIM plugin

.. code:: bash

    cp plugin/metaweblog.vim  ~/.vim/plugin/metaweblog.vim

2. Create new configuration file in ``~/.vim/password.vim``

.. code:: vim

    # password.vim
    let g:MetaWeblog_api_url='http://www.is-programmer.com/xmlrpc'
    let g:MetaWeblog_username='username'
    let g:MetaWeblog_password='password'

3. Install CSS to support style:

.. code:: bash

    # RST CSS style
    cat /usr/lib/python2.6/site-packages/docutils/writers/html4css1/html4css1.css > blog.css
    # code with scrolled bar
    echo "pre.code { overflow: auto; }" >> bslog.css
    # syntax highlight
    pygmentize -S default -f html -a pre.code >> blog.css

4. Upload blog.css to Blog site.

Guide
======
VIM shortcut keys:

.. code:: vim

    <leader>bl      toggle recent blog view
    <leader>bp      post article 
    <leader>bu      upload file under cursor in html

TODO
=====
+ How to locate original RST file by the article in Blog? 

