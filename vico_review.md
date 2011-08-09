Vico Review
===========

Vico is a text editor for Mac OS. Its signature features are its vi key bindings and its support for Textmate bundles. It has an attractive, Maclike interface, a project directory sidebar, a find-file search, and a find-symbol search.


Mac-style editing vs vi-style editing
-------------------------------------

First and foremost, Vico is a vi editor. That is, the primary way of interacting with and editing text is in Vico is via vi commands. vi is a text editor from the unix world which operates in two separate modes: text entry mode and command mode. This is different from (even anathema to) the Mac way, which eschews modes almost as a matter of principle. 

In a typical Mac text editor or word processor, you click where you want to insert text and start typing right away. You click and drag to select text, and you can issue commands by choosing a menu item or by pressing command-key shortcuts. It could be argued that there are modes (insertion, selection, etc.) but moving between them is fairly fluid and in line with the rest of the Mac's point, select, action interface.

vi works differently. It has two distinct modes: insertion mode and command mode. When you first launch vi, you are in command mode. The keys you press in this mode don't result in text being written out on the screen; they issue commands. One such command is 'i', which places vi in 'insert' mode, at which point you can start typing text normally. When you want to issue a command (such as move the text insertion point), you have to switch back to command mode by hitting the Escape ('esc') key. Once in command mode you can do things like move the insertion point ('h', 'l', to move left and right a letter; 'j' and 'k' to move up and down a line),  save changes, scroll through the document, copy lines of text ('yank' in vi parlance), and so on. Using vi effectively involves memorizing a handful of commands, some mnemonically named, others not. This represents a steep learning curve relative to the Mac way, but has payoffs on down the line for experienced users, who can combine vi's various commands to do quick movement and manipulation operations in a very small number of keystrokes. Because of this tradeoff between learning curve and experienced operation, vi is popular with programmers and other power-users who work with large amounts of text.

 

Editing in vico
---------------

Vico is a mesh between the two worlds. You start in vi command mode. Once you press 'i' for insert, the editor becomes more Maclike. That is, you can use arrow keys to advance the insertion point. You can combine arrow keys with the option key to move backwards and forwards a word, and command-arrow to move backwards and forwards one sentence or to the top or bottom of the document, just like most Mac text editors. Unlike most Mac text editors, you cannot combine these commands with the delete key. For example, in TextEdit, you can type option-delete to delete an entire word and command-delete to delete an entire sentence. When in Vico's insert mode, these Mac shortcuts do not work. It is possible to do the same operation in Vico's command mode, but the Mac-like way is not supported.

Other Maclike conventions are preserved somewhat. If you click somewhere in the document, Vico moves the insertion point there, although it places you in command mode at that point. If you click on a line number, to the left of a line, the entire line becomes highlighted (as in Microsoft Word). If you select text with the mouse and choose copy from the Edit menu or hit command-C, the block of text gets placed in the Mac clipboard. Vico will paste wherever you click the insertion point, but remain in command mode. Command-Z for undo and Shift-Command-Z for redo work as expected. Although for just about any command you issue, maclike or not, you end up in command mode. Given the overall vi-like approach to the editor, this is not altogether a bad thing.

There are other Maclike subtleties layered on top of Vico's vi interface. On particularly nice example is the split-pane view. In vi, you split the current document into panes by (starting from command mode) typing ":split" and hitting return. It was a command I used infrequently enough in standard vi that I would forget how to switch between panes. In Vico, there is a menu command for this in the View menu, and to switch between panes you can point and click in the pane you want to be editing in. When you are finished with a pane, you can click in it to select it, then type the standard Mac 'close window' command, Command-W, and the pane closes. It may sound silly to write this out, but it's what I expected of a Mac interface, so when I tried it the very first time and it worked, I immediately liked Vico. 

I don't work much with international text, but it's worth noting that Vico supports Unicode at least to the degree that I could copy some Japanese text from sony.co.jp and paste it into the editor and see nice-looking Kanji and Hiragana.

Vico's Menus
------------

Vico has a complement of menus and commands you would expect in a Mac text editor: File, Edit, Navigate, View, Window, and Help. Where vi would supply a command-mode equivalent, Vico shows the vi command in a gray box. Otherwise it shows the Mac command with the typical modifier key (Command, Control, Option or Shift) symbols plus keypress. Most text-specific commands must be issued in command mode (or if they are issued from a menu in insert mode, they switch you to commend mode, perform the action, and leave you in command mode). 

Window Tabs
-----------

