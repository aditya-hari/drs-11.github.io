+++
title = "syntax"
draft = false
tags = [
    "",
    "var",
    "www",
    "html",
    "dokuwiki",
    "data",
    "pages",
    "wiki",
    "syntax"
]

date = "2020-07-29"
+++
# Formatting Syntax 

<img style######` src'/img/< doku "DokuWiki" >'> supports some simple markup language, which tries to make the datafiles to be as readable as possible. This page contains all possible syntax you may use when editing the pages. Simply have a look at the source of this page by pressing "Edit this page". If you want to try something, just use the [playground](<img style######` src'/img/< relref "playground/playground.md" >'>) page. The simpler markup is easily accessible via <img style######'' src'/img/< doku "toolbar|quickbuttons" >'>, too.

## Basic Text Formatting 

DokuWiki supports **bold**, *italic*, __underlined__ and `monospaced` texts. Of course you can **__*`combine`*__** all these.

  DokuWiki supports **bold**, *italic*, __underlined__ and `monospaced` texts.
  Of course you can **__*`combine`*__** all these.

You can use <sub>subscript</sub> and <sup>superscript</sup>, too.

  You can use <sub>subscript</sub> and <sup>superscript</sup>, too.

You can mark something as ~~deleted~~ as well.

  You can mark something as ~~deleted~~ as well.

**Paragraphs** are created from blank lines. If you want to **force a newline** without a paragraph, you can use two backslashes followed by a whitespace or the end of line.

This is some text with some linebreaks<br/><br/> Note that the
two backslashes are only recognized at the end of a line<br/><br/>
or followed by<br/><br/> a whitespace <br/><br/>this happens without it.

  This is some text with some linebreaks<br/><br/> Note that the
  two backslashes are only recognized at the end of a line<br/><br/>
  or followed by<br/><br/> a whitespace <br/><br/>this happens without it.

You should use forced newlines only if really needed.

## Links 

DokuWiki supports multiple ways of creating links.

### External 

