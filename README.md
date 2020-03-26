# witcher 2 quest

## Creating dialogue

1. Create resource **Scene script**.
2. Open it.
3. Input is teh start and Output is the end of dialogue.
4. Add **section** which is like a chapter of dialogue (or sth like a scene in a script).
5. Name the section.
6. Find the entity template of character (not player) you want to be in a dialogue, go to tab Voicetags and make sure that his **Voicetag** is the one left from the appearance.
7. Go back to **Scene script** and in tab **Actors definitions** we have to link out NPCs to the dialogue (Geralt will be added automatically):
  - give NPC **Actor tag** which comes from tag from Appearance in its Entity template
  - as **Actor template** add Entity template from folder
  - finally add **Voicetag** of NPC
8. Write scene in **Scene script** tab, connect sections in diagram tree and name every Output.
9. Creating choice in dialogue:
- TODO
10. **Dialogset settings** shows who stands where. Different slot means different positions. **Is Pivot** means that the dialogue takes place where this person stands. Add voicetags of NPCs, Slot Number and Is Pivot (if necessary).
11. Close and open the dialogue again for changes to work.
12. Click **View -> Director's layout** and then **Debug**.
13. Manipulating the camera and animations:
- TODO
14. Now link the scene to the quest:
  - open quest file
- add **Scenes -> Interaction dialog**
- in scene add file of scene by clicking green arrow
- **actorTags** is indicating which NPS you have to click to acivate the dialogue
  
