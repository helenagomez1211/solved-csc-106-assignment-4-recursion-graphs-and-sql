Download Link: https://assignmentchef.com/product/solved-csc-106-assignment-4-recursion-graphs-and-sql
<br>
In this part of the assignment you will write two recursive functions in Python.  As in the last assignment, you can do this online using:  <u>https://repl.it/languages/python3</u> but as last time, you will need to copy and save the code to .py files with the correct names to upload them to conneX.

<ol>

 <li>Exercise to draw concentric circles:

  <ol>

   <li>Download py</li>

   <li>Start by uncommenting and running the tests of the concentric_loop function one at a time to see what the output looks like</li>

   <li>Write the recursive version of this function in the file under the comments provided. Your function must be named concentric_recursive</li>

   <li>Test your function by uncommenting the tests of the concentric_recursive function one at a time to compare the output to that of concentric_loop</li>

  </ol></li>

 <li>Exercise to draw Serpinski Fractals

  <ol>

   <li>Download py</li>

   <li>Start by uncommenting and running the tests of the stri function one at a time to see what the output looks like.</li>

  </ol></li>

</ol>

Notice, in the simplest case stri(24, 0, 0) with a CUTOFF of 25, no recursive calls are made, and the basecase draws one triangle with side length of 24:

The next testcase is a call to stri(50, 0, 0) with a CUTOFF of 25. This case, starts with an equilateral triangle with side length of 50.  Inside  of that triangle, three more Sierpinski triangles are drawn with a side length of 25 (two on the bottom and one above).  The inner triangles are drawn in red to highlight the recursion:

With the later testcase stri(150, 0, 0) with a CUTOFF of 25. In this case, the outer triangle is drawn with side length 150, inside that triangle are 3 more Sierpinski triangles are drawn, and inside each of those 3 more Sierpinski triangles, and so on

If we were to lower the CUTOFF value it would take much more time to run the program, but a more detailed fractal would be drawn like this one from <u>https://en.wikipedia.org/wiki/Sierpinski_triangle</u> :

<ol start="3">

 <li>Write the recursive function scarpet in the file under the comments provided in serpinskiFractals.py. You are provided with a square function that you can call similarly to how the triangle function was called in the stri function provided.</li>

</ol>

Test your function by uncommenting the tests of the scarpet function one at a time to compare the output to the images below.

In the simplest case scarpet(24, 0, 0) with a CUTOFF of 25,  will draw one square:

The next testcase scarpet(75, 0, 0) with a CUTOFF of 25,  will draw one square of side length 75.  Inside this square, 8 inner Serpinski carpets of side length 25 (75/3) are drawn in 3 rows:

<ul>

 <li>3 Serpinski carpets are drawn along the bottom row</li>

 <li>2 Serpinski carpets are drawn on the second row, one on the far left and the other on the far right leaving a blank square in the middle – 3 Serpinski carpets are drawn along the top row</li>

</ul>

The third testcase stri(100, 0, 0) with a CUTOFF of 25 will draw the outer square of side length 100, inside that outer square 8 more Serpinski carpets are drawn and inside each of those 8 carpets, 8 more Serpinski carpets are drawn:The last testcase is stri(400, -200, -200) with a CUTOFF of 25 will draw an image like this:

If you want to generate a more detailed Serpinki Carpet you can reduce the CUTOFF value.  This can take hours to complete if your CUTOFF is very small relative to your staring size so do not feel you need to do this to test your solution.

If you do test this, you will notice the accuracy of the turtle is not perfect when the square drawing gets really small, but it does produce a nice Serpinski carpet.

If you were to lower the CUTOFF value a more detailed fractal would be drawn like this one from <u>https://commons.wikimedia.org/wiki/File:Sierpinski_carpet.png</u> :

<strong> </strong>TASK 2: Graphs and BigO

Log into conneX and navigate to the <strong>Tests &amp; Quizzes</strong> link on the sidebar.  You will see an Assignment 4 quiz.  You can use lab and lecture notes to help you answer these questions.  You can submit your quiz as many times as you want, your highest score will be recorded.

You must complete and submit before the deadline.  Late submissions will not be accepted for any reason.

