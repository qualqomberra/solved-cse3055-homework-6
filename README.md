Download Link: https://assignmentchef.com/product/solved-cse3055-homework-6
<br>
Consider the <em>Turkish Super League</em> database accompanied with this homework.

<strong><em>Player</em></strong><em> (<u>PlayerID</u></em><em>: int</em><em>,   FirstName</em><em>: nvarchar(25)</em><em>,   LastName</em><em>: nvarchar(25)</em><em>,   Nationality</em><em>: varchar(25)</em><em>,   Birthdate</em><em>: smalldatetime</em><em>,   Age</em><em>: smallint</em><em>,   Position</em><em>: varchar(25)</em><em>) </em>

<strong><em>Team</em></strong><em> (<u>TeamID</u></em><em>: int</em><em>,   Name</em><em>: nvarchar(50)</em><em>,   City</em><em>: nvarchar(25)</em><em>) </em>

<strong><em>PlayerTeam</em></strong><em> (<u>PlayerID</u></em><em>: int</em><em>,   <u>TeamID</u></em><em>: int</em><em>,   <u>Season</u></em><em>: varchar(5)</em><em>) </em>

<strong>Match</strong> (<u>MatchID</u>: int,   HomeTeamID: int,   VisitingTeamID: int,   DateOfMatch: smalldatetime,   Week: tinyint)

<strong><em>Goals</em></strong><em> (<u>MatchID</u></em><em>: int</em><em>,   <u>PlayerID</u></em><em>: int</em><em>,   IsOwnGoal</em><em>: bit</em><em>,   <u>Minute</u></em><em>: tinyint</em><em>) </em>

<u>Notes</u>:

<ul>

 <li>Table <em>Match</em> stores data only for season 2013-2014.</li>

 <li>Table <em>Goals</em> stores data only for season 2013-2014.</li>

</ul>

<strong>1</strong> Implement a stored procedure <em>sp_GetStandingsUpToDate (aDate)</em> such that <em>exec sp_GetStandingsUpToDate (aDate)</em> computes and shows the standings table, same as in the

following figure, up to the date <em>aDate</em> (inclusive).

Calling with any invalid date causes an error with a message “Invalid date!” All transactions that have been done will be rolled back and stop doing further operations.<strong>           </strong>

<strong> </strong>

<em>Notes: </em>

<ul>

 <li>Invalid date: any date not between 2013-08-16 and 2014-07-31.</li>

 <li>The order of the table: Firstly, Pts; secondly, GT; thirdly, GF.</li>

 <li>Pos will be automatically generated according to the order. Study on ranks.</li>

 <li>GP (Games Played): the number of matches that a team has played.</li>

 <li>W (Wins): the number of wins of a team in all games that have been played.</li>

 <li>T (Ties/Deuce): the number of ties of a team in all games that have been played.</li>

 <li>L (Losts): the number of losts of a team in all games that have been played.</li>

 <li>GF (Goals For/Forward): the number of goals scored of a team in all games that have been played, including own goals of the other team.</li>

 <li>GA (Goals Against): the number of goals scored by the other teams in all games that have been played, including own goals of the team.</li>

 <li>GD (Goals Difference): GF-GA.</li>

 <li>Pts (Points): the points accumulated by a team. For each win, a team gets 3 points; for each tie, a team gets 1 point; and, for each lost, a team gets 0 points.</li>

</ul>


