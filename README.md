# Music Player

This JavaScript-based music player allows users to play, pause, shuffle, and navigate through a playlist of songs. The player provides an interactive user interface with controls for managing playback, as well as options to add, delete, and reset songs in the playlist.

## Features

- Play and pause songs
- Navigate to the next or previous song
- Shuffle the playlist
- Delete songs from the playlist
- Reset the playlist to its original state
- Update display with the current song's title and artist
- Highlight the currently playing song
- Accessible controls with aria-labels for better usability

## HTML Structure

- **Playlist Container**: `playlist-songs` - Holds the list of songs.
- **Play Button**: `play` - Starts playing the selected song or the first song in the playlist.
- **Pause Button**: `pause` - Pauses the currently playing song.
- **Next Button**: `next` - Plays the next song in the playlist.
- **Previous Button**: `previous` - Plays the previous song in the playlist.
- **Shuffle Button**: `shuffle` - Randomizes the order of songs in the playlist.

## JavaScript Functions

- **`playSong(id)`**: Plays the song with the specified `id`. Updates the user data and UI accordingly.
- **`pauseSong()`**: Pauses the currently playing song and updates the `userData`.
- **`playNextSong()`**: Plays the next song in the playlist, if available.
- **`playPreviousSong()`**: Plays the previous song in the playlist, if available.
- **`shuffle()`**: Randomizes the order of songs in the playlist and updates the UI.
- **`deleteSong(id)`**: Deletes the song with the specified `id` from the playlist. If the deleted song is the current song, it resets playback.
- **`setPlayerDisplay()`**: Updates the display with the current song's title and artist.
- **`highlightCurrentSong()`**: Highlights the currently playing song in the playlist.
- **`renderSongs(array)`**: Renders the playlist based on the provided array of songs.
- **`setPlayButtonAccessibleText()`**: Updates the `aria-label` of the play button based on the current song.
- **`getCurrentSongIndex()`**: Retrieves the index of the currently playing song in the playlist.
- **`sortSongs()`**: Sorts the songs alphabetically by title.

## Usage

1. **Initialization**: 
   - The playlist is initially populated with songs from the `allSongs` array.
   - Songs are rendered and sorted by title upon initialization.

2. **Control Interactions**:
   - Clicking the play button starts playback of the selected song.
   - Clicking the pause button pauses playback.
   - Clicking the next or previous buttons navigates through the playlist.
   - Clicking the shuffle button randomizes the playlist order.
   - Clicking the delete button removes a song from the playlist.
   - Clicking the reset button restores the playlist to its original state.

3. **Event Handling**:
   - The `audio` element triggers an `ended` event to automatically play the next song or reset the player if no next song is available.

## Dependencies

- **HTML5 Audio API**: Used for playing audio files.
- **CSS**: For styling and layout (assumed to be present but not included in the script).
