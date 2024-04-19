# BrickBreakerGame

In this project, the classic brickbreaker game has been implemented, which has three levels of varying difficulty - easy, medium and difficult. For each level, multithreading has been implemented where one thread is used to update ball positions and check for collisions  , and the other thread is used to redraw the game screen. In this game, two types of player modes have been implemented - singleplayer and multiplayer.

Now each level is differentiated by increasing level of difficulty- from easy to difficult.   Different factors like speed of ball, number of bricks, brick layout etc have been used to alter the game difficulties across different levels.
       
I have used JDBC to connect the Java game to MySQL. In MySQL, I have created a database for storing and retrieving the highest scores obtained by users across each of the levels. The database consists of several tables that are queried in order to display the all-time highest score in a particular level  along with the current user's own highest score. Additionally, there is a table in the database which keeps note of all the players created.
      
For the purpose of the multiplayer game, we need to track real-time interactions across both of the players. This has been achieved using the concepts of sockets for network programming. The setup consists of a server and 2 clients that would connect to the server. The 2 clients would routinely share game state data with the server upon the updation of a score or upon the ending of a game. The server would receive this data from one client and simply relay it onwards to the other client. The client would then render this received data from the server along with its own game state.
