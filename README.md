
# <h1 align="center">Nova-Dynamic-UI-Dialogue-System Documentation</h1>
<h2 align="center" dir="auto"><strong><code>Unity Engine System Package</code></strong></h2>

<h2 align="center" dir="auto"> Overview </h2>
<p dir="auto">This dialogue system was created with the purpose to help aid game developers and game designers produce quality dialogue and a functioning system that is easy to use and integrate into projects. <strong>You must please be sure to include my name in the credits if you intend to publish your projects with my system.</strong> This system is designed for dynamic and expressive storytelling dialogue. With that goal in mind there are several prefab assets that are styled in different ways to help give the dialogue a variety of styles when speech in game takes place.


This asset pack is helpful for beginners and seasoned developers and designers to get their ideas and concepts out of the brainstorming and storyboarding phase. With this system it will allow for easy transitions between being active and disabled and also introduce a creative and expressive feel to the dialogue of any project.</p>

<p>This asset package has in total <strong>6 prefab assets</strong>. All for a specific purpose and/or aesthetic design style. The different canvases allow for developers to create dynamic ui dialogue and implement animations to the profile image icons at specific points in the dialogue to help portray emotion.</p>

## <h2 align="center" dir="auto"> Asset Details </h2>

<h3 dir="auto"> Video Player Canvas </h3>
<p dir="auto">This is a canvas specifically meant for displaying .MP4 videos and animations. If projects are trying to have pre-recorded dialogue videos from any 3rd party software like adobe after effects, sony vegas, etc. The <code>Video Player</code> game object has an audio source that it takes from the Cutscene Canvas A root to allow the player to register audio.</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide:</h4>

