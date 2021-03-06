.. index:: P-Sphinx Theme; main sphinx theme, sphinx theme; p-main_theme (main theme)


==================================
"P-MAIN THEME" master sphinx theme
==================================


.. index:: P-Sphinx Theme; features

Features
========
This package provides a theme called "p-main_theme" which is the master theme of *P-Sphinx Theme*. A derivative called
`p-red` is used to generate this documentation.

Aside from being just another Sphinx theme, it has a few special features:

*Toggleable sections*
   You can mark sections with ``.. rst-class:: html-toggle``, which will make the section default to being collapsed under
   html, with a "show section" toggle link to the right of the title.

*Additional CSS classes*
   It provides a couple of simple styling directives for adding variety to long Python library documentation:

   - You can mark tables with ``.. rst-class:: html-plain-table`` to remove separating lines between rows.

   - You can mark ``<h2>`` sections with ``.. rst-class:: emphasize-children`` to provide addition visual dividers between
      large numbers of sub-sub-sections.

*Navigation enhancements*
   It provides options (``roottarget``, ``logotarget``) which allow the table of contents to be a distinct from the front
   page (``index.html``) of the document. This allows a master table of contents to be maintained, while still allowing the
   front page to be fully customized to welcome readers.

*Additional styling options*
   It also provides a number of styling options controlling small details such as external links, document sizing, etc.
   See below.

   It also uses an adaptive layout to work well on all screen sizes from mobile phones to widescreen desktops.

*Google Analytics Integration*
   By enabling two theme options within ``conf.py``, *P-Sphinx Theme* will automatically insert a Google Analytics tracker to
   the bottom  of each page, along with a polite link allowing users to set a cookie which opts them out.


.. _`special_target_values`:

*Special Target Values*
   ``<toc>``: the special value ``<toc>``, which uses the table of contents

   ``<root>``: the special value ``<root>``, which mirrors ``roottarget`` option see `Structure`_.


.. rst-class:: emphasize-children

.. index:: P-Sphinx Theme; options, Options; main options

List of Options
===============

.. important::

   Defaults for any additional theme might be different: these below are the one from the ``p-main_theme`` theme

Structure
---------
``roottarget``
   Sets to which page the title link in the navigation bar should point to
   (defaults to ``roottarget = index``).

``logotarget``
   Sets the page to which the sidebar logo (if any) should point to
   (defaults to ``logotarget = <root>``).


   .. seealso:: :ref:`Special Target Values <special_target_values>`

Document Layout
---------------
``max_width``
   (*inches*: an integer): Sets the maximum document width in inches, so the documentation does not stretch too far on wide
   monitors (defaults to ``max_width = 14``).

``compact_width``
   (*pixels*: an integer): Sets the maximum width in pixels where the "compact" layout will be used.
   This layout omits some of the padding and styling, and is  more suitable for smaller screens
   (defaults to ``compact_width = 960``).

``minimal_width``
   (*pixels*: an integer): Sets the maximum width in pixels where the "mobile" layout will be used.
   This layout omits the sidebar and everything else that can be trimmed, and is designed to (hopefully) be more usable on
   mobile devices. (defaults to ``minimal_width = 700``).

``min_height``
   (*inches*: an integer): Sets the minimum height of the page body in inches. (defaults to ``min_height = 6``).


.. index:: Options; decor options

Decor
-----
``borderless_decor``
   (true or false): Set to remove border between document and rest of page (defaults to ``borderless_decor = false``).

``beveled_decor``
   (true or false): Adds some bevels to some elements (defaults to ``beveled_decor = false``).

``lighter_decor``
   (true or false): Changes color for some elements (defaults to ``lighter_decor = false``).

