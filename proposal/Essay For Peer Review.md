PCG: Review

[SW180283]

Smith et al [1] propose a method for procedural content generation, for 2D platformer level design. Their objective is for creating an autonomous, designer-guided level generator with the use a two tiered, grammar-based approach. The generator that is explored and explained is Launchpad, a rhythm based level generator. Their goal is to create an “impressive variety of levels” which are “guaranteed to be playable”. A problem with some PCG games is that, while impressive in their generation, they are not functional as a level due to improper placement of objects, i.e. the exit is placed out of reach of the player.

One way that Launchpad creates a playable game is through the use of bridging two rhythm sets with a safe platform for the player to use. By giving the player a safe platform between generated areas, it creates a point of stabilisation to allow the player to realign their movements to the next stage.

In order to create an guaranteed playable level, they have “clear and intuitive” results based on designer refined generative space through manipulating parameters such as frequency of geometry components; collectible distribution throughout level, and dictating general path. Therefore, giving designers a responsive translation of their input by creating a level that matches their requirements.

Launchpad is designed for dexterity based challenges that would often rely on rhythm and timing. The implied model of an ideal player for a platformer is “speedrun” behaviour which suggests that the player should strive to move at maximum speed, and aiming to complete the level in the quickest time and shortest path. This model also influences player direction through the placement of coins, rewarding and reinforcing player movement towards a certain direction. For example, leading a line of coins in a vertical drop would suggest to the player to follow this direction. Another way in which coins have been used to enhance level design is to be used as decoration to fill long platforms and continue player engagement.

Other simplifications to Launchpad’s PCG approach is through creating enemies that can be killed (i.e.mobs) or avoided (i.e. spikes), gaps in platforms, sloped or flat platforms, along with moving horizontal or vertical paths.

Launchpad is based around the player input of rhythm, which includes: type, length and density. The two main player actions recorded are movement and jump, with recognition of when the player lets go of the button. The difference of hold time affects the height of the avatar’s jump, which a short hold is a short jump and long hold results in a long jump. This means for creating a game with varied platform gaps should be affected by the length of jump hold time.

A limitation of the simplification of Launchpad is through its focus on generation built into single-cell levels. While games such as Sonic [citation] use multiple-cell levels and portals, Launchpad is currently only capable of creating a single path which the player must follow. 

Jennings-Teats et al [2] discuss the use of Polymorph dynamic level generation which is based on player skill and access difficulty of the game. Using Dynamic Difficulty Adjustment (DDA), the program aims to produce “continually-appropriate challenge” for it’s players. Platform games can have players who find their game too easy or sometimes too hard, with each player differing in their opinion. To “avoid difficulty-related player frustrated and boredom”, Polymorph uses difficulty measure as a way to create a unique player experience.

The database of data collection uses multi-layer perceptron from play traces collected with a web-based tool. It asks users to complete multiple short level segments of about 10 seconds then asks them to rate the level by difficulty; 1-easy and 6-hard. This allows developers to see how hard the game is perceived by the user and where it ranges in terms of difficulty. To compensate for players learning the game mechanics in the first level, this first measure is discarded. The model then selects an appropriate level segment based on the player’s performance and rating.

Polymorph consists of a data collection tool, a level generator, a game engine and a learned model of level difficulty. The reason for the short data collection segments is to isolate the difficulty variable; i.e. a gap followed by an enemy. This means that not only does particular level components are assessed by difficulty but also adjacent components. An advantage of this data collection tool is that it and the polymorph game is Flash-based meaning it is easily distributed and used through web-browser with simultaneous players. By using this tool, data has been collected from 211 unique players completing 2258 level segments with data collection ongoing.

Steve Dahlskog et al [3] builds on analysis of Super Mario Bros levels into three levels of abstraction; using micro-, meso-, macro-patterns. These micro-patterns are used as the building blocks for the game producing vertical slices of the level which are then building into meso-patterns.

As opposed to the grammar-based approach of Launchpad, Multi-level Level Generator uses a search-based approach. This allows developers to create and analysis the difficult uses of features of groups such as groups of enemies, gaps for the player to jump or valleys of varying levels meaning multiple paths can be explored with elevation given with the use of stairs.

The results have shown to generate levels that “replicated macro-patterns of selected input levels” suggesting that this approach can replicated the design style of an input level through automatic analysation.

The use of this technique has been demonstrated through the researcher's experience with extended pattern-based level generation for Super Mario Bros which built on the Mario AI Framework which was featured in the Mario AI Competition. This example of application for their content and style generation is evidence of its successful level creation.

Conclusion

While Launchpad is a good foundation for procedural content generation, it is in the starting phase of suitable application due to it’s single-cell level design. This is a disadvantage to any large scope 2D platformer as the creative flare of the project is limited due to a linear path creation. Polymorph has shown to be a very successful data collection generator, with it’s own game engine a learned model of level difficulty. It has proven diligent in its examination of difficulty perception through its understand that it’s not only single components that generate game difficulty but adjacent components that should be assessed. The level of data collected is substantial enough as it’s use of Flash has proven useful in it’s collection due to a wide web-based audience. However, the extensive experience and the featured use of AI Framework in the Mario AI Competition is a clear example of the successful content and style generation. The in depth knowledge of PCG patterns Steve Dahlskog et al and their three levels of abstraction shows the most advanced generator and flexibility in terms of designer guided level generation.

References

[1] Smith, Gillian, et al. "Launchpad: A rhythm-based level generator for 2-d platformers." Computational Intelligence and AI in Games, IEEE Transactions on 3.1 (2011): 1-16.

[2] Jennings-Teats, Martin, Gillian Smith, and Noah Wardrip-Fruin. "Polymorph: A model for dynamic level generation." Sixth Artificial Intelligence and Interactive Digital Entertainment Conference. 2010.

[3] Dahlskog, Steve, and Julian Togelius. "A multi-level level generator." Computational Intelligence and Games (CIG), 2014 IEEE Conference on. IEEE, 2014.
