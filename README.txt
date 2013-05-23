==README for Sketchfab BB code add-on for miniBB==
Release date: May 22, 2013.
Latest update: May 22, 2013.
miniBB version: 3.0+
Author: Pierre-Antoine Passet (pa@sketchfab.com), Sketchfab (support@sketchfab.com)

This plug-in adds possibility to embed Sketchfab 3D models in forum postings. Works like any regular BB code with the button provided. Click the button - enter the model URL video - post the message.

==INSTALLATION==

* Copy the button image img/button_sketchfab.gif under /img/ folder of your forum

* Modify the file bb_codes.php file adding the codes provided under bb_codes.encode.txt and bb_codes.decode.txt. The code under bb_codes.encode.txt should be pasted in the function enCodeBB before the line which says

$msg=preg_replace($pattern, $replacement, $msg);

The code under bb_codes.decode.txt should be pasted in the function deCodeBB before the aforementioned line.

* Open the main_post_form.html template and add the javascript/HTML code provided under main_post_form.code.txt; Copy the inside of the <script/> tag at the top of the file below the lines:

        var enterSubject='{$l_enterSubject}';
        var enterMessage='{$l_enterMessage}';
        var enterLogin='{$l_anonDisallowedClr}';

* Copy the button code after the other button codes, before the <!--/BBJSBUTTONS--> tag)


==USAGE==

Example of BB code:

- [sketchfab]bYsbh03AJqkeimQ5FMulr5i8yGo[/sketchfab] - will be converted to an embedded model

Where to get these URLs? On Sketchfab's website! sketchfab.com


==FINALLY==
Questions? Suggestions? Improvements? Email support@sketchfab.com