![Video Player Canvas Guide](https://github.com/user-attachments/assets/bd46c274-3666-4cfb-a031-730ce0a5df3d)


<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>Video Player Canvas</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and navigate to <code>Video Player Canvas</code>.</li>
  <li>select the <code>Video Player</code>.</li>
  <li>Select and drag a <code>.MP4 file</code> into the <code>Video Player field</code> in the inspector <code>Video Player</code>.</li>
  <br>

  
</ol>
<p> In the Update method of the <code>Video Animation Controller Script</code> you will see a if statement with a empty block of code like this: <code>if (timer > limit) { /*Go to next scene*/}</code>. This is where you can add other functionalities for if you want to change scenes, etc.</p>

</div>
<hr></hr>

<h3 dir="auto"> Dialogue Canvas A </h3>
<p dir="auto">This is a canvas specifically meant for displaying dialogue between two characters showing a Single Character Dialogue Box UI at a time. It will disable one character dialogue ui and activate the other character taking in the sequence. Only one character will be shown at a time.
</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide Part 1: </h4>

![Dialogue Canvas A Guide (1)](https://github.com/user-attachments/assets/f1d282f7-ce93-4b84-bcff-f5a276a93e67)
  
<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>Dialogue Canvas A</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and select it to access the <code>Dialogue System</code> script.</li>
  <li>In order for the canvas to be activated it needs a gameObject to be assigned in the <code>Style Group</code> field. Select abd drag the <code>Dialoge Style A Group</code> into the field</li>
  <li>Assign the <code>Name Text</code> from the <code>Hierarchy</code> into the <code>Name Text</code> field in the <code>Inspector</code> so the names assigned can be viewed on screen</li>
  <li>Then assign names to the <code>name1</code> and <code>name2</code> variables in the <code>Inspector</code>, and drag the profile images into the fields. <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>, and <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>.</li>
  <li>The <code>TypingSpeed</code> is determined by the value given. The shorter the value the faster a character appears</li>
  <li>Then drag the <code>Dialogue Text</code> in the <code>Dialogue Text</code> field Then add your dialogue in the dialogue array.</li>
  <br>
</ol>

<h4 dir="auto"> Set Up Guide Part 2: </h4>

![Dialogue Canvas A Guide (2)](https://github.com/user-attachments/assets/d2fa7e11-67d6-4f17-a893-aa1c2a9d0124)
  
<ol align="left" dir="auto">
  <li><code>Character Swap Points</code> are the points in the dialogue where the images flip to show who is talking at the time. The points are dependent on the <code>Dialogue Array Element Number</code> in the <code>Inspector</code>.</li> 
  <li>Create a element and put the number/index where you want the profile images to flip. Then drag the <code>Next Button</code> from the <code>Hierarchy</code> into the <code>Next Button</code> field in the <code>Inspector</code>.</li>
  <br>
</ol>

<h4 dir="auto"> Set Up Guide Part 3: </h4>

![Dialogue Canvas A Guide (3)](https://github.com/user-attachments/assets/9f479c30-92bd-482d-a436-740d4903e092)

<ol align="left" dir="auto">
  <li>Drag the <code>Dialogue Canvas A</code> into the <code>Source</code> field to allow audio to play while the dialouge is active. You can add audio clips in the <code>clips</code> array.</li> 
  <li>Lastly the entry and exit animations have 3 types: Fade, Slide, and Pop. These are already pre made and mapped out in the <code>Dialogue Canvas A Animation Controller</code>.</li>
  <br>
</ol>
</div>

<hr></hr>

<h3 dir="auto"> Dialogue Canvas B </h3>
<p dir="auto">This is a canvas specifically meant for displaying dialogue between two characters showing only profile headshot images to represent the characters talking. The main difference is that with canvas c both Character images will be displayed at the same time on opposite ends sharing a dialogue box. Therefore there are no Charater Swap Points for this particular canvas. This also allows for more dynamic movement and animations to be applied to the profile images individually, and to better express emotion and impact.
</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide: </h4>

![Dialogue Canvas B Guide](https://github.com/user-attachments/assets/322515bd-b9c8-4e7b-8030-04fe9f51433a)
  
<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>Dialogue Canvas B</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and select it to access the <code>Dialogue System</code> script.</li>
  <li>In order for the canvas to be activated it needs a gameObject to be assigned in the <code>Style Group</code> field. Select abd drag the <code>Dialoge Style B Group</code> into the field</li>
  <li>Drag the <code>Person A Name Text</code> and the <code>Person B Name Text</code>from the <code>Hierarchy</code> into the <code>Name Text Array</code> field in the <code>Inspector</code> so the names assigned can be viewed on screen</li>
  <li>Then assign names to the <code>name1</code> and <code>name2</code> variables in the <code>Inspector</code>, and drag the profile images into the fields. <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>, and <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>.</li>
  <li>The <code>TypingSpeed</code> is determined by the value given. The shorter the value the faster a character appears</li>
  <li>Then drag the <code>Dialogue Text</code> in the <code>Dialogue Text</code> field Then add your dialogue in the dialogue array.</li>
  <li>Then drag the <code>Next Button</code> from the <code>Hierarchy</code> into the <code>Next Button</code> field in the <code>Inspector</code>.</li>
  <br>
</ol>

</div>

<hr></hr>

<h3 dir="auto"> Dialogue Canvas C </h3>
<p dir="auto">Canvas C is similar to Canvas B the only difference is that the headshot images are within the borders of the dialogue box. The names of the individual characters are also placed on the images. It will disable one character dialogue ui and activate the other character taking in the sequence. Only one character will be shown at a time.
</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide: </h4>

![Dialogue Canvas C Guide](https://github.com/user-attachments/assets/d7a31d2d-6798-44cf-a281-22ee41f4ff71)

<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>Dialogue Canvas C</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and select it to access the <code>Dialogue System</code> script.</li>
  <li>In order for the canvas to be activated it needs a gameObject to be assigned in the <code>Style Group</code> field. Select abd drag the <code>Dialoge Style B Group</code> into the field</li>
  <li>Drag the <code>Person A Name Text</code> and the <code>Person B Name Text</code>from the <code>Hierarchy</code> into the <code>Name Text Array</code> field in the <code>Inspector</code> so the names assigned can be viewed on screen</li>
  <li>Then assign names to the <code>name1</code> and <code>name2</code> variables in the <code>Inspector</code>, and drag the profile images into the fields. <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>, and <code>Person A Profile Image UI</code> goes in the <code>Profile Image 1</code>.</li>
  <li>The <code>TypingSpeed</code> is determined by the value given. The shorter the value the faster a character appears</li>
  <li>Then drag the <code>Dialogue Text</code> in the <code>Dialogue Text</code> field Then add your dialogue in the dialogue array.</li>
  <li><code>Character Swap Points</code> are the points in the dialogue where the images flip to show who is talking at the time. The points are dependent on the <code>Dialogue Array Element Number</code> in the <code>Inspector</code>.</li> 
  <li>Create a element and put the number/index where you want the profile images to flip. Then drag the <code>Next Button</code> from the <code>Hierarchy</code> into the <code>Next Button</code> field in the <code>Inspector</code>.</li>
  <br>
</ol>

</div>

<hr></hr>

<h3 dir="auto"> NPC Dialogue Canvas </h3>
<p dir="auto">This is an interactive canvas that is meant for npc interactions. This can be activated through triggers or specific conditions. The purpose of this canvas is to help deliver NPC speech to the player.</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide: </h4>

![NPC Dialogue Canvas](https://github.com/user-attachments/assets/6b2ef6e3-a46e-4375-9f74-c078b15692db)

<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>NPC Dialoge Canvas</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and select it to access the <code>NPC Dialogue Controller</code> script.</li>
  <li>In order for the canvas to work properly the proper values need to be assigned in the <code>Inspector</code>. Select and drag the gameObjects in the <code>NPC Dialogue Canvas</code> script into the field</li>
  <br>
</ol>

<h4 dir="auto"> Reference Image: </h4>
<p align="left" dir="auto">This is an image you can use as a reference to help get started in completing the set up, and then you can adjust the dialogue and settings how you see fit.</p>
<img width="635" height="504" alt="image" src="https://github.com/user-attachments/assets/31853bf0-0448-44c6-872b-432288ce18a8" />

</div>

<hr></hr>

<h3 dir="auto"> Item Dialogue Canvas </h3>
<p dir="auto">This is an interactive canvas that is meant for item interactions. This can be activated through triggers or specific conditions. The purpose of this canvas is to help deliver item details to the player.</p>

<div align="center">
  
<h4 dir="auto"> Set Up Guide: </h4>

![Item Dialogue Canvas Demo](https://github.com/user-attachments/assets/c1966471-2733-4147-98ba-cd849d66c0e1)

<ol align="left" dir="auto">
  <li>Within the <code>Project Window Tab</code> navigate to the <code>Prefabs folder</code> and drag the <code>Item Dialoge Canvas</code> in the scene.</li> 
  <li>Then in the editor find that canvas in the <code>Hierarchy</code> and select it to access the <code>Item Dialogue Canvas</code> script.</li>
  <li>In order for the canvas to work properly the proper values need to be assigned in the <code>Inspector</code>. Select and drag the gameObjects in the <code>Item Dialogue Canvas</code> script into the field</li>
  <br>
</ol>

<h4 dir="auto"> Reference Image: </h4>
<p align="left" dir="auto">This is an image you can use as a reference to help get started in completing the set up, and then you can adjust the dialogue and settings how you see fit.</p>
<img width="631" height="497" alt="image" src="https://github.com/user-attachments/assets/759e4b9e-99d6-4fd1-bf7a-cf1824579394" />


</div>


## <h2 align="center" dir="auto"> Animation Controller Settings </h2>

<div align="center">
  
<h3 dir="auto"> How To Guide </h3>

![Animation Controller Guide](https://github.com/user-attachments/assets/fd258233-7244-46c1-a7f9-6985accd3d53)

<ul align="left" dir="auto">
  <li dir="auto">Access the <code>Animation Controller</code> of any of the prefab canvases by navigating to the <code>Canvas Animations</code> and then go to the <code>Dialogue Style Animations</code> folder. Within the animation controllers they all posses the same parameters. The parameter <code>Dialogue Line</code> represents the element number for the <code>Dialogue Array</code>. Use this to play an animation state at an exact point in the dialogue. Also each mouseclick when clicking to go to the next line of dialogue increases the dialogue index by 1 <code>dialogueArrayIndex++</code>. This is what the <code>Dialogue Line</code> represents, and when creating new animations be sure to use this to navigate between different points in the dialogue.</li>
<li dir="auto">All the parameters for <code>Fade</code>, <code>Slide</code>, and <code>Pop</code> are all used at the start or end of the animation. If you wish to make your own custom animations to add on to your projects then the Dialogue System has a couple of functions used to assist in that. For playing <code>sound </code>in the <code>dialogue system</code> there is a funtion calld <code>PlaySFX()</code> this is a function specifically made for the <code>animation event</code>, for those who want to add on more to there project. The function <code>ResetProfileImages()</code> is used to flip your image back to its original state before the animation. I placed these at the end of every <code>Exit Animation</code> type to help reset the animation back to the start.</li>
</ul>
 ##
<h2 align="center" dir="auto"> Contact Information 📞</h2> 
<p align="center" dir="auto">Contact me at <a href="mailto:lenardclarke22@gmail.com">lenardclarke22@gmail.com</a> or <a href="https://lsclarke.github.io/Portfolio-Website/index.html">My Portfolio</a> for any questions/inquiries.</p>
</div>

