### Spotify-DashBoard

📑 Dataset Description
This project uses a Spotify dataset that captures user interactions, playback behavior, and engagement metrics. Below are the details of each column:

# 1. spotify_track_uri
Description: A unique identifier assigned to each track in Spotify’s database.

Format: spotify:track:<base-62 string> (e.g., spotify:track:3n3Ppam7vgaVa1iaRUc9Lp)

Purpose: Helps link tracks to their metadata and allows for cross-referencing with Spotify’s catalog.

# 2. ts (Timestamp)
Description: The exact time (in UTC) when the track stopped playing.

Format: ISO 8601 format (e.g., 2024-02-07T14:30:45Z)

Purpose: Used for analyzing listening patterns, session durations, and track end times.

3. platform
Description: The device or platform used to stream the track.

Possible Values:

desktop (Windows/Mac app)

mobile (iOS/Android app)

web (Spotify Web Player)

smart_speaker (Amazon Echo, Google Home, etc.)

Purpose: Helps understand where users are consuming music.

4. ms_played
Description: The total number of milliseconds the track was played before stopping or skipping.

Format: Integer value (e.g., 215000 for 3 minutes 35 seconds)

Purpose: Useful for engagement analysis, identifying completed plays, and calculating revenue.

5. track_name
Description: The title of the song being played.

Example: "Shape of You"

Purpose: Helps in analyzing the most played tracks.

6. artist_name
Description: The name of the artist performing the song.

Example: "Ed Sheeran"

Purpose: Useful for ranking popular artists and identifying user preferences.

7. album_name
Description: The name of the album the track belongs to.

Example: "÷ (Divide)"

Purpose: Helps analyze album popularity and user listening trends.

8. reason_start
Description: The reason why the track started playing.

Possible Values:

trackdone (Previous track ended)

clickrow (User manually selected the song)

backbtn (User pressed back)

fwdbtn (User pressed next)

playbtn (User pressed play)

autoplay (Spotify automatically selected the next track)

Purpose: Helps understand user behavior and track engagement patterns.

9. reason_end
Description: The reason why the track stopped playing.

Possible Values:

trackdone (Track finished playing)

endplay (User paused or stopped playback)

fwdbtn (User skipped to the next track)

backbtn (User went back to the previous track)

logout (User logged out or session ended)

Purpose: Helps identify why users stop listening to tracks.

10. shuffle
Description: Indicates whether shuffle mode was enabled during playback.

Possible Values: TRUE (Shuffle mode ON) / FALSE (Shuffle mode OFF)

Purpose: Helps analyze how often users use shuffle mode during listening sessions.

11. skipped
Description: Indicates whether the user skipped the song before it finished.

Possible Values: TRUE (User skipped) / FALSE (User did not skip)

Purpose: Important for understanding user engagement, drop-off rates, and song popularity.
