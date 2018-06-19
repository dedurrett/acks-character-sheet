# acks-character-sheet
Roll20 Character Sheet made for Adventurer Conqueror King System

Sheet Design inspired by the [Lamentations of the Flame Princess sheet by Toni Ruiz](https://github.com/Roll20/roll20-character-sheets/tree/master/Lotfp).

Attack throws, saving throws, and movement rates are calculated automatically based on race, class, level and encumbrance entered on the sheet. Many, if not all of these can be adjusted via modifier fields that can be entered by the user. Common adventuring proficiency throws are included by default, and target numbers can be entered manually to include modifiers from race, additional proficiency, etc.

House Rules Included:
* Wisdom modifier applies to all Saving Throws, rather than just Saves vs Magic.
* Trained and Untrained Skills Throws are present and automatically calculated based on character level. [This progression was taken from here.](http://www.autarch.co/comment/9485#comment-9485)

Proficiency Throws whose outcome may affect player decisions can be entered in the GMRoll Actions section. This section functions by outputting a button for the GM to press, keeping the result hidden. This does not have to be used; these skills could be added in the regular Action section underneath.

Also included is a toggle to change the sheet over for monster statblocks. A monster statblock copied in the same format as the core rulebook will automatically be parsed, and the data can be quickly copied over to a small sheet which includes roll buttons for monster initiative, morale, saves and attacks. Entering the monsters full notation hit dice (eg. 1d8, or 3d8+3) in the attribute Mhitdice and using the [API script MonsterHitDice](https://wiki.roll20.net/Script:Monster_Hit_Dice) will enable automatic hitpoint rolling for tokens generated from the sheet.

Lastly, a roll template has been implemented and is used by the sheet roll buttons. A custom output can be created using the format:

&{template:acks_template} {{type=WWW}} {{name=XXX}} {{YY1=ZZ1}} {{YY2=ZZ2}} {{YY3=ZZ3}}... etc.

For example, one could macro this:

&{template:acks_template} {{type=GM Report}} {{name=Player Defense}} {{Player1=[[@{Player1|armorclass}]] AC}} {{Player2=[[@{Player2|armorclass}]] AC}}

![Custom Roll Template Output](https://raw.githubusercontent.com/dedurrett/acks-character-sheet/master/ACKS_rolltemplate.png)
