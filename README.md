# Chat-Application :iphone:

It is a classic chat application that you can chat with your friends or other people in a channel. You can chat in same network or online. This is a school project that we make. We used websocket for the connection. It does keep attributes in mysql database like messages, date, who send the message, first name, last name, nickname etc. We used xampp for the apache and mysql. You have to create a database for keep the messages. We used php, html, SQL.

## How to run websocket

On Linux:
- php -q php-socket.php
- php -S 0.0.0.0:8000 index2.php

The parameter in the first command means quite and php runs the socket silently. Your terminal will be frozen after the first command, so either a second command
use terminal or type php -q php-socket.php&. The & sign makes it run in the background.

The second command allows you to run index2.php on port 8000.

## How to activate DB :eyes:
We used XAMPP for our project. It is so simple, you have to download [xampp](https://www.apachefriends.org/tr/download.html) and create a database named chat_app. Later create tables named; signup and posts with attributes respectively (uid, first_name, last_name, username, email, password.), (id, msg, date, name). 

There are the SQL codes:

```
CREATE TABLE `signup` (
    `id` int(11) NOT NULL AUTO_INCREMENT PRIMARY KEY,
    `username` varchar(30) NOT NULL,
    `first_name` varchar(15) NOT NULL,
    `last_name ` varchar(25) NOT NULL, 
    `email` varchar(50) NOT NULL,
    `password` varchar(50) NOT NULL) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `posts` (
    `id` int(11) NOT NULL AUTO_INCREMENT PRIMARY KEY,
    `msg` varchar(100) NOT NULL,
    `date` DATETIME DEFAULT CURRENT_TIMESTAMP,
    `name` varchar(25) NOT NULL) ENGINE=InnoDB DEFAULT CHARSET=latin1;

ALTER TABLE `signup` ADD UNIQUE(`username`);
ALTER TABLE `signup` ADD UNIQUE(`email`);

```
For deleting empty messages we created a trigger function like this:

```
CREATE TRIGGER trigger1
  AFTER INSERT
  ON  posts
  FOR EACH ROW 
DELETE FROM posts WHERE msg = ''";

```
It has to look like this: 
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/tablolar%20.JPG)
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/Resim13.png)
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/Resim14.png)


## Structure :classical_building:
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/Resim1.png)

## Screenshots :camera:
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/1.JPG)
![](https://github.com/eneeesyk/Chat-Application/blob/main/chat%20app%20ss/Resim2.png)


## Requests :bell:
If you find a bug or a feature, you can open an issue [here](https://github.com/eneeesyk/English-Turksih-Game/issues/new) by including your search query and the expected result.

## Contact with me! :telephone_receiver:
[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/linkedin.png" title="LinkedIn">](https://www.linkedin.com/in/enes-yedikardes-b989041ba/)       [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/github.png" title="Github">](https://github.com/eneeesyk)     [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/instagram-new.png" title="Instagram">](https://instagram.com/eneesyk/) 
[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/twitter.png" title="LinkedIn">](https://twitter.com/eneees_yk)
