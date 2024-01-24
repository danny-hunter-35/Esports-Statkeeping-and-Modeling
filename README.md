# Esports-statkeeping-and-modeling

These two spreadsheets concern statistics and calculations associated with the video game **Rocket League**. 
As a formerly avid player, competiter, and fan of the game and associated eSport, I helped gather and display game statistics and individual accolades for a group of friends as well as develop methods for model projections of "fantasy" points for the pro scene.

**Pandamonium Team Stats** was a spreadsheet that a friend and I used to compile statistics, such as goals per game, which would then be compared to other members in our server to see who was, on that same example, the best striker. Most notably, I was able to update the rankings for these accolades automatically by developing commands in excel/google sheets such as the following

> =IF(IFNA(MATCH(INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)), $A$3:A3, 0), FALSE()), INDEX($A$18:$A$31, SMALL(IF($C$18:$C$31 = B4, ROW($C$18:$C$31) - MIN(ROW($C$18:$C$31)) + 1), (ROW(A4) -1) -MATCH(INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)), $A$3:A3, 0))), INDEX($A$18:$A$31, MATCH(LARGE($C$18:$C$31, (ROW(A4) - 2)), $C$18:$C$31, 0)))

In the *Server Accoloade Race* sheet of Pandamonium Team Stats, this command is in the cell *A4*. Essentially, the command searches the *GPG (Goals Per Game)* category on the same page (C18 through C31) and finds the 2nd highest number. From there, it finds the corresponding value in column A (the name of the player)