Like Textmate and many other text editors, Vico allows you to keep multiple files open at once accessibe via tabs at the top of the window. There is not much to say about this feature; it works pretty much the way you might expect it to if you have used Textmate, UltraEdit (or Firefox, Safari, or Chrome). Opening an existing file from the File menu or starting a new file opens a new tab in the existing window. To move between tabs, you can hit Command-Option-arrow, or Command-Option-square-bracket. Open files are also selectable from an "Open files" menu at the top of the Vico window.  

Textmate Bundles
----------------

Vico supports the use of Texmate bundles. Textmate is a popular Mac OS text editor which is highly extensible via "bundles," collections of code which provide language syntax definitions and scripted commands and macros. Through bundles, the basic functionality of Texmate can be enhanced in innumerable useful ways. Vico comes preinstalled with a handful of Texmate bundles (C, Css, Diff, Java, Javascript, Json, Nu, Objective-C, Perl, PHP, Python, Ruby-On-Rails, Ruby, Shellscript, Source, Sql, Text, Xml and Yaml). It also includes a tab on the Preferences dialog box to install more bundles. 

Textmate changed a lot of rules for Mac text editors. Among them was the notion that commands and shortcuts needn't be initiated by some combination of command keys (Command-Shift-Control-Option). Instead, it had scripted expansions such that you could type 'doctype' and hit Tab, and it would auto-expand into something like this:

  `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`

These shortcuts are a great boon for power users who remember them. Even if the commands are not completely memorized, they are available in a pull-down menu and their shortcuts are apparent. Vico has the ability to use these bundles mostly the same as they are used inside Textmate.  

For example, I installed the Markdown bundle to use while editing this review. It includes Markdown syntax highlighting, as well as convenient shortcuts. If I type '-' on a blank line and hit the Tab key, a script in the bundle extends an 'underline' of dashes along the line above (a Markdown convention indicating a subheading). If I type Command-Control-Option-P, Vico shows a formatted preview of my document in a split pane. Bundle commands are also available from a menu in the bottom of the editor, so you don't have to memorize these commands (though if you work with one programming or markup language a lot it behooves you to do so). 

Go to File and Go to Symbol features
------------------------------------

As someone who used Texmate quite a bit previously, I was happy to see two highly-useful commands carried over: Go to File and Go to Symbol. 

When you open a folder rather than a file (commonly called opening a "project" -- you do so by choosing a folder from the File > Open command or pointing the vico command-line tool at a directory rather than a file) a search box at the top left of the Vico window allows you to search for any file found in the directory hierarchy in the left pane of the window. You can search by any combination of characters, even omitting some. This works in the same way as the Textmate tool, where if you search for "demol", it will find all of these files "**demol**ition.txt", "**demo**.xm**l**", and "**demo**.htm**l**". Matches appear in the left-hand sidebar and you can use the arrow keys to select the file you're after, and hit return to open it. 

Find symbol works the same way. If you are in a structured syntax file that Vico recognizes through one of the installed bundles, and you type something into the Go to Symbol box, you'll get a list of functions, class definitions, etc. that match the string you typed. The matches appear in a temporary right-hand pane and again are selectable via arrow keys. Return jumps to the symbol location in the file. If you have multiple files open in tabs, Go To Symbol also searches in those files, with your currently open file given preference at the top. This is a nice enhancement to Textmate's version, which only searches within the file you're looking.

Bugs/Annoyances
---------------

Vico was first released in May of 2011, and is presently at version 1.1. There are still many rough edges. None of these are completely detrimental to using Vico, but I've run into them enough that they are worth  mentioning:

* Syntax coloring is occasionally spotty. It seems there are times where the syntax parser for the given language hasn't completely slurped the file, and only portions are colored (and the Find Symbol command only finds symbols up to that point). Fixing this requires choosing a different syntax setting for the file and then re-choosing the original syntax.
* Up-arrow keys sometimes stop working in insert mode. I don't know why. Switching to command mode and then back makes them work again.
* Quasi-crashes. Vico will stop providing visual feedback for something like a Save operation, and you're left wondering if the last save command you issued worked. I.e. you still see a dot in the middle of the Close button and some other commands don't appear to work. This has happened when I have multiple windows open, so it could be that a reference to a window is being lost somehow. In the instances I've seen it happen, I've been able to spot-check the file on the command line, find that it has in fact been saved, and then Quit and restart Vico. 
* Real crashes. After editing for many minutes with several open tabs and unsaved files, I chose Hide File Explorer from the View menu. Spinning pizza of death, then Vico unexpectedly quit. 
* Vi syntax coloring mucks up quotes inside comments. A shortcoming not limited to vico, a single quote (i.e. an apostrophe) inside a commented block of text can throw off the syntax parser to the extent that entire blocks of code appear as quoted text, when they are in fact not.

