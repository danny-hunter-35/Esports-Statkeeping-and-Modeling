# Esports-statkeeping-and-modeling

These two spreadsheets concern statistics and calculations associated with the video game **Rocket League**. 
As a formerly avid player, competiter, and fan of the game and associated Esport, I helped gather and display game statistics and individual accolades for a group of friends as well as develop methods for model projections of "fantasy" points for the pro scene.

## Pandamonium Team Stats
**Pandamonium Team Stats** was a spreadsheet that a friend and I used to compile statistics, such as goals per game, which would then be compared to other members in our server to see who was, on that same example, the best striker. Most notably, I was able to update the rankings for these accolades automatically by developing commands in excel/google sheets such as the following:
> =IF(IFNA(MATCH(INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)), $A$3:A3, 0), FALSE()), INDEX($A$18:$A$31, SMALL(IF($C$18:$C$31 = B4, ROW($C$18:$C$31) - MIN(ROW($C$18:$C$31)) + 1), (ROW(A4) -1) -MATCH(INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)), $A$3:A3, 0))), INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)))

In the *Server Accoloade Race* sheet of Pandamonium Team Stats, this command is in the cell *A4*. Essentially, the command searches the *GPG (Goals Per Game)* category on the same page (C18 through C31) and finds the 2nd highest number. From there, it finds the corresponding value in column A (the name of the player). Not only did we do this for "basic stats", but because of this quick automation, we went as far as having a leaderboard for boost collection stats too (see *Boost and Positioning Title Race*)

## Rlcs stats and projections
**Rlcs stats and projections** was during the pandemic when daily fantasy sports sites such as draftkings did not have much content in the way of real sports, and had to find a new market in esports. Figuring I could capatalize on those that did not have as much knowledge in the esport of pro Rocket League, I compiled data from a secret source into this spreadsheet and used some "basic" formulas to compute projections based on the given score system. Perhaps the most organized of these sheets is *EU Spring series projections* where you can see the teams, their players, the stats, projections, and the teams they are playing against. 
> =((10\*C3)+(5\*D3)+(5\*E3)+(F3\*3)+(G3/100))

This command in *H3* is a simple projection based off of the player's statistical averages and the given scoring system for the fantasy game.
> =((10\*((($C$2+M3)/2)\*(C3/$C$2)))+(5\*((($D$2+N3)/2)\*(D3/$D$2)))+(5\*((($E$2+O3)/2)\*(E3/$E$2)))+(3\*((($F$2+P3)/2)\*(F3/$F$2)))+(((($G$2+Q3)/2)\*(G3/$G$2))/100))

Though it may not seem like it, this command (*H4*) is similar, but it accounts for the value the opponents ALLOW in the given statistical categories.

I built fantasy teams based off of both methods of projeciton, played in several competetions, and came away with several hundred dollars in the end. Not a bad way to spend some time in 2020 :)