<h1>TASK 3: SQL</h1>

Statistical data is available at our fingertips for almost anything we are interested in these days.  In this assignment resources you have been provided with a file

premierleague_data.sql which constructs an SQL database of English Premier League Soccer (<u>https://www.premierleague.com</u>) data from the 2017/2018 season.  This data is set comprised of three separate tables is described below.

Look in premierleague_data.sql to get exact column names for your queries:

<ul>

 <li>stadiums:

  <ul>

   <li>contains a record for each home stadium that a team in the league plays at o columns include the name of the home team that plays there, the city it is in, the name of the stadium and its capacity</li>

   <li>collected from: <u>https://opisthokonta.net/?p=619</u></li>

  </ul></li>

 <li>players:

  <ul>

   <li>contains a record for each player in the league</li>

   <li>columns include the player name, the name of the team they play for, their age, position they play and their nationality</li>

   <li>a position is one of (value = definition):

    <ul>

     <li>GK = Goalkeeper</li>

     <li>AM = Attacking Midfielder</li>

     <li>CB = Center Back</li>

     <li>CF = Center Forward</li>

     <li>CM = Center Midfielder</li>

     <li>LB = Left Back</li>

     <li>RB = Right Back</li>

     <li>LM = Left Midfielder</li>

     <li>RM = Right Midfielder</li>

     <li>SS = Second Striker</li>

     <li>DM = Defensive Midfielder</li>

     <li>RW = Right Wing</li>

     <li>LW = Left Wing o collected from: <u>https://www.kaggle.com/mauryashubham/english-premierleague-players-dataset</u></li>

    </ul></li>

  </ul></li>

</ul>




<ul>

 <li>games:

  <ul>

   <li>contains a record for each game played in 2017/2018 o there are many columns in this table including but not limited to: the home team name, away team name, winner of the game (one of H, A or D = home team, away team or draw/tie game), the number of fouls, red cards, yellow cards given to the home and away teams</li>

   <li>you will not need to use all of the columns provided but feel free to come up with your own queries on the data besides those you are asked to do!</li>

   <li>collected from: <u>https://datahub.io/sports-data/english-premierleague#resource-season-1718</u></li>

  </ul></li>

</ul>

Write the SQL queries for each of the questions below in the space provided in premierleague_queries.sql.  Do not modify any of the existing code in the files given, only add your queries below each question heading.

Your query outputs must match the sample outputs given below exactly including: column names, the data in each row and the ordering of the data.  Your column widths can be different.  A given query may only need to use one table or possibly multiple tables.




<ol>

 <li>Write a query to print the team name, city, stadium name and capacity of all stadiums in the league in order of decreasing capacity.</li>

</ol>

team_name             city                  stadium_name          capacity   ——————–  ——————–  ——————–  ———-

Man United            Stretford             Old Trafford          75811

Arsenal              London                Emirates Stadium      60361

Newcastle             Newcastle upon Tyne   Sports Direct Arena   52409

Man City              Manchester            Etihad Stadium        47405

Liverpool             Liverpool             Anfield               45276

Chelsea               London                Stamford Bridge       42449

Everton               Liverpool             Goodison Park         40157

Tottenham             London                White Hart Lane       36230

West Ham              London                Boleyn Ground         35303

Southampton           Southampton           St Marys Stadium      32689

Leicester City        Leicester             King Power Stadium    32500

West Brom             West Bromwich         The Hawthorns         27877

Stoke                 Stoke-on-Trent        Britannia Stadium     27740

Crystal Palace        London                Selhurst Park         26309

Huddersfield          Huddersfield          The John Smiths Stad  24500

Watford               Watford               Vicarage Road         23500

Burnley               Burnley               Turf Moor             22546

Brighton              Brighton              American Express Com  22374

Swansea               Swansea               Liberty Stadium       20520      Bournemouth           Bournemouth           Goldsands Stadium     12000

<ol start="2">

 <li>Write a query to print the names of the players that are goal keepers that play at a home stadium with a capacity between 30,000 and 50,000. You should print this in alphabetical order of the name of the stadium they play at, then in alphabetical order of the name of the player.</li>

</ol>

player_name           stadium_name         ——————–  ——————–

Loris Karius          Anfield

Simon Mignolet        Anfield

Adrian                Boleyn Ground

Darren Randolph       Boleyn Ground

Claudio Bravo         Etihad Stadium

Ederson Moraes        Etihad Stadium

Joel Robles           Goodison Park

Jordan Pickford       Goodison Park

Maarten Stekelenburg  Goodison Park

Ben Hamer             King Power Stadium

Kasper Schmeichel     King Power Stadium

Fraser Forster        St Marys Stadium

Thibaut Courtois      Stamford Bridge

Willy Caballero       Stamford Bridge

Hugo Lloris           White Hart Lane

Michel Vorm           White Hart Lane

<ol start="3">

 <li>Write a query to print the names of the referee, the number of games they have refereed and the number of red cards and yellow cards they award to the home team. The output should be in order of the number of red cards then by yellow cards.</li>

</ol>

referee          games_refereed   red_cards     yellow_cards —————  —————  ————  ————

D Coote          1                0             1

S Hooper         1                0             1

K Friend         21               0             16

P Tierney        16               0             16

M Jones          12               0             20

L Mason          18               0             24

S Attwell        15               0             26

C Kavanagh       15               0             27

N Swarbrick      20               0             28

M Dean           25               0             48

L Probert        14               1             12

G Scott          20               1             21

R East           18               1             21

R Madley         18               1             26

A Taylor         27               1             49

J Moss           29               1             53

A Marriner       28               2             41

M Oliver         30               2             47

M Atkinson       28               3             52           C Pawson         24               4             33




<ol start="4">

 <li>Write a query to print the nationality and the number of players of that nationality. Print those nationalities with either 1 player or more than 10 players in the league.  The data should be sorted by increasing number of players of a given nationality.</li>

</ol>

nationality           num_players    ——————–  ————–

Armenia               1

Benin                 1

Bermuda               1

Canada                1

Colombia              1

Croatia               1

Curacao               1

Estonia               1

Finland               1

Greece                1

Kenya                 1

New Zealand           1

Norway                1

Romania               1

Slovenia              1

The Gambia            1

Trinidad and Tobago   1

Tunisia               1

Uruguay               1

Venezuela             1

Brazil                12

Wales                 12

Scotland              14

Germany               16

Argentina             17

Ireland               17

Belgium               18

Netherlands           20

France                25

Spain                 28

England               156

<ol start="5">

 <li>Write a query to print the number of wins that each home team had. Print the result in decreasing order of wins.</li>

</ol>

team_name             num_wins       ——————–  ————–

Man City              16

Arsenal               15

Man United            15

Tottenham             13

Liverpool             12

Chelsea               11

Everton               10

Newcastle             8

Bournemouth           7

Brighton              7

Burnley               7

Crystal Palace        7

Leicester             7

Watford               7

West Ham              7

Huddersfield          6

Swansea               6

Stoke                 5

Southampton           4

West Brom             3

<ol start="6">

 <li><strong>OPTIONAL:</strong> Write a query to print the names of players on most winning team ordered by nationality then by player name. Tip: You will need to find the team with the maximum number of wins and join that result with the players table.</li>

</ol>

player_name           team_name       nationality  ——————–  ————–  ————

Nicolas Otamendi      Man City        Argentina

Sergio Aguero         Man City        Argentina

Kevin De Bruyne       Man City        Belgium

Vincent Kompany       Man City        Belgium

Ederson Moraes        Man City        Brazil

Fernandinho           Man City        Brazil

Fernando              Man City        Brazil

Gabriel Jesus         Man City        Brazil

Claudio Bravo         Man City        Chile

Yaya Toure            Man City        Cote dIvoire

Fabian Delph          Man City        England

John Stones           Man City        England

Kyle Walker           Man City        England

Raheem Sterling       Man City        England

Ilkay Gundogan        Man City        Germany

Leroy Sane            Man City        Germany

Kelechi Iheanacho     Man City        Nigeria

Bernardo Silva        Man City        Portugal

Aleksandar Kolarov    Man City        Serbia

David Silva           Man City        Spain