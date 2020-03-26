# witcher 2 quest

## Creating dialogue

<ol>
  <li>Create resource **Scene script**.</li>
<li>Open it.</li>
<li>Input is teh start and Output is the end of dialogue.</li>
  <li>Add <b>Section</b> which is like a chapter of dialogue (or sth like a scene in a script).</li>
<li>Name the section.</li>
<li>Find the entity template of character (not player) you want to be in a dialogue, go to tab Voicetags and make sure that his <b>Voicetag</b> is the one left from the appearance.</li>
  <li>Go back to <b>Scene script</b> and in tab <b>Actors definitions</b> we have to link out NPCs to the dialogue (Geralt will be added automatically):</li>
  <ul>
    &emsp;<li>give NPC <b>Actor tag</b> which comes from tag from Appearance in its Entity template</li>
    &emsp;<li>as <b>Actor template</b> add Entity template from folder</li>
    &emsp;<li>finally add <b>Voicetag</b> of NPC</li>
  </ul>
  <li>Write scene in <b>Scene script</b> tab, connect sections in diagram tree and name every Output.</li>
  <li>Creating choice in dialogue:</li>
- TODO
  <li><b>Dialogset settings</b> shows who stands where. Different slot means different positions. <b>Is Pivot</b> means that the dialogue takes place where this person stands. Add voicetags of NPCs, Slot Number and Is Pivot (if necessary).</li>
  <li>Close and open the dialogue again for changes to work.</li>
  <li>Click <b>View -> Director's layout</b> and then <b>Debug</b>.</li>
  <li>Manipulating the camera and animations:</li>
- TODO
  <li>Now link the scene to the quest:</li>
 <ul>
   <li>open quest file</li>
   <li>add <b>Scenes -> Interaction dialog</b></li>
   <li>in scene add file of scene by clicking green arrow</li>
   <li><b>actorTags</b> is indicating which NPS you have to click to acivate the dialogue</li>
  </ul>
</ol>  
