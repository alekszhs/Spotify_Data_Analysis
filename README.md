# 🎧 Spotify Listening Behavior Analysis

📝 Project Overview
This project explores patterns in Spotify user listening habits using Python. The dataset includes track-level playback history, and the analysis focuses on play duration, platform usage, track skipping behavior, and time-based engagement.

📂 Data Loading and Preprocessing
- Loaded listening history from a .csv file
- Displayed sample rows, basic metadata, and data types
- Converted timestamp ts into separate columns: date, hour, day, and month
- Filtered out entries where ms_played == 0
- Created a new column seconds_played by converting milliseconds to seconds
- Filled missing values in reason_start and reason_end with 'missing'
- Verified data cleanliness using isnull().sum()

📈 Summary Statistics
Calculated core metrics:
- Total listening time
- Mean, median, min, and max play durations
- Total number of tracks played
- Count of unique artists
- Tracks played per platform
These give a snapshot of overall usage intensity and diversity.

📊 Time-Based Analysis
🔹 Seconds Per Day
- Grouped playtime by day
- Bar chart shows total daily listening behavior
- Highlights active vs. less active days
🔹 Seconds Per Hour
- Grouped playtime by hour of day
- Red bar chart visualizes peak listening hours
- Reveals hourly engagement patterns (e.g., morning vs. late-night music)

📱 Platform-Based Analysis
🔹 Daily Platform Usage
- Grouped by day and platform
- Pivoted for easier side-by-side comparison
- Great for visualizing how platforms trend day by day
🔹 Distribution of Playtime by Platform
- Grouped total seconds_played by platform
- Displayed using a pie chart
- Highlights dominant listening devices (e.g., mobile vs. desktop)

🎶 Popularity Breakdown
🔹 Top 10 Songs
- Based on total seconds played
- Identifies most engaging tracks
🔹 Top 10 Artists
- Based on cumulative listening time
- Spotlights fan favorites and high-play artists

🚫 Skipped Track Analysis
- Filtered tracks with skipped == True
- Grouped by track_name and counted skips
- Revealed the top 10 most skipped songs—possible indicators of low engagement or playlist fatigue

🧭 Start Reason Analysis
- Counted how often each reason_start value appeared
- Normalized to percentages for fair comparison
- Visualized with a bar chart to show interaction trends (e.g., manual selection vs. playlist autoplay)

✅ Final Thoughts
This Spotify analysis combines exploratory data processing, descriptive statistics, and intuitive visualizations to uncover how, when, and why music is played. You could enhance this further with:
- Time-series trends per artist or genre
- Playlist-specific analysis
- User segmentation (if you had user IDs)

