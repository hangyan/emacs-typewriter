emacs-typewriter
================

Typewriter Sound Simulation,Works on MAC OSX.

This project is mainly based on
<http://www.bobnewell.net/writer-typewriter.el>,I only did a few
modifies to make it work on mac osx too.


## INSTALL ##
1. Just put the el file in your load path,and load it.
   
   `(load-file "/path/to/writer-typewriter.el")`

2. set the sound file paths.eg:

   `(defvar writer-keyclick-noise "~/Emacs/data/sound/typewriter-key-1.wav")`
   
    `(defvar writer-keyclick-noise "~/Emacs/data/sound/typewriter-key-1.wav")`

    `(defvar writer-keyclick-noise
    "~/Emacs/data/sound/typewriter-key-1.wav")`

    Some website will provide these kind of wavs,I download some from
    <http://www.soundjay.com/typewriter-sounds.html>(They don't allowd
    to link directly to individual audio files).

3. set play command

    On Mac OSX,you can use "alplay"
    
    `(defvar writer-play-command "afplay")`

4. enjoy it.

    `(writer-make-noise)`


## NOTE ##
Your other settings may change the command bound to *RET*,for example,I
have change it to *newline-and-indent*,if you use only *newline*,you
may need to replace *newline-and-indet* to *newline* in the file(at
the end).

The origin file use *or* to match different situatoins,I think it may
be not necessary it you are sure about your settings.Since This
function will be invoked every time you type a char,use only one judgment
statement may be more efficient.
    
   
