==================================
Sphinx extention : wikipedia
==================================

This Sphinx_ extension adds a docutils role to create links to wikipedia 
articles.

.. _Sphinx: http://sphinx-doc.org/

Licensing
---------

This code is released under the BSD License.  

Installing
----------

Clone the sphinx-ext-wikipedia repository ::

  $ git clone https://github.com/quiver/sphinx-ext-wikipedia.git

Copy extension module ::

  $ cp -r  sphinx-ext-wikipedia/sphinx-ext path/to/directory

Enabling the extension in Sphinx
--------------------------------

To enable the use of this extension in your Sphinx project, you will need 
to edit ``conf.py`` file in your Sphinx project.

First, add the extension module path to ``sys.path``. ::

    sys.path.append(os.path.abspath('path/to/ext/directory'))

Then, enable this extention by adding ``wikipedia`` to the list of
``extensions``. ::

    extensions += [ 'wikipedia']

Configuration
-------------

You can set the following config value in your Sphinx project's 
``conf.py`` file.

wikipedia_lang

    Defalut languge of the wikipedia.
    If not specified, this defaults to ``"en"``. ::

        wikipedia_lang = "fi"   #Finnish
    
Usage
-----

In your restructuredText markup, you can create links to various Trac 
entities using markup of the following format::

To link to a *Sphinx* article ::

    :wikipedia:`Sphinx`

To link to a *Sphinx* article with explicit title *mythical creature* ::

    :wikipedia:`mythical creature <Sphinx>`

To link to a non-default language article, use ``:lang:article`` markup ::

    :wikipedia:`:zh:斯芬克斯`

Of course, you can mix explicit title and non-default language ::

    :wikipedia:`Answer to the Ultimate Question of Life, the Universe, and Everything <:de:42 (Antwort)>`

