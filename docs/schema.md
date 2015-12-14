# Schema Information



## track
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
title       | string    | not null
description | text      | not null
genre       | string    | not null
artist_id   | integer   | not null, foreign key (references users), indexed
album_id    | integer   | not null, foreign key (references notebooks), indexed
file_url    | string    | not null, (thinking of using amazon web services for cdn)
play_count  | integer   | not null

## albums
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
artist_id   | integer   | not null, foreign key (references users), indexed
title       | string    | not null
track_list  | string    | 

## playlist
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
creator_id  | integer   | not null, foreign key (references users), indexed
track_list  | string    | 

## follows
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
follower_id | integer   | not null, foreign key (references users), indexed
followee_id | integer   | not null, foreign key (references users), indexed

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
username        | string    | not null, indexed, unique
profile_pic_url | string    | not null
password_digest | string    | not null
session_token   | string    | not null, indexed, unique


## comments
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
author_id       | integer   | not null, indexed, foreign key (references users), unique
body            | text      | not null
track_id        | integer   | not null, foreign key (references tracks), indexed
timestamp       | string    | not null, identifies location to place comment through duration of track
