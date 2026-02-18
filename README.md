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
<p>If you'd like to watch the full jam process, <a href="https://www.youtube.com/playlist?list=PLB3nBZNJyn2FahdGnqH3H5Tym2FhZFRJo">I streamed and recorded the whole thing!</a></p>

<h4><i>About the Jam</i></h4>
<p>&emsp;Godot Wild Jam #73's main theme was "Tower". We were required to implement this theme and were given three optional themes or design elements to choose from called Wildcards. I ended up including "Warp Speed"; "Include a teleportation and/or fast travel mechanic". We were given nine days to design, develop, test, and publish our game.</p>

<h4><i>Game Design Overview</i></h4>
<p>&emsp;I had always wanted to try developing a platformer. My first experiences with video games mostly revolved around them and I still enjoy them today. At the time the jam was going on, Jump King was popular. That inspired me to try a vertical platformer that would hinge on gauging the amount of jump power used. Unlike Jump King, I did want to give the player a little more freedom with the ability to control their horizontal position while they are jumping.</p>
<p>&emsp;Once the genre and mechanic had been decided, I wanted to determine who the player character was and what the tower looked like. My mind leaned toward classic medieval-castle towers initially and eventually wandered toward the visual of a tower buried in the ground, with only the top exposed. Though exposed, it would be overgrown and dilapidated to the point that it was difficult to tell it was a tower, not just a hill with a hole and some rubbish around it. Though, this isn't the idea I stuck with in the end.</p>
<p>&emsp;I was toying with the idea of the jump height maximum being much higher than expected. It would make for a challenge in level design, would provide a higher range for the players to experiment with, and would allow the tower to be taller without necessarily needing more platforms. This led me to the idea that the player character could be a grasshopper. With their strong back legs, they would be able to jump quite high and it could easily make natural sense to the player since most people probably have seen a grasshopper and know how they jump. This idea actually gave me a different style for the tower that I added after the jam was over. It also would have allowed me the option to attempt another of the wildcards, which involved making fun facts appear in the game. I decided to scrap that part due to time, though.</p>

<h4><i>Programming and Development</i></h4>
<p>&emsp;I knew at the start of this jam that I wanted to attempt a build that could run in-browser, unlike Soul Salvage. It was necessary to become familiar with GDScript, Godot's own language, in order to achieve this.</p>
