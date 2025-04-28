<h1 align="center">🎶 Spotify Listening  Dashboard</h1>

<p align="center">
Analyze Spotify user streaming patterns, device usage, and engagement insights through an interactive Power BI dashboard.
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project visualizes user listening behavior using real Spotify streaming data. It aims to uncover insights about user engagement, device/platform usage, song popularity, and streaming habits. The dashboard is built in Power BI, offering an interactive experience for deeper exploration.
</p>

<hr>

<h2>📚 Dataset Description</h2>

<p>This project uses a Spotify dataset that captures user interactions, playback behavior, and engagement metrics. Below are the details of each column:</p>

<h3>1. <strong>spotify_track_uri</strong></h3>
<ul>
<li><strong>Description:</strong> A unique identifier assigned to each track in Spotify’s database.</li>
<li><strong>Format:</strong> <code>spotify:track:&lt;base-62 string&gt;</code> (e.g., <code>spotify:track:3n3Ppam7vgaVa1iaRUc9Lp</code>)</li>
<li><strong>Purpose:</strong> Helps link tracks to their metadata and allows for cross-referencing with Spotify’s catalog.</li>
</ul>

<h3>2. <strong>ts (Timestamp)</strong></h3>
<ul>
<li><strong>Description:</strong> The exact time (in UTC) when the track stopped playing.</li>
<li><strong>Format:</strong> ISO 8601 format (e.g., <code>2024-02-07T14:30:45Z</code>)</li>
<li><strong>Purpose:</strong> Used for analyzing listening patterns, session durations, and track end times.</li>
</ul>

<h3>3. <strong>platform</strong></h3>
<ul>
<li><strong>Description:</strong> The device or platform used to stream the track.</li>
<li><strong>Possible Values:</strong>
  <ul>
    <li><code>desktop</code> (Windows/Mac app)</li>
    <li><code>mobile</code> (iOS/Android app)</li>
    <li><code>web</code> (Spotify Web Player)</li>
    <li><code>smart_speaker</code> (Amazon Echo, Google Home, etc.)</li>
  </ul>
</li>
<li><strong>Purpose:</strong> Helps understand where users are consuming music.</li>
</ul>

<h3>4. <strong>ms_played</strong></h3>
<ul>
<li><strong>Description:</strong> The total number of milliseconds the track was played before stopping or skipping.</li>
<li><strong>Format:</strong> Integer value (e.g., <code>215000</code> for 3 minutes 35 seconds)</li>
<li><strong>Purpose:</strong> Useful for engagement analysis, identifying completed plays, and calculating revenue.</li>
</ul>

<h3>5. <strong>track_name</strong></h3>
<ul>
<li><strong>Description:</strong> The title of the song being played.</li>
<li><strong>Example:</strong> "Shape of You"</li>
<li><strong>Purpose:</strong> Helps in analyzing the most played tracks.</li>
</ul>

<h3>6. <strong>artist_name</strong></h3>
<ul>
<li><strong>Description:</strong> The name of the artist performing the song.</li>
<li><strong>Example:</strong> "Ed Sheeran"</li>
<li><strong>Purpose:</strong> Useful for ranking popular artists and identifying user preferences.</li>
</ul>

<h3>7. <strong>album_name</strong></h3>
<ul>
<li><strong>Description:</strong> The name of the album the track belongs to.</li>
<li><strong>Example:</strong> "÷ (Divide)"</li>
<li><strong>Purpose:</strong> Helps analyze album popularity and user listening trends.</li>
</ul>

<h3>8. <strong>reason_start</strong></h3>
<ul>
<li><strong>Description:</strong> The reason why the track started playing.</li>
<li><strong>Possible Values:</strong>
  <ul>
    <li><code>trackdone</code> (Previous track ended)</li>
    <li><code>clickrow</code> (User manually selected the song)</li>
    <li><code>backbtn</code> (User pressed back)</li>
    <li><code>fwdbtn</code> (User pressed next)</li>
    <li><code>playbtn</code> (User pressed play)</li>
    <li><code>autoplay</code> (Spotify automatically selected the next track)</li>
  </ul>
</li>
<li><strong>Purpose:</strong> Helps understand user behavior and track engagement patterns.</li>
</ul>

<h3>9. <strong>reason_end</strong></h3>
<ul>
<li><strong>Description:</strong> The reason why the track stopped playing.</li>
<li><strong>Possible Values:</strong>
  <ul>
    <li><code>trackdone</code> (Track finished playing)</li>
    <li><code>endplay</code> (User paused or stopped playback)</li>
    <li><code>fwdbtn</code> (User skipped to the next track)</li>
    <li><code>backbtn</code> (User went back to the previous track)</li>
    <li><code>logout</code> (User logged out or session ended)</li>
  </ul>
</li>
<li><strong>Purpose:</strong> Helps identify why users stop listening to tracks.</li>
</ul>

