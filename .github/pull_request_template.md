### Requirements

* Filling out this template is required. Pull Requests without a clear description may be closed at the maintainers' discretion.

### Description

<!--
When I tell the BlTouch from TFT 24 v1.1 in 12864 mode, it goes down - up and when I tell it up - down. since the touch screen works well, the positioning does well, and leveling the bed is also going well.
After analyzing and testing all the configurable Marlin options on the LCD and not getting results, I have gone to analyze the language file. In my case I use Spanish.
Indeed here I found the error. The translation is reversed.
You currently have this:
   PROGMEM Language_Str MSG_BLTOUCH_STOW = _UxGT ("Cmd: Bajar piston");
   PROGMEM Language_Str MSG_BLTOUCH_DEPLOY = _UxGT ("Cmd: Subir piston");
The correct one is this.
   PROGMEM Language_Str MSG_BLTOUCH_STOW = _UxGT ("Cmd: Subir piston");
   PROGMEM Language_Str MSG_BLTOUCH_DEPLOY = _UxGT ("Cmd: Bajar piston");
We must be able to understand your proposed change from this description. If we can't understand what the code will do from this description, the Pull Request may be closed at the maintainers' discretion. Keep in mind that the maintainer reviewing this PR may not be familiar with or have worked with the code recently, so please walk us through the concepts.

-->

### Benefits

<!-- What does this fix or improve? -->
The traslation
### Related Issues

<!-- Whether this fixes a bug or fulfills a feature request, please list any related Issues here. -->
