Smith et al - launchpad rhythm pcg
2d platformer level design
small segments called rhythm groups
generated using a 2 tiered, grammar-based approach
rated by set of design heuristics

generation controlled by:
level pacing
geometry
minimises amount of content manual authored

launchpad
autonomous, designer-guided level generator
uses base components commonly found in 2D platformers
produces impressive variety of levels
guaranteed to be playable
based on model of rhythmic player movement
designed for dexterity-based challenges
derived from analysing existing games in genre
allows designer to refine generative space by manipulating parameters
clear and intuitive impact on generated levels
parameters dictate general path
the types of frequencies of geometry components
how collectible items are distributed throughout level
adjusting these parameters dramatically alters generated level
acts of implied model of ideal player “speedrun” behaviour
player strives to move at maximum speed

dexterity based challenges
based on rhythm and timing
launchpad understands this theory
movement aid in launchpad is a spring
simplify the problem
focus on generating rhythm groups to build single-cell levels
can create flat or sloped platforms
and can move horizontal or vertical paths
enemies that can be killed
enemies that can be avoided
gaps in platforms
coins positioned to guide players along jumps
coins used as decoration along long platforms

future work
researching methods of incorporating triggers
secret areas
multiple paths into grammar-based level generator

Launchpad tiers
first tier is a rhythm generator
first stage creates a set of beats
corresponds to player action
second tier creates geometry based on rhythm
second stage uses a grammar to realise set of actions
corresponds geometry according to set of physical constraints
end results is a set of rhythm groups
separation of tiers ensure intended rhythm is present regardless of geometric representation
feel of game and intended rhythm is shown and controlled
rhythm groups fit together side by side
bridging them with small safe platforms
levels are tested against a set of design heuristics
best level is selected
level is modified by a global pass
adds collectible items according to rhythm and geometry
Rhythm
type, length, density
two actions: move, jump
end time when player lets go of button
different hold times affect the height of avatar’s jump
Physics constraints
avatar’s capabilities and different types of jumps available
avatar size
maximum movement speed
initial jump velocity
height avatar can jump for short, medium, long jump hold
in-air time for each jump type
relative height different for two platforms on either side of jump
velocity of avatar when spring is used
model is ballistics based
extended to allow variable jump heights due to different amounts of time button is held
analysis of launchpad
techniques for visualising the expressive range of launchpad
applying external heuristics
clustering generated content to explore generated space






Essay Draft http://escholarship.org/uc/item/0fn558gq#page-30
http://sokath.com/main/files/1/smith-launchpad-tciaig.pdf
http://pcg.fdg2015.org/accepted.php


Smith et al [citation] propose a method for procedural content generation, for 2D platformer level design. Their objective is for creating an autonomous, designer-guided level generator with the use a two tiered, grammar-based approach. The generator that is explored and explained is Launchpad, a rhythm based level generator. Their goal is to create an “impressive variety of levels” which are “guaranteed to be playable”. A problem with some PCG games is that, while impressive in their generation, they are not functional as a level due to improper placement of objects, i.e. the exit is placed out of reach of the player.

One way that Launchpad creates a playable game is through the use of bridging two rhythm sets with a safe platform for the player to use. By giving the player a safe platform between generated areas, it creates a point of stabilisation to allow the player to realign their movements to the next stage.

In order to create an guaranteed playable level, they have “clear and intuitive” results based on designer refined generative space through manipulating parameters such as frequency of geometry components; collectible distribution throughout level, and dictating general path. Therefore, giving designers a responsive translation of their input by creating a level that matches their requirements.

Launchpad is designed for dexterity based challenges that would often rely on rhythm and timing. The implied model of an ideal player for a platformer is “speedrun” behaviour which suggests that the player should strive to move at maximum speed, and aiming to complete the level in the quickest time and shortest path. This model also influences player direction through the placement of coins, rewarding and reinforcing player movement towards a certain direction. For example, leading a line of coins in a vertical drop would suggest to the player to follow this direction. Another way in which coins have been used to enhance level design is to be used as decoration to fill long platforms and continue player engagement.

Other simplifications to Launchpad’s PCG approach is through creating enemies that can be killed (i.e.mobs) or avoided (i.e. spikes), gaps in platforms, sloped or flat platforms, along with moving horizontal or vertical paths.

Launchpad is based around the player input of rhythm, which includes: type, length and density. The two main player actions recorded are movement and jump, with recognition of when the player lets go of the button. The difference of hold time affects the height of the avatar’s jump, which a short hold is a short jump and long hold results in a long jump. This means for creating a game with varied platform gaps should be affected by the length of jump hold time.

A limitation of the simplification of Launchpad is through its focus on generation built into single-cell levels. While games such as Sonic [citation] use multiple-cell levels and portals, Launchpad is currently only capable of creating a single path which the player must follow.

Polymorph: A Model for Dynamic Level Generation

Jennings-Teats et al - Polymorph dynamic level generation
based on players skill and accessed difficulty of game
Dynamic Difficulty Adjustment (DDA)
aims for “continually-appropriate challenge”
unique player experience “personalised and structural”
“avoid difficulty-related player frustration and boredom”
multi-layer perceptron from play traces
traces collected with a web-based tool
asks users to complete multiple short level segments
about 10 seconds
rate them by difficulty
1 - Easy, 6 - Hard
first level is ignored due to learning game, multiple levels considered
then model selects appropriate level segment for player’s performance
variation of Smith et al. (2009)
level segments are generated by adaption of Smith et al (2009)
Polymorph
consists of data collection tool, a level generator, a game engine
and a learned model of level difficulty
Data collection
only short segments are used to isolate the difficulty variable
ideal granularity for cust, player performance-based, generated level chunks
each time they pass a segment or die
another segment of the same length is generated and places
top extend the level
potential fallback is that inexperienced players 
might spend the first level segment learning to play
so the first level is discarded
data collection tool and polymorph game proper
is Flash-based
is easily distributed and used through web-browsers
by many simultaneous players
By using this tool
data collected from 211 unique players
completing 2258 level segment playthroughs
data collection is ongoing
Learning features
first statistical model learned is ranking level segments according to difficulty
difficulty in 2D platformers is related to a combination of adjacent components
not just one component, i.e a gap followed by an enemy not just the gap
records both particular level components and occurrences of two-component










Jennings-Teats et al [citation] discuss the use of Polymorph dynamic level generation which is based on player skill and access difficulty of the game. Using Dynamic Difficulty Adjustment (DDA), the program aims to produce “continually-appropriate challenge” for it’s players. Platform games can have players who find their game too easy or sometimes too hard, with each player differing in their opinion. To “avoid difficulty-related player frustrated and boredom”, Polymorph uses difficulty measure as a way to create a unique player experience.

The database of data collection uses multi-layer perceptron from play traces collected with a web-based tool. It asks users to complete multiple short level segments of about 10 seconds then asks them to rate the level by difficulty; 1-easy and 6-hard. This allows developers to see how hard the game is perceived by the user and where it ranges in terms of difficulty. To compensate for players learning the game mechanics in the first level, this first measure is discarded. The model then selects an appropriate level segment based on the player’s performance and rating.

Polymorph consists of a data collection tool, a level generator, a game engine and a learned model of level difficulty. The reason for the short data collection segments is to isolate the difficulty variable; i.e. a gap followed by an enemy. This means that not only does particular level components are assessed by difficulty but also adjacent components. An advantage of this data collection tool is that it and the polymorph game is Flash-based meaning it is easily distributed and used through web-browser with simultaneous players. By using this tool, data has been collected from 211 unique players completing 2258 level segments with data collection ongoing.