External links are recognized automagically: http:*www.google.com or simply www.google.com - You can set the link text as well: [This Link points to google](http:*www.google.com). Email addresses like this one: <andi@splitbrain.org> are recognized, too.

  DokuWiki supports multiple ways of creating links. External links are recognized
  automagically: http://www.google.com or simply www.google.com - You can set
  link text as well: [This Link points to google](http://www.google.com). Email
  addresses like this one: <andi@splitbrain.org> are recognized, too.

### Internal 

Internal links are created by using square brackets. You can either just give a [pagename](<img style######` src'/img/< relref "pagename.md" >'>) or use an additional [link text](<img style######` src'/img/< relref "pagename.md" >'>).

  Internal links are created by using square brackets. You can either just give
  a [pagename](<img style######` src'/img/< relref "pagename.md" >'>) or use an additional [link text](<img style######` src'/img/< relref "pagename.md" >'>).

<img style######'' src'/img/< doku "pagename|Wiki pagenames" >'> are converted to lowercase automatically, special characters are not allowed.

You can use [some/namespaces](<img style######'' src'/img/< relref "some/namespaces.md" >'>) by using a colon in the pagename.

  You can use [some/namespaces](<img style######'' src'/img/< relref "some/namespaces.md" >'>) by using a colon in the pagename.

For details about namespaces see <img style######'' src'/img/< doku "namespaces" >'>.

Linking to a specific section is possible, too. Just add the section name behind a hash character as known from HTML. This links to [this Section](<img style######'' src'/img/< relref "syntax#internal.md" >'>).

  This links to [this Section](<img style######'' src'/img/< relref "syntax#internal.md" >'>).

Notes:

  * Links to [existing pages](<img style######` src'/img/< relref "syntax.md" >'>) are shown in a different style from [nonexisting](<img style######` src'/img/< relref "nonexisting.md" >'>) ones.
  * DokuWiki does not use <img style######` src'/img/< wp "CamelCase" >'> to automatically create links by default, but this behavior can be enabled in the <img style######` src'/img/< doku "config" >'> file. Hint: If DokuWiki is a link, then it's enabled.
  * When a section's heading is changed, its bookmark changes, too. So don't rely on section linking too much.

### Interwiki 

DokuWiki supports <img style######` src'/img/< doku "Interwiki" >'> links. These are quick links to other Wikis. For example this is a link to Wikipedia's page about Wikis: <img style######` src'/img/< wp "Wiki" >'>.

  DokuWiki supports <img style######'' src'/img/< doku "Interwiki" >'> links. These are quick links to other Wikis.
  For example this is a link to Wikipedia's page about Wikis: <img style######'' src'/img/< wp "Wiki" >'>.

### Windows Shares 

Windows shares like [this](<img style######` src'/img/< relref "<br/><br/>server<br/>share.md" >'>) are recognized, too. Please note that these only make sense in a homogeneous user group like a corporate <img style######` src'/img/< wp "Intranet" >'>.

  Windows Shares like [this](<img style######'' src'/img/< relref "<br/><br/>server<br/>share.md" >'>) are recognized, too.

Notes:

  * For security reasons direct browsing of windows shares only works in Microsoft Internet Explorer per default (and only in the "local zone").
  * For Mozilla and Firefox it can be enabled through different workaround mentioned in the [Mozilla Knowledge Base](http://kb.mozillazine.org/Links_to_local_pages_do_not_work). However, there will still be a JavaScript warning about trying to open a Windows Share. To remove this warning (for all users), put the following line in `conf/lang/en/lang.php` (more details at <img style######'' src'/img/< doku "localization#changing_some_localized_texts_and_strings_in_your_installation|localization" >'>): ```-
<?php
/**
 * Customization of the english language file
 * Copy only the strings that needs to be modified
 */
$lang['js']['nosmblinks'] = '';
```

### Image Links 

You can also use an image to link to another internal or external page by combining the syntax for links and [images](<img style######'' src'/img/< relref "#images_and_other_files.md" >'>) (see below) like this:

  [<img style######'' src'/img/wiki/dokuwiki-128.png'>](http://php.net)

[<img style######'' src'/img/wiki/dokuwiki-128.png'>](http://php.net)

Please note: The image formatting is the only formatting syntax accepted in link names.

The whole [image](<img style######` src'/img/< relref "#images_and_other_files.md" >'>) and [link](<img style######` src'/img/< relref "#links.md" >'>) syntax is supported (including image resizing, internal and external images and URLs and interwiki links).

## Footnotes 

You can add footnotes ((This is a footnote)) by using double parentheses.

  You can add footnotes ((This is a footnote)) by using double parentheses.

## Sectioning 

You can use up to five different levels of headlines to structure your content. If you have more than three headlines, a table of contents is generated automatically -- this can be disabled by including the string `<nowiki>~~NOTOC~~</nowiki>` in the document.

### Headline Level 3 
#### Headline Level 4 
##### Headline Level 5 

  ### Headline Level 3 
  #### Headline Level 4 
  ##### Headline Level 5 

By using four or more dashes, you can make a horizontal line:

----

## Media Files 

You can include external and internal <img style######'' src'/img/< doku "images|images, videos and audio files" >'> with curly brackets. Optionally you can specify the size of them.

Real size:                        <img style######'' src'/img/wiki/dokuwiki-128.png'>

Resize to given width:            <img style######'width: 50px;' src'/img/wiki/dokuwiki-128.png'>

Resize to given width and height((when the aspect ratio of the given width and height doesn't match that of the image, it will be cropped to the new ratio before resizing)): <img style######'width: 200px; height: 50px;' src'/img/wiki/dokuwiki-128.png'>

Resized external image:           <img style######'width: 200px; height: 50px;' src'/img/https///secure.php.net/images/php.gif'>

  Real size:                        <img style######'' src'/img/wiki/dokuwiki-128.png'>
  Resize to given width:            <img style######'width: 50px;' src'/img/wiki/dokuwiki-128.png'>
  Resize to given width and height: <img style######'width: 200px; height: 50px;' src'/img/wiki/dokuwiki-128.png'>
  Resized external image:           <img style######'width: 200px; height: 50px;' src'/img/https///secure.php.net/images/php.gif'>


By using left or right whitespaces you can choose the alignment.

<img style######'float: left;' src'/img/wiki/dokuwiki-128.png'>

<img style######'float: right;' src'/img/wiki/dokuwiki-128.png'>

<img style######'margin-left: auto; margin-right: auto;' src'/img/wiki/dokuwiki-128.png'>

  <img style######'float: left;' src'/img/wiki/dokuwiki-128.png'>
  <img style######'float: right;' src'/img/wiki/dokuwiki-128.png'>
  <img style######'margin-left: auto; margin-right: auto;' src'/img/wiki/dokuwiki-128.png'>

Of course, you can add a title (displayed as a tooltip by most browsers), too.

<img style######'float: left;' src'/img/wiki/dokuwiki-128.png |This is the caption'>

  <img style######'float: left;' src'/img/wiki/dokuwiki-128.png |This is the caption'>

For linking an image to another page see [#Image Links](<img style######'' src'/img/< relref "#Image_Links.md" >'>) above.

### Supported Media Formats 

DokuWiki can embed the following media formats directly.

| Image | `gif`, `jpg`, `png`  |
| Video | `webm`, `ogv`, `mp4` |
| Audio | `ogg`, `mp3`, `wav`  |
| Flash | `swf`                    |

If you specify a filename that is not a supported media format, then it will be displayed as a link instead.

By adding `?linkonly` you provide a link to the media without displaying it inline

  <img style######'width: linkonlypx;' src'/img/wiki/dokuwiki-128.png'>

<img style######'width: linkonlypx;' src'/img/wiki/dokuwiki-128.png'> This is just a link to the image.

### Fallback Formats 

Unfortunately not all browsers understand all video and audio formats. To mitigate the problem, you can upload your file in different formats for maximum browser compatibility.

For example consider this embedded mp4 video:

  <img style######'' src'/img/video.mp4|A funny video'>

When you upload a `video.webm` and `video.ogv` next to the referenced `video.mp4`, DokuWiki will automatically add them as alternatives so that one of the three files is understood by your browser.

Additionally DokuWiki supports a "poster" image which will be shown before the video has started. That image needs to have the same filename as the video and be either a jpg or png file. In the example above a `video.jpg` file would work.

## Lists 

Dokuwiki supports ordered and unordered lists. To create a list item, indent your text by two spaces and use a `*` for unordered lists or a `-` for ordered ones.

  * This is a list
  * The second item
    * You may have different levels
  * Another item

  1. The same list but ordered
  2. Another item
    1. Just use indention for deeper levels
  3. That's it

```
  * This is a list
  * The second item
    * You may have different levels
  * Another item

  1. The same list but ordered
  2. Another item
    1. Just use indention for deeper levels
  3. That's it
```

Also take a look at the <img style######'' src'/img/< doku "faq/lists|FAQ on list items" >'>.

## Text Conversions 

DokuWiki can convert certain pre-defined characters or strings into images or other text or HTML.

The text to image conversion is mainly done for smileys. And the text to HTML conversion is used for typography replacements, but can be configured to use other HTML as well.

### Text to Image Conversions 

DokuWiki converts commonly used <img style######` src'/img/< wp "emoticon" >'>s to their graphical equivalents. Those <img style######` src'/img/< doku "Smileys" >'> and other images can be configured and extended. Here is an overview of Smileys included in DokuWiki:

  * :sunglasses: %%  :sunglasses:  %%
  * :flushed: %%  :flushed:  %%
  * :worried: %%  :worried:  %%
  * :simple_smile: %%  :simple_smile:  %%
  * ######)  %%  )   %%
  * :confused: %%  :confused:  %%
  * :-<br/> %%  :-<br/>  %%
  * :sweat: %%  :sweat:  %%
  * :laughing: %%  :laughing:  %%
  * :stuck_out_tongue: %%  :stuck_out_tongue:  %%
  * :open_mouth: %%  :open_mouth:  %%
  * :grimacing: %%  :grimacing:  %%
  * :expressionless: %%  :expressionless:  %%
  * :wink: %%  :wink:  %%
  * :smile: %%  :smile:  %%
  * :question: %%  :question:  %%
  * :exclamation: %%  :exclamation:  %%
  * :laughing: %%  :laughing:  %%
  * FIXME %%  FIXME %%
  * DELETEME %% DELETEME %%

### Text to HTML Conversions 

Typography: [DokuWiki](<img style######'' src'/img/< relref "DokuWiki.md" >'>) can convert simple text characters to their typographically correct entities. Here is an example of recognized characters.

-> <- <-> ######> < <=> >> << -- --- 640x480 (c) (tm) (r)
"He thought 'It's a man's world'..."

```
-> <- <-> ######> < <=> >> << -- --- 640x480 (c) (tm) (r)
"He thought 'It's a man's world'..."
```

The same can be done to produce any kind of HTML, it just needs to be added to the <img style######'' src'/img/< doku "entities|pattern file" >'>.

There are three exceptions which do not come from that pattern file: multiplication entity (640x480), 'single' and "double quotes". They can be turned off through a <img style######'' src'/img/< doku "config/typography|config option" >'>.

## Quoting 

Some times you want to mark some text to show it's a reply or comment. You can use the following syntax:

```
I think we should do it

> No we shouldn't

>> Well, I say we should

> Really?

>> Yes!

>>> Then lets do it!
```

I think we should do it

> No we shouldn't

>> Well, I say we should

> Really?

>> Yes!

>>> Then lets do it!

## Tables 

DokuWiki supports a simple syntax to create tables.

^ Heading 1      ^ Heading 2       ^ Heading 3          ^
| Row 1 Col 1    | Row 1 Col 2     | Row 1 Col 3        |
| Row 2 Col 1    | some colspan (note the double pipe) ||
| Row 3 Col 1    | Row 3 Col 2     | Row 3 Col 3        |

Table rows have to start and end with a `|` for normal rows or a `^` for headers.

  ^ Heading 1      ^ Heading 2       ^ Heading 3          ^
  | Row 1 Col 1    | Row 1 Col 2     | Row 1 Col 3        |
  | Row 2 Col 1    | some colspan (note the double pipe) ||
  | Row 3 Col 1    | Row 3 Col 2     | Row 3 Col 3        |

To connect cells horizontally, just make the next cell completely empty as shown above. Be sure to have always the same amount of cell separators!

Vertical tableheaders are possible, too.

|              ^ Heading 1            ^ Heading 2          ^
^ Heading 3    | Row 1 Col 2          | Row 1 Col 3        |
^ Heading 4    | no colspan this time |                    |
^ Heading 5    | Row 2 Col 2          | Row 2 Col 3        |

As you can see, it's the cell separator before a cell which decides about the formatting:

  |              ^ Heading 1            ^ Heading 2          ^
  ^ Heading 3    | Row 1 Col 2          | Row 1 Col 3        |
  ^ Heading 4    | no colspan this time |                    |
  ^ Heading 5    | Row 2 Col 2          | Row 2 Col 3        |

You can have rowspans (vertically connected cells) by adding `%%:::%%` into the cells below the one to which they should connect.

^ Heading 1      ^ Heading 2                  ^ Heading 3          ^
| Row 1 Col 1    | this cell spans vertically | Row 1 Col 3        |
| Row 2 Col 1    | :::                        | Row 2 Col 3        |
| Row 3 Col 1    | :::                        | Row 2 Col 3        |

Apart from the rowspan syntax those cells should not contain anything else.

  ^ Heading 1      ^ Heading 2                  ^ Heading 3          ^
  | Row 1 Col 1    | this cell spans vertically | Row 1 Col 3        |
  | Row 2 Col 1    | :::                        | Row 2 Col 3        |
  | Row 3 Col 1    | :::                        | Row 2 Col 3        |

You can align the table contents, too. Just add at least two whitespaces at the opposite end of your text: Add two spaces on the left to align right, two spaces on the right to align left and two spaces at least at both ends for centered text.

^           Table with alignment           ^^^
|         right|    center    |left          |
|left          |         right|    center    |
| xxxxxxxxxxxx | xxxxxxxxxxxx | xxxxxxxxxxxx |

This is how it looks in the source:

  ^           Table with alignment           ^^^
  |         right|    center    |left          |
  |left          |         right|    center    |
  | xxxxxxxxxxxx | xxxxxxxxxxxx | xxxxxxxxxxxx |

Note: Vertical alignment is not supported.

## No Formatting 

If you need to display text exactly like it is typed (without any formatting), enclose the area either with `%%<nowiki>%%` tags or even simpler, with double percent signs `<nowiki>%%</nowiki>`.

<nowiki>
This is some text which contains addresses like this: http://www.splitbrain.org and **formatting**, but nothing is done with it.
</nowiki>
The same is true for %%*__this__ text* with a smiley :wink:%%.

  <nowiki>
  This is some text which contains addresses like this: http://www.splitbrain.org and **formatting**, but nothing is done with it.
  </nowiki>
  The same is true for %%*__this__ text* with a smiley :wink:%%.

## Code Blocks 

You can include code blocks into your documents by either indenting them by at least two spaces (like used for the previous examples) or by using the tags `%%```%%` or `%%```%%`.

  This is text is indented by two spaces.

```
This is preformatted code all spaces are preserved: like              <-this
```

```
This is pretty much the same, but you could use it to show that you quoted a file.
```

Those blocks were created by this source:

    This is text is indented by two spaces.

  ```
  This is preformatted code all spaces are preserved: like              <-this
  ```

  ```
  This is pretty much the same, but you could use it to show that you quoted a file.
  ```

### Syntax Highlighting 

[wiki/DokuWiki](<img style######` src'/img/< relref "wiki/DokuWiki.md" >'>) can highlight sourcecode, which makes it easier to read. It uses the [GeSHi](http://qbnz.com/highlighter/) Generic Syntax Highlighter -- so any language supported by GeSHi is supported. The syntax uses the same code and file blocks described in the previous section, but this time the name of the language syntax to be highlighted is included inside the tag, e.g. `<nowiki>```java</nowiki>` or `<nowiki>```java</nowiki>''.

```java
/**
 * The HelloWorldApp class implements an application that
 * simply displays "Hello World!" to the standard output.
 */
class HelloWorldApp {
    public static void main(String[] args) {
        System.out.println("Hello World!"); //Display the string.
    }
}
```

The following language strings are currently recognized: *4cs 6502acme 6502kickass 6502tasm 68000devpac abap actionscript3 actionscript ada aimms algol68 apache applescript apt_sources arm asm asp asymptote autoconf autohotkey autoit avisynth awk bascomavr bash basic4gl batch bf biblatex bibtex blitzbasic bnf boo caddcl cadlisp ceylon cfdg cfm chaiscript chapel cil c_loadrunner clojure c_mac cmake cobol coffeescript c cpp cpp-qt cpp-winapi csharp css cuesheet c_winapi dart dcl dcpu16 dcs delphi diff div dos dot d ecmascript eiffel email epc e erlang euphoria ezt f1 falcon fo fortran freebasic freeswitch fsharp gambas gdb genero genie gettext glsl gml gnuplot go groovy gwbasic haskell haxe hicest hq9plus html html4strict html5 icon idl ini inno intercal io ispfpanel java5 java javascript jcl j jquery julia kixtart klonec klonecpp kotlin latex lb ldif lisp llvm locobasic logtalk lolcode lotusformulas lotusscript lscript lsl2 lua m68k magiksf make mapbasic mathematica matlab mercury metapost mirc mk-61 mmix modula2 modula3 mpasm mxml mysql nagios netrexx newlisp nginx nimrod nsis oberon2 objc objeck ocaml-brief ocaml octave oobas oorexx oracle11 oracle8 oxygene oz parasail parigp pascal pcre perl6 perl per pf phix php-brief php pic16 pike pixelbender pli plsql postgresql postscript povray powerbuilder powershell proftpd progress prolog properties providex purebasic pycon pys60 python qbasic qml q racket rails rbs rebol reg rexx robots roff rpmspec rsplus ruby rust sas sass scala scheme scilab scl sdlbasic smalltalk smarty spark sparql sql sshconfig standardml stonescript swift systemverilog tclegg tcl teraterm texgraph text thinbasic tsql twig typoscript unicon upc urbi uscript vala vbnet vb vbscript vedit verilog vhdl vim visualfoxpro visualprolog whitespace whois winbatch wolfram xbasic xml xojo xorg_conf xpp yaml z80 zxbasic*

There are additional <img style######'' src'/img/< doku "syntax_highlighting|advanced options" >'> available for syntax highlighting, such as highlighting lines or adding line numbers.

### Downloadable Code Blocks 

When you use the `%%```%%` or `%%```%%` syntax as above, you might want to make the shown code available for download as well. You can do this by specifying a file name after language code like this:

```
```php
<?php echo "hello world!"; ?>
```
```

```php
<?php echo "hello world!"; ?>
```

If you don't want any highlighting but want a downloadable file, specify a dash (`-`) as the language code: `%%```-%%`.


## Embedding HTML and PHP 

You can embed raw HTML or PHP code into your documents by using the ''%%%%` or `%%<php>%%'' tags. (Use uppercase tags if you need to enclose block level elements.)

HTML example:

```

This is some <span style="color:red;font-size:150%;">inline HTML</span>

<HTML>
<p style="border:2px dashed red;">And this is some block HTML</p>
</HTML>
```


This is some <span style="color:red;font-size:150%;">inline HTML</span>

<HTML>
<p style="border:2px dashed red;">And this is some block HTML</p>
</HTML>

PHP example:

```
<php>
echo 'The PHP version: ';
echo phpversion();
echo ' (generated inline HTML)';
</php>
<PHP>
echo '<table class="inline"><tr><td>The same, but inside a block level element:</td>';
echo '<td>'.phpversion().'</td>';
echo '</tr></table>';
</PHP>
```

<php>
echo 'The PHP version: ';
echo phpversion();
echo ' (inline HTML)';
</php>
<PHP>
echo '<table class="inline"><tr><td>The same, but inside a block level element:</td>';
echo '<td>'.phpversion().'</td>';
echo '</tr></table>';
</PHP>

**Please Note**: HTML and PHP embedding is disabled by default in the configuration. If disabled, the code is displayed instead of executed.

## RSS/ATOM Feed Aggregation 
[DokuWiki](<img style######'' src'/img/< relref "DokuWiki.md" >'>) can integrate data from external XML feeds. For parsing the XML feeds, [SimplePie](http://simplepie.org/) is used. All formats understood by SimplePie can be used in DokuWiki as well. You can influence the rendering by multiple additional space separated parameters:

^ Parameter  ^ Description ^
| any number | will be used as maximum number items to show, defaults to 8 |
| reverse    | display the last items in the feed first |
| author     | show item authors names |
| date       | show item dates |
| description| show the item description. If <img style######'' src'/img/< doku "config/htmlok|HTML" >'> is disabled all tags will be stripped |
| nosort     | do not sort the items in the feed |
| *n*[dhm] | refresh period, where d######days, hhours, m######minutes. (e.g. 12h  12 hours). |

The refresh period defaults to 4 hours. Any value below 10 minutes will be treated as 10 minutes. [wiki/DokuWiki](<img style######` src'/img/< relref "wiki/DokuWiki.md" >'>) will generally try to supply a cached version of a page, obviously this is inappropriate when the page contains dynamic external content. The parameter tells [wiki/DokuWiki](<img style######` src'/img/< relref "wiki/DokuWiki.md" >'>) to re-render the page if it is more than *refresh period* since the page was last rendered.

By default the feed will be sorted by date, newest items first. You can sort it by oldest first using the `reverse` parameter, or display the feed as is with `nosort`.

**Example:**

  <img style######'float: right;' src'/img/rss>http///slashdot.org/index.rss 5 author date 1h'>

<img style######'float: right;' src'/img/rss>http///slashdot.org/index.rss 5 author date 1h'>


## Control Macros 

Some syntax influences how DokuWiki renders a page without creating any output it self. The following control macros are availble:

^ Macro           ^ Description |
| %%~~NOTOC~~%%   | If this macro is found on the page, no table of contents will be created |
| %%~~NOCACHE~~%% | DokuWiki caches all output by default. Sometimes this might not be wanted (eg. when the %%<php>%% syntax above is used), adding this macro will force DokuWiki to rerender a page on every call |

## Syntax Plugins 

DokuWiki's syntax can be extended by <img style######'' src'/img/< doku "plugins|Plugins" >'>. How the installed plugins are used is described on their appropriate description pages. The following syntax plugins are available in this particular DokuWiki installation:

~~INFO:syntaxplugins~~
