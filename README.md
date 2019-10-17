Quick Start

Buy in keys. Keys are the tokens that you need to play this game. You can exchange for them at 1 key = 1 CTXC at the second row on the right, paying directly from your Cortex wallet. Likewise, after each game, you can withdraw all your winnings back to your Cortex wallet at the third row on the right.
Pick either Red or Blue team (You will not be able to change your team again for this round).
Start drawing on the Canvas and help your team win the game. If you’re red, try to morph the digit into any of these: 0, 1, 2, 3, 4 and if you’re blue, try to morph the digit into any of these: 5, 6, 7, 8, 9.

It is strongly recommended that you carefully read the detailed game rules below to understand how to win and make $$$ in this game. This game is a blast once you can understand it, but note that this is not your average mindless game - be prepared to work your brain (you don’t need math background other than basic high school arithmetic)! Please leave a comment by opening an issue on our Github if any of the rules are unclear. 

Overview

At each round, you can pick a team, either red or blue. 

Your team will compete against the other by drawing/erasing pixels on the canvas in order to create a particular digit (from 0-9). At the end of each round, an AI algorithm will determine which digit the canvas has morphed into and the red team wins if it is 0, 1, 2, 3, 4 whereas the blue team wins if it looks like 5, 6, 7, 8, 9. Members of the winning team will divide the reward pool according to their stake ratio. 

Note that while there will be only one winning team for each round, you can still come away having earned money by choosing your strategy wisely. To see why this is, let’s take a deeper look at how exactly you play the game.

How do I draw/erase pixels?

The pixels on the canvas work sort of like real estate (except the buy and sell are automatic) or Fomo3d. 

At the beginning of each round, you can buy any untraded pixels at the price of 1 key per pixel. Once you purchase a pixel, you can do whatever you want with it: you can draw it black, grey, or white (effectively erasing it). Then, when someone purchases it from you, they will need to pay cost = current_price × 1.35 × f(d). You will get 10% of the price difference whereas the other 90% goes into the final reward pool. (Don’t worry about the f(d). Assume it is 1 unless the balance between red and blue is severely tilted. More details on this below).

For example, you are a member of the blue team, and you buy in a pixel at the price of 1 key. Later, someone from the red team wants to buy it from you (because he wants to erase your pixel to make the digit look more like a 4). He needs to pay a cost = 1 key × 1.35 × 1 = 1.35 keys. 

You will get a total of 1.035 keys as a result of “selling” the pixel. (The process is automatic so you cannot choose not to sell a pixel).

Why? Because the selling price (1.35 keys) is 0.35 keys higher than the buy price (1 key). And 10% of this profit (0.035 keys) goes directly to you, while the other 90% (0.315 keys) go into the final reward pool. So your 1.035 keys are a full refund (1 key), plus the 0.035 keys of the profit. 

Note that even if your team loses the game, you can still come away with a profit $$$ by buying strategic pixels which are later sold. 


How many pixels can I draw on the Canvas at a time?

No more than 15 at a time.

When does the game end? 

When the highest priced pixel reaches 100,000 keys, or the accumulated number of pixel transactions reaches 10,000, the Digital Clash's Contract freezes the Canvas and begins to settle. The winning team will divide the reward pool whereas members of the losing team will lose all their currently staked pixels. (The developer team will get 2%).

Why do I need to be careful when the two teams are unbalanced? 

To ensure fairness and prevent imbalances between the red and blue team (because having everyone joining the same team is no fun), we introduced a difficulty parameter f(d) into the cost calculation when buying pixels. Recall from above, the cost of buying a pixel is: cost = current_price × 1.35 × f(d)

As mentioned, you usually don’t need to worry about f(d), when the two teams are balanced. This is because f(d) is a function of stake ratio (see the graph below) and as long as one team’s stake ratio against the other is between 0.382 and 0.618, f(d) = 1. However, let’s say the blue team has all the pixels (a lot of imbalance!) on the canvas, so the stake ratio is 1 for the blue team. Now if you’re a blue team member, buying pixels become 1.5 times more expensive for you because f(d) = 1.5. Meanwhile, if you’re a red team member, you can buy the same pixel at half the price because f(d) = 0.5 for you. Therefore, if you’re on the dominant team when the stake ratio is unbalanced, you may risk losing money because people from the other team can buy your pixels at half the price by taking advantage of the f(d).

Side note (for those more mathematically inclined): f(d) + f(d’) = 2. This makes sense when you take another look at the graph with the example above. When the blue team has a stake ratio of 1, f(d) = 1.5 for the blue team; meanwhile, the red team has a stake ratio of 0, and f(d’) = 0.5 for the red team. 
