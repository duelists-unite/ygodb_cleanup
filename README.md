# ygodb_cleanup

To submit any string corrections, first tell us on discord, which cards you will be working on so we can split the work. This project will take a while, but once its complete, it will be the most accurate database. Submit a cdb with the number range you did. For example, I am doing the first 100 cards, so my cdb will be cards_1-100.cdb. This contains only the text table. You will also need to look at the corresponding script to understand what effect is being referenced.

As an example, open the c39015.lua. You will see (aux.Stringid(39015,0)). This refers to str1. The "0" here is the index, always add 1 to it to get the str field it references to. It is obvious here by looking at the script that this str1 refers to the Special Summon effect. This card is "Assault Sentinel".

"You can Tribute this card; Special Summon 1 monster from your hand or Deck that specifically lists "Assault Mode Activate" in its text, except "Assault Sentinel", also you cannot Special Summon monsters from the Extra Deck for the rest of this turn, except Synchro Monsters. You can target 1 face-up monster you control; reveal 1 Synchro Monster in your Extra Deck, and if you do, the targeted monster's Type and Attribute become the same as the revealed monster's, until the end of this turn. You can only use each effect of "Assault Sentinel" once per turn."

This is the card text. Hence, the first part of the effect states, "Special Summon 1 monster from your hand or Deck that specifically lists "Assault Mode Activate" in its text, ...".

The str1 field then should say, "Special Summon?". No need to write the rest.
