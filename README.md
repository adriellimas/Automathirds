# Automathirds
![Automathirds](https://user-images.githubusercontent.com/107147039/172746741-d9d99289-534e-4fd0-af6f-fd2b87bae167.PNG)

Automathirds is a generative music performance interface that uses a grid operating on Life-like cellular automaton rulesets to trigger different pitches. The conditions for cells to be born, survive, or die are iterations of the original “life” ruleset devised by British mathematician John Conway in 1970. This interface was created by Adriel Limas on Max MSP for the Spring 2022 RTVF 376: Digital Music Instrument Design Class at Northwestern University.
# Inspiration
![Gospers_glider_gun](https://user-images.githubusercontent.com/107147039/172748930-f69dd894-02bd-47e5-b06c-12c4cee69c7f.gif)

Sonifying cellular automata is hardly an original idea. There are countless interpretations of what sonifying a cellular automata would look like. So now that we’ve established that this isn’t entirely original, what original things can I do with my interpretation?

![Selected_Ambient_Works_Volume_II_cover](https://user-images.githubusercontent.com/107147039/172748780-911a0e9e-49e6-45c7-bc57-c9773ecd2f2e.jpg)

I listen to ambient music occasionally: Aphex Twin, Autechre, etc. Being particularly inspired by some of the compositions on Aphex Twin’s Selected Ambient Works Volume II, I thought the evolving visuals of a cellular automaton could be perfectly paired with similar ambient music. So I've decided that I want my interface to play chords and on using the x and y axis of the grid to map out different pitches. Next, I wanted to be able to play all the notes of a diatonic scale. Because most constructs in Life and related automata are composed of adjacent live cells, I anticipate that if I map out the diatonic scale to the X axis I would be met with a lot of major and minor 2nds. So Instead of mapping out a diatonic scale to the cells, how about space them in 3rds since that’s how extended chords are built? So the X axis is mapped in thirds, hence the name. For the Y axis I decided on mapping out the overtones series onto it in the spirit of additive synthesis. Each cell thus has a unique pitch assigned to them. The root note of the chord lies in cell 1,1 and can be determined using the keyboard interface. Each individual cell has its own sine wave oscillator and its on/off status act as envelope triggers.  

# Interface
Interaction with the automaton is as simple as clicking on any point in the grid to give it life. Like most interfaces you see online of these automata, you could also click on a cell at any point whether it’s progressing through generations or being paused. Additionally, holding the left mouse button or holding shift and the left mouse button while dragging across the grid allows you to awaken or kill multiple cells respectively. You could essentially draw or erase on the grid. So rather than being a zero player game where you select which cells to give life to, hit play and watch, the user interface facilitates a sort of collaboration with the automaton. 

Why a cellular automaton? Personally it’s very mesmerizing to watch. To see how a grid reacts to your input is very satisfying to me. Drawing constructs and seeing them evolve is very fun. It’s almost like playing god as you give life as you please and see your world evolve. Since the visual aspect is a large part of the instrument, I decided to spend time making the GUI satisfying to use and watch. The envelope of oscillators are also visually represented by the LEDs. The knobs and master volume indicates when it is being clicked on and changed.

# Future Versions
In the future, I would like to figure out how to make chord changes more smooth and less abrupt, and implement a rhythmic element to the updates where you can specify the rhythm of the updates in a 16 step sequencer style interface. I would also like to try either implementing the option to toggle toroidal boundaries so that gliders could move infinitely. I have previously set up a 16x16 grid but it seems like my brute force Max programming was a little too much for the cpu to effectively handle and display. I would love to optimize the patch and maybe find a less brute force method of handling the automata.

# Demo
https://youtu.be/4eQsvT5IpQc
