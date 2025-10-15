# Automathirds
![Automathirds](https://user-images.githubusercontent.com/107147039/172756920-deb1503e-8d45-45aa-bf2a-8e506b3b2673.PNG)

Automathirds is a grid-based generative music performance interface running Life-like cellular automaton rulesets to trigger different pitches. The birth and survival conditions for cells are based on iterations of the original “life” ruleset created by British mathematician John Conway in 1970. Automathirds was created by Adriel Limas on Max MSP for the Spring 2022 RTVF 376: Digital Music Instrument Design Class at Northwestern University.
# Inspiration
![Gospers_glider_gun](https://user-images.githubusercontent.com/107147039/172748930-f69dd894-02bd-47e5-b06c-12c4cee69c7f.gif)

Sonifying cellular automata is hardly an original idea. There are countless interpretations of sonified a cellular automata. That being said, what are some original things I can do with my interpretation?

![Selected_Ambient_Works_Volume_II_cover](https://user-images.githubusercontent.com/107147039/172748780-911a0e9e-49e6-45c7-bc57-c9773ecd2f2e.jpg)

Inspired by some of the compositions on Aphex Twin’s Selected Ambient Works Volume II, I sought to pair the visuals of an evolving cellular automaton with similar ambient music. I've decided on an interface to play chords, using the x and y axis of the grid to map out different pitches. Next, I wanted to be able to play all the notes of a diatonic scale. Because most constructs in Life and related automata are composed of adjacent live cells, I anticipate that if I map out the diatonic scale to the X axis I would be met with a lot of major and minor 2nds. So Instead of mapping out a diatonic scale to the cells, I've spaced the pitches in thirds on the X axis since that’s how extended chords are built, hence the name. As for the Y axis, I chose to map out the overtones series onto it in the spirit of additive synthesis. Each cell thus has a unique pitch assigned to them. The root note of the chord lies in cell 1,1 and can be determined using the keyboard interface. Each individual cell has its own sine wave oscillator and its on/off status act as envelope triggers.  

# Interface
Interaction with the automaton is as simple as clicking on any point in the grid to give it life. Like most Life interfaces available online, you could also click on a cell as it’s progressing through generations without having to pause. Holding the left mouse button or holding shift and the left mouse button while dragging across the grid allows you to awaken or kill multiple cells respectively. You could essentially draw or erase on the grid. So rather than being a zero player game where you select which cells to give life to, hit play and watch, the user interface facilitates a sort of collaboration with the automaton. 

Why a cellular automaton? Personally it’s mesmerizing to watch. To see how a grid reacts to your input is incredibly satisfying. Drawing constructs and seeing them evolve is very fun. It’s almost like playing God, giving life as you please and seeing your world evolve. Since the visual aspect is a large part of the instrument, I decided to spend time making the GUI satisfying to use and watch. The oscillators envelopes are visually represented by the LEDs. The knobs and master volume indicates when it is being clicked on and changed.

# Future Versions
In the future, I would like to figure out how to make chord changes smoother while running as well as implement a rhythmic step sequencer interface allowing you to specify the rhythm of the updates. I would also like to try either implementing the option to toggle toroidal boundaries so that gliders could move infinitely. I have previously set up a 16x16 grid but it seems like my unoptimized brute force programming was a little too much for the cpu to effectively display. I would love to optimize the patch and maybe find a less brute force method of handling the automaton.

# Demo
https://youtu.be/4eQsvT5IpQc
