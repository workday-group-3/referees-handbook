# Project Plan

Pod Members: Ernesto Enriquez, Aileen Ji, Travis Navarro

## Problem Statement and Description

Insert the latest summary of your problem statement and app description.

All in one guide to learning a new sport for fans, so that they can carry a conversation amongst friends or be able to understand the rules of a game while watching. Target audience is for people who want to get into watching a new sport.

A website where beginners could learn the rules and history of any sport, how it's played, and common terms so that you could follow along watching any game and join in conversation among your friends. Added features can be stats and details about collegiate, amateur, and professional teams, statistics for each player, and the history of each team. Lastly, a fantasy league component could be added, or a recent events page where you can see that team's upcoming games and who they're against.

## User Roles and Personas

Include the most up-to-date user roles and personas.

**User roles**

Sports fan - Seeking knowledge and advice on how to play a new sport or tips and tricks they can use

Coach - Looking to give back to sports community by creating new course with their knowledge

Amateur sports player - Trying to improve upon their techniques and strategies by reading up on user created courses

**User Personas**

Bob Scott, Middle school football coach from Salina, Kansas
Age 45, average sophistication with technology, mainly uses smartphone, accesses site weekly 
Motivation is to give back to community and spread wealth within football community
Potential pain points are accessibility for creating courses and navigation throughout the learning center page

James Franklin, College level football coach from State College, PA
Age 36, high level sophistication with technology, uses a desktop, and accesses the site daily
Motivation is to check for new developments in football community, and add new football plays he could use during practice for his team
Potential pain points might be loading times throughout the site, being able to sort by newest courses to check latest developments

Josh, Golden State Warriors fan, 24 years old, recent college graduate from California, very familiar with technology. They mainly use a phone and access the site daily. Their motivation is to keep up with Golden State Warrior because they love the team, potential pain points is easy access to the specific team and sport they are interested in.


Isabella, basketball fan, 30 year old from Boston, Massachusetts, busy businesswoman, not super good with technology. She mainly uses her computer and access the site every week. Her motivation is to keep up with information related to her favorite basketball team without having to spend a lot of time using search engines. Potential pain points are being able to navigate the website and search for useful information easily.

Suleiman Q., middle school sports player 11 years old from Scranton, PA
High level sophistication with technology, uses a smartphone, accesses the site monthly
Motviation to is become a better player and work on throwing techniques
Potential pain points might be being able to do a simple search, or having web responsiveness from his smartphone

Nikolas, high school soccer player from Delaware
Age 16, high level sophistication with technology, uses a laptop and accesses the site bi-weekly
Motivation is to keep up with his favorite sports teams and follow their upcoming games
Potential pain points might be navigating the discovery page and being able to filter by following sports teams


## User Stories

1. As a Middle school football coach, I want to have open access to rules and regulations in an easily accessible manner and format, because I want to see if any plays I have in mind violate any rules. 

2. As an intermediate level tennis player, I want a platform that offers tips and strategies by other players which would serve to increase my current skills because it is often difficult to find online resources for my current skill level. 

3. As a basketball fan, I want a platform that displays all things related to basketball (or my favorite team) in an intuitive and digestible way because using search engines often takes too much time and the process of finding useful information can be roundabout. 

4. As a beginner soccer player, I wish to find a platform for learning more about how to get better at the game because, as a complete beginner, I’m not sure where I should start in my sports journey. 

5. As a student studying the history of my new favorite sport, I want to see it's evolution throughout the years

6. As a retired basketball coach, I want to create online courses for others so I can share my passion and accumulated understanding of the game with future players. 

7. As an NBA fan, I want a website that delivers up to date basketball news because I love keeping up with the latest updates on players and teams. 

8. As an innovative tennis player, I want a website that allows me to share my upcoming and new techniques, because I love showing newer players my hidden strategies in tennis.

9. As someone who likes to dabble in all sports, I want one central hub that I can rely on so I can keep up to date with new courses & strategies in each sports community and stay on top of my game.

