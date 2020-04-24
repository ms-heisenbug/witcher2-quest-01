# witcher 2 quest

## Creating new world

<ol>
  <li>File -> New World</li>
  <li>Tools -> Terrain tools -> Create/modify terrain</li>
  <li>Materials -> change lores terrain to tile 000x000 -> Asset browser -> Add material from asset browser</li>
  <li>Adding sky:</li>
  <ul>
    <li>In scene add new group and new laer</li>
    <li>Make sky layer active</li>
    <li>Find skybox in Asset browser</li>
    <li>Drag and drop skybox on world (but on platform, not on the black surronding!)</li>
  </ul>
  <lil>Adding areas:</li>
  <ul>
    <li>Create new gorup and layer</li>
    <li>Right click on world -> Close active tool</li>
    <li>Right click on world -> Graphics -> Add area environment</li>
  </ul>
  <li>Creating day/night cycle<li>
  <ul>
    <li>Tools -> World environment -> Fake daycycle -> Enable<li>
    <li>Unclick World environment and click it again</li>
    <li>New option popped up -> click AreaEnvvironment0</li>
  </ul>
</ol>

## Creating dialogue

<ol>
  <li>Create resource <b>Scene script</b>.</li>
<li>Open it.</li>
<li>Input is teh start and Output is the end of dialogue.</li>
  <li>Add <b>Section</b> which is like a chapter of dialogue (or sth like a scene in a script).</li>
<li>Name the section.</li>
<li>Find the entity template of character (not player) you want to be in a dialogue, go to tab Voicetags and make sure that his <b>Voicetag</b> is the one left from the appearance.</li>
  <li>Go back to <b>Scene script</b> and in tab <b>Actors definitions</b> we have to link out NPCs to the dialogue (Geralt will be added automatically):</li>
  <ul>
    <li>give NPC <b>Actor tag</b> which comes from tag from Appearance in its Entity template</li>
    <li>as <b>Actor template</b> add Entity template from folder</li>
    <li>finally add <b>Voicetag</b> of NPC</li>
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


## How to make an interactive object:
1) Copy entity template of an object you want Geralt to interact with (for example some book) and open the copy;
2) Right-click on the Components field (over the panel with Template properties, Body parts etc.) and choose [Create 'CInteractionComponent'];
3) Click on newly created Interaction Component and choose Node properties from the panel below;
4) There are many options to customize said Component, but for this to work you got to fill:
- name (eg. read_book, examine_body);
- friendlyName (eg. Read, Examine);
- actionName (choose from drop-down menu, eg. Use);
- change showHint, checkCameraVisibility and reportToScript flags to true;
5) Save entity template, drag it into your level and tag it;

How to use it:
1) Create a Pause (right-click -> Flow control -> Pause) in your Quest file;
2) Add [CQuestInteractionCondition] condition from the drop-down menu in Pause properties;
3) Fill in interactionName (as above, eg. read_book, examine_body) and ownerTags (with tag you used for entity dragged into level);
4) Now you need to connect Pause with the rest of your Quest flow and a script you want to trigger by interacting with object (like dialogue scene);