``main_boarder_bg_color``
   (color): Sets the footer & border between document and rest of page background color.
   (defaults to ``main_boarder_bg_color = #1A4162``).


.. index:: Options; external references / diverse options

Diverse Configurations
----------------------
``externalrefs``
   (true or false): Controls whether references should be displayed with an icon. (defaults to ``externalrefs = true``).

``externalrefsicon``
   (image or string): Optional image or string to prefix before any external links.
   (defaults to ``externalrefsicon = "\21D7"`` rendered as ``⇗``).

``issueicon``
   (image or string): Optional image or string to prefix before any issue tracker links generated by
   :mod:`PSphinxTheme.ext.issue_tracker`
   (defaults to ``issueicon = "\2727"`` rendered as ``✧``, ignored if ``externalrefs=False``).


``fontcssurl``
   (url or path): For loading in fonts (e.g. google fonts: ``//fonts.googleapis.com/css?family=Open+Sans|Droid+Sans+Mono``)
   Or set it to a local css file which loads fonts. (defaults to ``fontcssurl = _static/local_fonts.css``).


.. index:: Options; googleanalytics options

Googleanalytics
~~~~~~~~~~~~~~~
``googleanalytics_id``
   (string): Setting this via ``html_theme_options`` to your GA id (e.g. ``UA-XXXXXXXX-X``)
   will enable a `Google Analytics <http://www.google.com/analytics>`_
   tracker for all pages in the document, as well insert a link in the footer allowing users to opt out of tracking.
   (defaults to not set ``googleanalytics_id =``).

``googleanalytics_path``
   (string): Setting this allows limiting the tracker to a subpath, useful for shared documentation hosting
   (e.g. PyPI or ReadTheDocs). e.g. ``googleanalytics_path = /project/``
   (defaults to ``googleanalytics_path = /``).


.. index:: Sidebar; sidebar options, Options; sidebar options

Sidebar
-------

Sidebar Layout
~~~~~~~~~~~~~~
``sidebarwidth``
   (*pixels*: an integer): Sets the width of the sidebar in pixels. (defaults to ``sidebarwidth = 230``).

``rightsidebar``
   (true or false): Sets whether the sidebar is on the right side instead of the left (defaults to ``rightsidebar = false``).

``stickysidebar``
   (true or false): Sets whether the sidebar should "stay in view" as the page is scrolled, otherwise it will stay fix at the
   original position. (defaults to ``stickysidebar = true``)

   .. note::

      if the `sidebar` has more entries than what can be displayed in the current window view, it will not "stay in view"
      even if ``stickysidebar`` is set to true.

``collapsiblesidebar``
   (true or false): Sets whether the sidebar can be hidden or not (defaults to ``collapsiblesidebar = true``).

``defaultcollapsed``
   (true or false): Sets whether the sidebar should start collapsed (defaults to ``defaultcollapsed = false``).

``sidebar_prev_next``
   (true or false): Sets whether sidebar should include the `sidebar_prev_title` and `sidebar_next_title`
   (defaults to ``sidebar_prev_next = false``).

``sidebar_highlighttoc``
   (true or false): Sets whether sidebar should highlight the sections which are currently being viewed
   (defaults to ``sidebar_highlighttoc = true``).

``sidebar_popuptoc``
   (true or false): By default, TOC entries which overflow the sidebar will be cut off until the cursor hovers over the
   sidebar, at which point they will expand across the document. to disable this feature (and make them wrap within the
   sidebar), set ``sidebar_popuptoc=false``. (defaults to ``sidebar_popuptoc = true``).

Sidebar Labels
~~~~~~~~~~~~~~
``sidebar_localtoc_title``
   (text): Sets title of per-page table of contents header (in ``localtoc.html`` sidebar).
   (defaults to ``sidebar_localtoc_title = Page contents``).

``sidebar_prev_title``
   (text): Sets title of link to previous page header (in ``relations.html`` sidebar). (defaults to ``Previous page``).

``sidebar_next_title``
   (text): Sets title of link to next page header (in ``relations.html`` sidebar).
   (defaults to ``sidebar_prev_title = Next page``).

``sidebar_quicklinks_title``
   (text): Sets title of the quick links header (in ``quicklinks.html`` sidebar).
   (defaults to ``sidebar_quicklinks_title = Quick Links``).

``sidebar_root_title``
   (text): Sets title of the root document link (in ``quicklinks.html`` sidebar).
   (defaults to ``sidebar_root_title = Front Page``).

Sidebar Styling
~~~~~~~~~~~~~~~
``sidebarbgcolor``
   (color): Sets the sidebar background color. (defaults to ``sidebarbgcolor = #F2F2F2``).

``sidebartextcolor``
   (color): Sets the sidebar text color. (defaults to ``sidebartextcolor = #777777``).

``sidebarlinkcolor``
   (color): Sets the sidebar linkcolor color. (defaults to ``sidebarlinkcolor = #003469``).

``sidebarhighcolor``
   (color): Sets the sidebar highcolor color. (defaults to ``sidebarhighcolor = #FFF8E4``).

``sidebar_boarder_color``
   (color): Sets the sidebar trimcolor color. e.g. sidebar searchbox input border
   (defaults to ``sidebar_boarder_color = rgba(0,0,0,.2)``).

``sidebarsearchtipcolor``
   (color): Sets the sidebar searchtip color. (defaults to ``sidebarsearchtipcolor = #999999``).

``sidebar_button_bg``
   (color): Sets the sidebar buttons background color. (defaults to ``sidebar_button_bg = #F2F2F2``).

``sidebar_button_bg_hover``
   (color): Sets the sidebar buttons background hover color. (defaults to ``sidebar_button_bg_hover = rgba(255,0,0,.2)``).


.. index:: Relation bar; relation bar options, Options; relation bar options

Top & Bottom Relation bar
-------------------------
``relbarbgcolor``
   (color): Sets the background color for the relation bar. (defaults to ``relbarbgcolor = #5682AD``).

``relbartextcolor``
   (color): Sets the text color for the relation bar. (defaults to ``relbartextcolor = #ffffff``).

``relbarlinkcolor``
   (color): Sets the link color for the relation bar. (defaults to ``relbarlinkcolor = #ffffff``).

``relbar_link_bg``
   (color): Sets the link background color for the relation bar. (defaults to ``relbar_link_bg = rgba(0,0,0,.1)``).

``relbar_link_bg_hover``
   (color): Sets the relation bar link background hover color. (defaults to ``relbar_link_bg_hover = rgba(0,0,0,.2)``).


Content Pages
-------------

.. index:: Options; page body options

Page Body
~~~~~~~~~

``bodylineheight``
   (*em*: a float): Sets the body line height in ``em``. (defaults to ``bodylineheight = 1.5``).

   .. note:: `em`

      An `em` is a unit in the field of typography, equal to the currently specified point size.
      1em is equal to the current font size. 2em means 2 times the size of the current font. E.g., if an element is
      displayed with a font of 12 pt, then '2em' is 24 pt.

``bodyfont``
   (font-family): Sets the body font for normal text. (defaults to ``bodyfont = "Noto Sans"``).

``body_boarder_color``
   (color): Sets the body boarder color (e.g. between body and sidebar) of the page.
   (defaults to ``body_boarder_color = rgba(0,0,0,.12)``).

``bgcolor``
   (color): Sets the body background color of the page. (defaults to ``bgcolor = #ffffff``).

``textcolor``
   (color): Sets the body text color of the page. (defaults to ``textcolor = #000000``).

``linkcolor``
   (color): Sets the body links color of the page. (defaults to ``linkcolor = #003469``).

``highlightcolor``
   (color): Sets the body highlight color (e.g. footnotes targets ) of the page.
   (defaults to ``highlightcolor = #fbe54e``).


.. index:: Code; code block options, Options; code block options

Code Blocks
```````````
``codeblockfont``
   (font-family): Sets the font for code blocks.
   (defaults to ``codeblockfont = "Source Code Pro"``).

``codebgcolor``
   (color): Sets the background color for code blocks.
   (defaults to ``codebgcolor = #eeffcc``).

``codetextcolor``
   (color): Sets the text color for code blocks.
   (defaults to ``codetextcolor = #111111``).

   .. note:: usually *code block text color* is additional adjusted by *pygments style*

``code_boarder_color``
   (color): Sets the boarder color for code blocks.
   (defaults to ``code_boarder_color = #AACC99``).

.. index:: Docstrings; code docstrings options, Options; code docstrings options

Docstrings
``````````
``docstring_descclassname_color``
   (color): Sets the background color for code `docstring descclassname` part.
   (defaults to ``docstring_descclassname_color = transparent``).

``docstring_descclassname_font_weight``
   (font-weight): Sets the font weight for code `docstring descclassname` part.
   (defaults to ``docstring_descclassname_font_weight = normal``).

   .. note:: `font-weight`

      ::

         normal
         bold
         bolder
         lighter
         100
         200
         300
         400 (400 is the same as normal)
         500
         600
         700 (700 is the same as bold)
         800
         900


``docstring_descclassname_font_size``
   (*em*: a float): Sets the code `docstring descclassname` part height in ``em``.
   (defaults to ``docstring_descclassname_font_size = 1.1``).

   .. note:: `em`

      An `em` is a unit in the field of typography, equal to the currently specified point size.
      1em is equal to the current font size. 2em means 2 times the size of the current font. E.g., if an element is
      displayed with a font of 12 pt, then '2em' is 24 pt.

``docstring_descname_color``
   (color): Sets the background color for code `docstring descname` part.
   (defaults to ``docstring_descname_color = rgba(242, 242, 242, 0.5)``).

``docstring_descname_font_weight``
   (font-weight): Sets the font weight for code `docstring descclassname` part.
   (defaults to ``docstring_descname_font_weight = normal``).

``docstring_descname_font_size``
   (*em*: a float): Sets the code `docstring descname` part height in ``em``.
   (defaults to ``docstring_descname_font_size = 1.2``).


.. index:: Literals; literals / quoted text options, Options; literals / quoted text options

Quoted Text / Literals
``````````````````````
``quotedtxtfont``
   (font-family): Sets the font for code quoted text / literals.
   (defaults to ``quotedtxtfont = "Droid Sans Mono"``).

``quotedbgcolor``
   (color): Sets the body color of the page for **quoted** text. eg. ``literal``.
   (defaults to ``quotedbgcolor = rgba(0,0,0,.075)``).

``quoted_boarder_color``
   (color): Sets the body boarder ``quoted text`` color of the page.
   (defaults to ``quoted_boarder_color = rgba(0,0,0,.05)``).

``literalvariablesfont``
   (font-family): Sets the font for code variables in samp.literal parts.
   (defaults to ``literalvariablesfont = "Noticia Text"``).

   .. seealso:: :mod:`~PSphinxTheme.ext.escaped_samp_literals` extension.


.. index:: Headings; headers options, Options; headers options

Page & Section & Rubrics Headers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
``headfont``
   (font-family): Sets the font for page and section headings. (defaults to ``headfont = "Noto Serif"``).

``headtextcolor``
   (color): Sets the text color for page headings. (defaults to ``headtextcolor = #000000``).

``headlinkcolor``
   (color): Sets the link color for page headings *Permalink* ''¶''. (defaults to ``headlinkcolor = #003469``).

``sectionbgcolor``
   (color): Sets the background color for sections. (defaults to ``sectionbgcolor = #84A6C7``).

``rubricbgcolor``
   (color): Sets the background color for rubrics. (defaults to ``rubricbgcolor = #92BCDE``).

``sectiontextcolor``
   (color): Sets the text color for for sections headings /rubrics. (defaults to ``sectiontextcolor = #ffffff``).

``section_boarder_color``
   (color): Sets the boarder color for sections/rubrics. (defaults to ``section_boarder_color = rgba(0,0,0,.125)``).

``section_border_top_width``
   (*pixels*: an integer): Sets the border top width in pixels for sections/rubrics.
   (defaults to ``sectionborder_top_width  = 0``).

``section_border_right_width``
   (*pixels*: an integer): Sets the boarder right width in pixels for sections/rubrics.
   (defaults to ``section_border_right_width = 1``).

``section_boarder_bottom_width``
   (*pixels*: an integer): Sets the boarder bottom width in pixels for sections/rubrics.
   (defaults to ``section_boarder_bottom_width = 1``).

``section_boarder_left_width``
   (*pixels*: an integer): Sets the boarder left width in pixels for sections/rubrics.
   (defaults to ``section_boarder_left_width = 1``).


.. _`admonitions_deprecated_todo`:

.. index:: Admonitions; main admonition options, Options; main admonition options

Admonitions & deprecated / todo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
``inline_admonitions``
   (true or false): Merges the title into the first paragraph (defaults to ``inline_admonitions = true``).

``admonition_boarder_color``
   (color): Sets the boarder color for admonitions. (defaults to ``admonition_boarder_color = rgba(0,0,0,.05)``).

``admonition_title_color``
   (color): Sets the title color for admonitions. (defaults to ``admonition_title_color = rgba(0,0,0,.05)``).

``admonition_size``
   (*%*: a float): Sets the size for admonitions in ``%``. (defaults to ``admonition_size = 90.0``).


``admonition_todo_color``
   (color): Sets the background color for the ``todo`` admonition. (defaults to ``admonition_todo_color = #FFF7E0``).

   .. important:: This needs the `Sphinx extension todo <http://sphinx-doc.org/ext/todo.html>`_

``admonition_deprecated_color``
   (color): Sets the background color for thr ``deprecated`` directive.
   (defaults to ``admonition_deprecated_color = #fbece0``).

``admonition_note_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``note``.
   (defaults to ``admonition_note_color = #E7F0FE``).

``admonition_tip_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``tip``.
   (defaults to ``admonition_tip_color = #f8defd``).

``admonition_important_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``important``.
   (defaults to ``admonition_important_color = #feffd6``).

``admonition_warning_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``warning``.
   (defaults to ``admonition_warning_color = #efc2c2``).

``admonition_seealso_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``seealso``.
   (defaults to ``admonition_seealso_color = #FFF7E0``).

``admonition_optional_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``optional``.
   (defaults to ``admonition_optional_color = #FFFFFF``).

``admonition_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``example``.
   (defaults to ``admonition_example_color = #d1ffd6``).

``admonition_python_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``python-example``.
   (defaults to ``admonition_python_example_color = #d1ffd6``).

``admonition_shell_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``shell-example``.
   (defaults to ``admonition_shell_example_color = #d1ffd6``).

``admonition_javascript_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``javascript-example``.
   (defaults to ``admonition_javascript_example_color = #d1ffd6``).

``admonition_json_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``json-example``.
   (defaults to ``admonition_json_example_color = #d1ffd6``).

``admonition_lconf_example_color``
   (color): Sets the background color for the *P-Sphinx Theme* admonition ``lconf-example``.
   (defaults to ``admonition_lconf_example_color = #fff0c7``).


**seealso:** the *P-Sphinx Theme extension* :doc:`All official P-SphinxTheme admonitions <api/PSphinxTheme.ext.psphinx_admonitions>`


.. index:: Tables; tables options, Options; tables options

Tables
~~~~~~
``table_header_color``
   (color): Sets the table header color. (defaults to ``table_header_color = rgba(0,0,0,.15)``).

``table_shade_color``
   (color): Sets the table row shade color. (defaults to ``table_shade_color = rgba(0,0,0,.06)``).

``table_boarder_color``
   (color): Sets the table boarder (incl. `table column dividers`) shade color.
   (defaults to ``table_boarder_color = rgba(0,0,0,.15)``).

   .. note:: for mor info on ``table column dividers`` see the *P-Sphinx Theme* extension
      :mod:`~PSphinxTheme.ext.table_styling` extension.

Footer
~~~~~~
``footertextcolor``
   (color): Sets the footer text color. (defaults to ``footertextcolor = #B0B0B0``).

Index page
~~~~~~~~~~
``index_category_color``
   (color): Sets the index category color. (defaults to ``index_category_color = #84ADBE``).

   .. note:: requires classes set by the *P-Sphinx Theme extension* :mod:`~PSphinxTheme.ext.index_styling`


.. _usage_example:

.. index:: Usage; using the theme ``conf.py``

Usage
=====

Using the theme
---------------
To use the *P-SphinxTheme*, open your documentation's Sphinx ``conf.py`` file, make the following changes::

   # import at least "set_psphinxtheme"
   from PSphinxTheme.utils import set_psphinxtheme

::

   # =====================================================================
   # PSphinxTheme's extensions

   # a collection of all "official P-SphinxTheme admonitions"
   'PSphinxTheme.ext.psphinx_admonitions',

   # replace sphinx :samp: role handler with one that allows escaped {} chars
   'PSphinxTheme.ext.escaped_samp_literals',

   # adds extra ids & classes to genindex html, for additional styling
   'PSphinxTheme.ext.index_styling',

   # add "issue" role
   'PSphinxTheme.ext.issue_tracker',

   # modify logo per page
   'PSphinxTheme.ext.sidebarlogo_perpag',

   # inserts any link entries into the navigation bar (``relbar``)
   'PSphinxTheme.ext.relbar_links',

   # allow table column alignment styling
   'PSphinxTheme.ext.table_styling',

::

   issue_tracker_url = 'gh:peter1000/PSphinxTheme'

   # set the: html_theme_path, html_theme, needs_sphinx
   html_theme_path, html_theme, needs_sphinx = set_psphinxtheme('p-red')


   # [optional] overwrite some of the default options listed above...
   html_theme_options = { "lighter_decor": True }

   # The name of an image file (relative to this directory) to place at the top of the sidebar.
   html_logo = path_join('_static', 'P-SphinxTheme180_95_logo.png')
   # The name of an image file (within the static path) to use as favicon of the docs.
   html_favicon = path_join('_static', 'P-Projects32_32.ico')

   # The api document: extension: relbar_links
   relbar_links_doc = [
      ('toc', 'contents'),
      ('api', 'api'),
   ]
   # modify logo per page: using: `P-Sphinx Theme extension`: sidebarlogo_perpag
   sidebarlogo_perpage_dict = {
      None: ['api', 'index', 'copyright'],
      'P-SphinxTheme180_95_bg.png': ['main_theme', 'history'],
   }


   # [optional] Add custom sidebar templates, maps document names to template names.
   common_sidebars = ['quicklinks.html', 'sourcelink.html', 'searchbox.html']
   html_sidebars = {
      '**': ['localtoc.html', 'relations.html'] + common_sidebars,
      'py-modindex': common_sidebars,
      'genindex': common_sidebars,
      'search': common_sidebars,
   }



Section Styles
--------------

.. seealso:: See the next pages for examples of these options in action.

   - :doc:`theme_test`

Emphasized Children
~~~~~~~~~~~~~~~~~~~
Adding ``.. rst-class:: emphasize-children`` to a 2nd-level section header will cause the headers of all of it's child
sections to be emphasized with a solid background.
This is mainly useful for very long sections, where there needs to be a visual divide between 3rd-level sections.

Toggleable Sections
~~~~~~~~~~~~~~~~~~~
By adding ``.. rst-class:: html-toggle`` before any section header, it can be made toggleable::

   .. rst-class:: html-toggle

   Toggleable Section
   ------------------

   This section is collapsed by default.

While toggleable sections start out collapsed by default, you can use ``.. rst-class:: html-toggle expanded`` to override
this.

Table Styles
------------
- Adding ``.. rst-class:: plain`` can be used to remove the row shading and other styling from a table.

- Adding ``.. rst-class:: centered`` can be used to center a table.

- Adding ``.. rst-class:: fullwidth`` can be used to expand a table to the full width of the page.

.. seealso::
   The :mod:`~PSphinxTheme.ext.table_styling` extension for additional table styling abilities, e.g. per-column text
   alignment.