Room For Improvement
--------------------

For me the number-one improvement for the editing environment would be for insert mode to fully support typical Mac conventions. Mostly that means I can Option- and Command-delete just as in other apps.  

Number two would be multi-file search (and replace). BBedit still rules the roost for multifile search among Mac text editors. Coda also has a nice Find in Files Command, and Textmate's works, at the very least. Vico doesn't even have the option. I sincerely hope that something is in the works in this regard for Vico. Right now when this becomes necessary (several times a day), I am either using a command line `find | xargs grep` command or switching into BBEdit. A dialog-box-based search and replace would also be a welcome addition.

As of version 1.1 you cannot pipe the output of command-line commands into Vico. e.g. `$ cat vico_review.md | vico` switches from Terminal to Vico, but Vico does not open an anonymous window with the result of the pipe, as BBEdit and TextMate do.

Textmate's block select/insert is one of its best features. It would be nice to see something like it in Vico, probably by supporting a vimlike column selection feature enhanced with point-and-click from the Mac side.

I would love to see Mac OS "Lion" full-screen support.

Vico is based on vi, not vim, the "enhanced" version of vi that ships with Mac OS and many other modern unix-y OSes. That means that several features you might associate with vi which are actually vim features, are not available, such as '(' and ')' to move to previous/next sentence, '{' and '}' to move to previous/next paragraph. It doesn't support multiple registers for yanks and deletes (the equivalent of multiple clipboards on the Mac). Plenty of other examples abound. It does have some vimlike features (e.g. multple undo) and support some Mac-equivalent movement commands in insert mode to make these shortcomings tolerable.

Conclusion
----------

Vico is an interesting beast. Upon launch it immediately feels like a Mac application, and in most respects is. This differentiates it in my mind from the most obvious app to compare it to, MacVim, because the latter feels like vim shoehorned into a Mac window. The author of Vico on the other hand has demonstrated some thoughtfulness to the interface, a respect for Mac conventions and a familiarity with the field of Mac text editors.


One of the problems with a modal, text-command interface like vi's is that when learning the editor, you inevitably find yourself "stuck," and pulling up a quick reference card. How do I select multiple lines of text? How do I undo? How do I redo? What Vico does is provide enough of a Mac interface on vi that you never really get stuck as long as you remember how to get in and out of insert mode. Knowing that vi has much more power than is exposed by a basic Mac text editor is a motivating factor too, so I've found myself becoming a more powerful vi/vim user, which has benefits beyond just my Mac.

I didn't have an overwhelmingly compelling reason to switch from TextMate other than I was tired of waiting for the author to fix the lame character-by-character Undo. Vico does that much right and more. Gaining split-window functionality is another immediate win over Textmate. It's worth noting that TextMate pulled me away from BBEdit for its themes, its bundles and its overall attractiveness. Vico has all of this.

I have been using Vico as my main text editor for almost three weeks now. I don't see myself moving back to Textmate (which was my main editor for the last 2 1/2 years). Before Textmate I used BBEdit for about thirteen or fourteen years, interspersed with flings with Alpha, Coda, NisusWriter (!), Xcode and MPW, performing the gamut of web development (markup, stylesheets, database, browser-side scripting, server-side programming). I've been using unixen throughout that time, so have been comfortable if not completely fluent with vi for a while.

Vico is probably right for you if you...

* want a vi or vim that is more Mac-like than MacVim or the command line, or
* want to learn a powerful, ubiquitous text editor but have some training wheels while you do it, or
* want a lightweight editor with some scriptability, pretty syntax coloring, and no lame undo, and aren't averse to shifting to a different text-editing paradigm.

Vico is probably wrong for you if you...

* must have integrated multi-file search, or
* must have a complete vim command set, or
* don't want to learn a different editing paradigm. 

Topics not Covered
------------------

* SFTP
* Nu scripting language


Resources
---------

* [Vi Reference Card](http://www.digilife.be/quickreferences/qrc/vi%20reference%20card.pdf)
* [vi and vim editors](http://oreilly.com/catalog/9780596529833)
* [Texmate](http://macromates.com)
* [BBEdit](http://barebones.com/bbedit)
* [Coda](http://panic.com/coda)

© 2011, David Kurtz
