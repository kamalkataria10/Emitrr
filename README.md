# Emitrr-Project

<h2>Fullstack Quiz App</h2>
To run application locally, you need to download the zip folder of project and you need to update some code to run application.<br/>
You need to update the MySQL Credentials in API/util/database with your credential <br/>
You need to run npm install in both emitrr-project/API directory and emitrr-project/Client directory <br/>
After doing these set up we need to run npm start in both above mentioned directory.

<h3>Database Logic</h3>
There are total 3 table 1)User, 2)Questions, 3)userQuestions

1. User table --> there are total 6 column username, email, password, totalScore, correctAnswer, incorrectAnswer
2. Questions --> there are total 8 column question, option_a, option_b, option_c, option_d, correct_option, language, difficulty
3. userQuestion --> it is used for do many to many relation between User and Question

<h3>Backend Logics</h3>
There are many API endpoins routes we will see all one by one. <br/>

user/signup:

Registers a new user with username, email, and password securely stored using bcrypt.
user/login:<br>

Allows an existing user to log in, sending a JWT token for authentication.<br>
user/reset:

Resets the user profile by deleting totalScore, correctAnswer, incorrectAnswer, and associated UserQuestions.<br>
user/leaderboard:

Retrieves and displays a leaderboard of all users ordered by total score.