<h3>10. <strong>shuffle</strong></h3>
<ul>
<li><strong>Description:</strong> Indicates whether shuffle mode was enabled during playback.</li>
<li><strong>Possible Values:</strong> <code>TRUE</code> (Shuffle mode ON) / <code>FALSE</code> (Shuffle mode OFF)</li>
<li><strong>Purpose:</strong> Helps analyze how often users use shuffle mode during listening sessions.</li>
</ul>

<h3>11. <strong>skipped</strong></h3>
<ul>
<li><strong>Description:</strong> Indicates whether the user skipped the song before it finished.</li>
<li><strong>Possible Values:</strong> <code>TRUE</code> (User skipped) / <code>FALSE</code> (User did not skip)</li>
<li><strong>Purpose:</strong> Important for understanding user engagement, drop-off rates, and song popularity.</li>
</ul>

<hr>
<hr>

<h2>🎵 Albums Analysis Overview</h2>
<p>On the first page of the dashboard, the <em>Albums</em> container presents the following key metrics:</p>

<ul>
  <li>🎵 <strong>Total Albums Played Over Time</strong> – Track how album listening trends change over months and years.</li>
  <li>📅 <strong>Number of Albums Listened by Year</strong> – Identify annual listening habits and volume (find the minimum and maximum albums in the view).</li>
  <li>💥 <strong>Albums Played on Weekday &amp; Weekend</strong> – Compare listening patterns between weekdays and weekends.</li>
  <li>🏆 <strong>Top 5 Albums</strong> – Highlight the most played albums based on listening frequency.</li>
  <li>📊 <strong>Latest Year vs Previous Year Analysis</strong> – Compare album consumption between the latest and previous years, including:
    <ul>
      <li><strong>LY (Latest Year) vs PY (Previous Year) Trends</strong></li>
      <li><strong>YoY (Year-over-Year) Growth Analysis</strong></li>
    </ul>
  </li>
</ul>


<hr>

<h2>🎶 Artists Analysis Overview</h2>
<p>On the second page of the dashboard, the <em>Artists</em> container presents the following key metrics:</p>

<ul>
  <li>🎵 <strong>Total Artists Played Over Time</strong> – Track how artist listening trends evolve across months and years.</li>
  <li>📅 <strong>Number of Artists Listened by Year</strong> – Identify annual listening habits and artist diversity (find the minimum and maximum artists in the view).</li>
  <li>💥 <strong>Artists Played on Weekday &amp; Weekend</strong> – Compare listening patterns between weekdays and weekends.</li>
  <li>🏆 <strong>Top 5 Artists</strong> – Highlight the most played artists based on listening frequency.</li>
  <li>📊 <strong>Latest Year vs Previous Year Analysis</strong> – Compare artist engagement between the latest and previous years, including:
    <ul>
      <li><strong>LY (Latest Year) vs PY (Previous Year) Trends</strong></li>
      <li><strong>YoY (Year-over-Year) Growth Analysis</strong></li>
    </ul>
  </li>
</ul>


<hr>

<h2>🎵 Tracks Analysis Overview</h2>
<p>On the third page of the dashboard, the <em>Tracks</em> container presents the following key metrics:</p>

<ul>
  <li>🎵 <strong>Total Tracks Played Over Time</strong> – Monitor how track listening trends change across months and years.</li>
  <li>📅 <strong>Number of Tracks Listened by Year</strong> – Identify annual listening habits and track diversity (find the minimum and maximum tracks in the view).</li>
  <li>💥 <strong>Tracks Played on Weekday &amp; Weekend</strong> – Compare listening patterns between weekdays and weekends.</li>
  <li>🏆 <strong>Top 5 Tracks</strong> – Highlight the most played tracks based on listening frequency.</li>
  <li>📊 <strong>Latest Year vs Previous Year Analysis</strong> – Compare track engagement between the latest and previous years, including:
    <ul>
      <li><strong>LY (Latest Year) vs PY (Previous Year) Trends</strong></li>
      <li><strong>YoY (Year-over-Year) Growth Analysis</strong></li>
    </ul>
  </li>
</ul>



<h3>📷 Dashboard Screenshot</h3>
<p align="center">
  <img src="[albums_dashboard.png](https://github.com/Vinit-joshi2/Spotify-DashBoard/blob/main/Image1.png)" alt="Albums Dashboard Screenshot" width="800">
</p>





<h2>🖼️ Dashboard Preview</h2>

<!-- You can insert your dashboard screenshot here -->

<a href = "https://github.com/Vinit-joshi2/Spotify-DashBoard/blob/main/Spotify%20DashBoard.pdf">Spotify DashBoard</a>

<hr>

<h2>🏷️ Tags</h2>

<p>
<code>#spotify</code> <code>#spotifydashboard</code> <code>#musicdata</code> <code>#dataanalysis</code> <code>#eda</code> <code>#powerbi</code> <code>#datavisualization</code> <code>#userbehavior</code> <code>#musicstreaming</code> <code>#dataanalytics</code>
</p>