10. As a Golden State Warriors fan, I want to be able to keep up with their recents game quickly and see an up to date stat sheet with their win/loss record, so I can keep up with analysts when I watch the game.

## Pages/Screens

Login, registration, landing, home, profile, learning center, beginner course, user created course

MVP wireframes (high fidelity):

[![image](https://user-images.githubusercontent.com/73731802/179061253-e47607d0-29bf-4332-b594-b3f6c61949cc.png)](https://www.figma.com/file/6C4n8jyxLDV2LetttFvioE/Referee-handbook-wireframe?node-id=0%3A1)

All wireframes contained in figma link below:

[![image](https://user-images.githubusercontent.com/73731802/178373605-807ca31c-7998-485c-a6c7-2dabb8d9209e.png)](https://www.figma.com/file/6C4n8jyxLDV2LetttFvioE/Referee-handbook-wireframe?node-id=0%3A1)

## Data Model

Describe your app's data model using diagrams or tables

User Table:

| Column Name | Type | Description |
| ----------- | ---- | ----------- |
| id | integer | Primary key |
| email | text | User's email |
| username | text | User's username |
| password | text | User's password |
| first_name | text | User's first name |
| last_name | text | User's last name |
| location | text | User's city and state |
| created_at | date | User's account creation date |


Beginner courses Table:

| Column Name | Type | Description |
| ----------- | ---- | ----------- |
| id | integer | Primary key |
| sport_name | text | Name of sport to be listed under |
| beginner_history_timeline| text | Timeline URL for iframe to run timeline widget |
| beginner_rules | text | Rules of the sport |
| beginner_short_description | text | Sentence long hook for the user to draw in readers, shown in course list page |
| beginner_cover_image_URL | text | Cover image, shown in course list page |
| beginner_tutorial_video_URL | text | URL to tutorial video for sport |
| beginner_field_diagram_URL | text | Image URL for field diagram |
| created_at | date | Beginner course created date |



## POST MVP ADDITIONS FOR DATA MODEL

Followers to following Table:

| Column Name | Type | Description |
| ----------- | ---- | ----------- |
| follower_id | integer | Primary key |
| following_id | integer | Id of team user is following |
| following_at | date | Date user started following the team |


User created courses Table:

| Column Name | Type | Description |
| ----------- | ---- | ----------- |
| id | integer | Primary key |
| sport_name | text | Name of sport to be listed under |
| user_id | integer | Id of the user who created the course |
| course_title | text | Title of the course |
| course_short_description | text | Sentence long hook for the user to draw in readers, shown in course list page |
| course_cover_image_URL | text | Cover image, shown in course list page |
| course_content | text | Main content of the course |
| course_tutorial_video_URL | text | URL to tutorial video |
| course_tips_tricks | text | Content for tips and trick |
| created_at | date | Course created date |


## Endpoints

List the API endpoints you will need to implement.


| CRUD | HTTP Verb | Description | User stories |
| ---- | --------- | ----------- |------------|
|Read|POST|Logs the user in|6, 8, 10|
|Create|POST|Creates a new user account|6, 8, 10|
|Read|GET|Fetch the user's profile|6, 8, 10|
|Read|GET|Fetches the beginner course for a specific sport|1, 4, 5|

## POST MVP ADDITIONAL ENDPOINTS

| CRUD | HTTP Verb | Description | User stories |
| ---- | --------- | ----------- |------------|
|Read|GET|Fetches standings, recent matches and news about a specific sport|3, 7|
|Read|GET|Fetches a list of teams for a sport|3, 7|
|Read|GET|Fetches the newest games for a sport|3, 7|
|Read|GET|Fetches the latest news for a sport|3, 7|
|Create|POST|Allows the user to follow a team|3, 7, 10|
|Read|GET|Fetches detailed information about a specific team|3, 7, 10|
|Create|POST|Creates a new course for a specific sport|6, 8|
|Read|GET|Fetches a list of user created courses for a specific sport|2, 4, 9|
|Read|GET|Fetches a specific course created by a user|2, 9|

***Don't forget to set up your Issues, Milestones, and Project Board!***
