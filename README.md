<h1>Column Clamber</h1>

<table>
	<tr>
		<td><img src="Images/MainScreen.png" alt="Screenshot of initial game window" height=640 width=360/></td>
		<td><img src="Images/MidJump.png" alt="Screenshot of player mid-jump" height=640 width=360/></td>
		<td><img src="Images/Portals.png" alt="Screenshot of some portals" height=640 width=360/></td>
	</tr>
</table>
<p align="center">A game-jam game made for Godot Wild Jam #73</p>

<h3>Summary</h3>
<p>&emsp;A small grasshopper has accidentally fallen into an old, buried tower. It looks like a hard climb back to the top. But with careful control and a good sense of jump power, you'll make it out into the light once again.</p>

<h3>Where To Play?</h3>
<p>You can play this game directly in your browser either via the <a href=https://doctorsquawk.itch.io/column-clamber>itch.io page</a> or here on <a href=https://jbevell.github.io/Column-Clamber/>github pages</a>.</p>

<h3>Gameplay Controls</h3>
<p>This game only support keyboard controls:</p>
<ul>
	<li>Move with A and D or Left and Right Arrow Keys</li>
    <li>Hold Spacebar to charge jump. Release to jump.</li>
</ul>

<h3>Development Notes</h3>
<p>If you'd like to watch the full jam process, <a href="https://www.youtube.com/playlist?list=PLB3nBZNJyn2FahdGnqH3H5Tym2FhZFRJo">I streamed and recorded the whole thing</a>!</p>

<h4><i>About the Jam</i></h4>
<p>&emsp;Godot Wild Jam #73's main theme was "Tower". We were required to implement this theme and were given three optional themes or design elements to choose from called Wildcards. I ended up including "Warp Speed"; "Include a teleportation and/or fast travel mechanic". We were given nine days to design, develop, test, and publish our game.</p>

<h4><i>Game Design Overview</i></h4>
<p>&emsp;I had always wanted to try developing a platformer. My first experiences with video games mostly revolved around them and I still enjoy them today. At the time the jam was going on, Jump King was popular. That inspired me to try a vertical platformer that would hinge on gauging the amount of jump power used. Unlike Jump King, I did want to give the player a little more freedom with the ability to control their horizontal position while they are jumping.</p>
<p>&emsp;Once the genre and mechanic had been decided, I wanted to determine who the player character was and what the tower looked like. My mind leaned toward classic medieval-castle towers, initially, and eventually wandered toward the visual of a tower buried in the ground, with only the top exposed. What was exposed would be overgrown and dilapidated to the point that it was difficult to tell it was a tower, not just a hill with a hole and some rubbish around it. Though, this isn't the idea I stuck with in the end due to character design. And I still really liked the initial tower idea, so I may use it for something later.</p>
<p>&emsp;I was toying with the idea of the jump height maximum being much higher than expected. It would make for a challenge in level design, would provide a higher range for the players to experiment with, and would allow the tower to be taller without necessarily needing more platforms. This led me to the idea that the player character could be a grasshopper. With their strong back legs, they would be able to jump quite high and it could easily make natural sense to the player since most people probably have seen a grasshopper and know how they jump. This idea is what gave me a different style for the tower that I added after the jam was over. It also would have allowed me the option to attempt another of the wildcards, which involved making fun facts appear in the game. Due to time, I decided to scrap that part, though.</p>

<h4><i>Programming and Development</i></h4>
<p>&emsp;When first approaching this jam, I originally wanted to complete it in the MonoScript version of Godot, using C# like in Soul Salvage. However, I ended up starting the jam a little later than I wanted and ran into some problems getting it working properly. Thus, I found myself on the way to using GDScript. I had been curious about programming a game that could run directly in the browser, which I would need to use GDScript to do. I wasn't expecting to do it so soon but I figured I could work with the language much more quickly. So, swallowing my pride and worry, it was time to put my pattern matching skills to use. I created some quick, rectangular platforms, used a template that Godot offers to get some basic movement handled, and began modifying. This is also around the time I learned about Godot's tile maps and switched to experimenting with them instead of making new nodes for each boundary edge. With the basics done, I charged into getting the portals completed. Overall, the prototyping phase went pretty quickly for using a brand new language.</p>
<p>&emsp;The portals were the first fully implemented mechanic in the game. I separated the entrance and the exit and simply gave the entrance a reference to the exit's location. This way, I could place them where I wanted in the scene and the entrance would automatically know where to send the player without much leg-work. The exit doesn't even have any scripts attached; it's just a position marker. This setup also allows me to connect one exit to multiple entrances, opening up some more flexible level design options.</p>
<p>&emsp;Basic jumping was already implemented with the template that I used. After some experimentation, I settled on a system that used a jump velocity value to affect the jump depending on how long the player held down the spacebar. This value would build over the course of the _process function, which updates every frame, and gets applied on the next available physics frame when the jump key is released. The character also has various states that I keep track of, most notably a difference in states of "falling" vs "bonked". That separation allows the game to determine if control should be taken away from the player while they are falling. It only gets triggered if a ceiling collides with the player's character while they are in the "jumping" state. I think the bonked state adds an extra layer of difficulty and compliments the charged jump as a feature. Now players must choose how much they charge the jump in order to avoid losing control of their character. Losing control could mean being sent back down to the bottom of the tower.</p>
