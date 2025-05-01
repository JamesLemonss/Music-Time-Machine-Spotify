Billboard 100 to Spotify Playlist Creator
Have you ever wondered what music was topping the charts on the day you were born, graduated, or had your first heartbreak? This Python script takes you on a nostalgic journey by letting you enter a date, then scraping the Billboard Hot 100 chart for that day and creating a private Spotify playlist with those songs — ready for you to relive that moment.

WHAT This Project Does
This project is a small yet powerful automation tool built with Python. When executed, it asks the user to input a date in the YYYY-MM-DD format. It then scrapes the Billboard website to retrieve the top 100 songs listed for that day. Each of those song titles is searched on Spotify, and if found, it’s added to a brand-new, private playlist under your Spotify account. This is a fun way to explore music from any past moment — your birthday, your parents' anniversary, or even the day your favorite movie came out.

HOW It Works
The script uses the requests and BeautifulSoup libraries to fetch and parse the HTML content of the Billboard Hot 100 chart for a specific date. It then uses the spotipy library to authenticate with the Spotify Web API using your developer credentials and create a new playlist in your account.

Each song title scraped from Billboard is used to search for a corresponding track on Spotify. If found, its URI (unique Spotify identifier) is stored. Once all matches are collected, the script automatically creates a private playlist titled with the input date and adds all the found tracks to it. If a song is not available on Spotify, it is gracefully skipped with a console message.

Example Output
If you entered 2005-07-01, a playlist titled 2005-07-01 Billboard 100 would be created in your Spotify account, containing as many matches from the top 100 songs as could be found.

Songs not found on Spotify (due to metadata differences or regional unavailability) are skipped, and you’ll see a message in the terminal like:
“Song Title” doesn’t exist in Spotify. Skipped.


WHY Use This?
This tool is great for music lovers, nostalgia seekers, or developers wanting to explore web scraping and API integration. It's also a fun way to build curated playlists from memorable dates in your life, share throwback playlists with friends, or explore the evolution of music over time.

🔐 Privacy
All playlists created are private by default. You will be prompted to log into your Spotify account the first time you run the script. Authentication tokens are stored locally to avoid repeated logins.
