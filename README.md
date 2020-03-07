# ygodb_cleanup

To submit any string corrections, first tell us on discord, which cards you will be working on so we can split the work. This project will take a while, but once its complete, it will be the most accurate database. Submit a cdb with the number range you did. For example, I am doing the first 100 cards, so my cdb will be cards_1-100.cdb. This contains only the text table. You will also need to look at the corresponding script to understand what effect is being referenced.

As an example, open the c39015.lua. This is the first card listed in StrToFix.txt.

It says "1) 39015 has 3 strs and 2 auxes calls"

This means that the database has 3 string entries but the card script only references 2. 

You will see (aux.Stringid(39015,0)) as the first reference. This refers to str1. The "0" here is the index, always add 1 to it to get the str field it references to. It is obvious here by looking at the script that this str1 refers to the Special Summon effect. This card is "Assault Sentinel".

"You can Tribute this card; Special Summon 1 monster from your hand or Deck that specifically lists "Assault Mode Activate" in its text, except "Assault Sentinel", also you cannot Special Summon monsters from the Extra Deck for the rest of this turn, except Synchro Monsters. You can target 1 face-up monster you control; reveal 1 Synchro Monster in your Extra Deck, and if you do, the targeted monster's Type and Attribute become the same as the revealed monster's, until the end of this turn. You can only use each effect of "Assault Sentinel" once per turn."

This is the card text. Hence, the first part of the effect states, "Special Summon 1 monster from your hand or Deck that specifically lists "Assault Mode Activate" in its text, ...".

The str1 field then should say, "Special Summon?". No need to write the rest.

The next string reference is e2:SetDescription(aux.Stringid(39015,1)) which is the second part of this card's effect to target 1 monster and change its type and attribute to a synchro monster in your extra deck.

So it could read, "Target your monster to change its Type and Attribute." Try not to be too wordy. If adding detail is necessary, then do it. Otherwise, being vague is ok. Just imagine you are playing and you see this string, as a player you know which card this is referring to.
