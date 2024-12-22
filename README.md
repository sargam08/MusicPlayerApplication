  **MUSIC PLAYER APPLICATION**

A command-line-based Music Player built in Java that simulates managing music albums, songs, and playlists. It supports adding songs, creating playlists, and controlling playback (next, previous, replay).

# Project Overview:
This project implements a music player with the following core components:

Album Class: Represents an album containing multiple songs.
Song Class: Represents an individual song with a title and duration.
Main Class: Provides the entry point and implements the user interface to interact with the album and playlist.
The main functionalities include adding songs to albums, creating playlists, navigating through the songs in the playlist, and removing songs.

# Features
Create albums with multiple songs (title and duration).
Add songs to playlists by track number or title.
Play songs: next, previous, or replay.
List and manage playlist songs.
Remove songs from the playlist.

# Requirements:
Java 8 or higher.
No external libraries (uses built-in Java collections).

# Code Structure
1. Album.java
Handles album-related operations, including song management and adding songs to playlists.

2. Song.java
Represents an individual song with its title and duration. Provides functionality to get song details.

3. Main.java
The entry point of the application. Initializes albums, adds songs, and facilitates user interaction with the playlist.

4. Playlist Management
Songs are stored in an ArrayList within an album.
A LinkedList is used to represent the playlist, which allows easy manipulation (adding/removing songs).

Methods in Key Classes
Album:

addSong(String title, double duration): Adds a new song to the album.
addToPlaylist(String title, LinkedList<Song> playlist): Adds a song to the playlist by its title.
addToPlaylist(int trackNumber, LinkedList<Song> playlist): Adds a song to the playlist by its track number.

Main:

play(LinkedList<Song> playlist): Manages the playlist, allowing navigation through songs and handling user input for playback.
printMenu(): Prints available commands for user interaction.

# Installation
1. Clone the repository: git clone https://github.com/sargam08/music-player.git

2. Navigate to the project directory: cd music-player

3. Compile the code: javac src/com/sargam/*.java

4. Run the application: java -cp src com.sargam.Main

# Example Usage
The following steps show an example of how the app behaves:

Create albums and add songs.
Add songs to the playlist.
Play the playlist, navigate through songs, and remove songs.

# Sample Interaction:

Available options:
press
0 - to quit
1 - to play next song
2 - to play previous song
3 - to replay the current song
4 - list of all songs
5 - print all available options
6 - delete current song

# Project Structure

/.gitignore                     # Git ignore rules
.idea/                          # IDE configuration files (IntelliJ)
src/                            # Source code
  └── com/
        └── sargam/             # Main code directory
            └── Album.java     # Album class implementation
            └── Song.java      # Song class implementation
            └── Main.java      # Main application logic
            
# Design Decisions

LinkedList is used for the playlist because it allows efficient insertion and removal of songs from the playlist, making it ideal for this use case where songs can be added or removed dynamically.

ArrayList is used in the Album class because the size of the album is relatively fixed, and we are mostly adding new songs rather than frequently removing or inserting in the middle.

The use of ListIterator enables forward and backward navigation through the playlist, providing an intuitive way to handle song playback.

License
MIT License

