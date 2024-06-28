 detailed documentation for the lyrics extractor application built using tkinter and lyricsgenius:

---

## Lyrics Extractor Documentation

### Overview
Flood-Lyrics Extractor is a Python application that retrieves song lyrics from Genius using the lyricsgenius library and presents them in a simple graphical user interface (GUI) built with tkinter.

### Features
- *User-Friendly GUI*: Allows users to input an artist's name and song title to fetch lyrics.
- *Lyrics Extraction*: Retrieves song lyrics from Genius.
- *Error Handling*: Provides feedback if the lyrics cannot be found or if there are missing inputs.

### Requirements
- Python 3.x
- tkinter library (usually included with Python installations)
- lyricsgenius library
- Genius API token

### Installation

1. *Install Python 3.x* if it is not already installed.
2. **Install lyricsgenius library**:
   sh
   pip install lyricsgenius
   
3. *Get a Genius API token*: Sign up at [Genius API](https://genius.com/api-clients) and generate a token.

### Usage

1. *Set the Genius API Token*: Replace the placeholder in the api_token variable with your actual Genius API token.
   python
   api_token = "your_genius_api_token"  # Replace with your Genius API token
   
2. *Run the Script*: Execute the script to launch the GUI.
3. *Input Artist and Song*: Enter the artist's name and the song title in the respective fields.
4. *Extract Lyrics*: Click the "Extract Lyrics" button to retrieve and display the lyrics.

### Components

#### GUI Elements
- *Root Window*: The main application window.
- *Labels*: Indicate where to enter the artist and song title.
- *Entry Widgets*: Allow users to input the artist's name and song title.
- *Extract Button*: Triggers the lyrics extraction process.
- *Result Text Box*: Displays the retrieved lyrics or error messages.

#### Functions

##### get_lyrics(api_token, artist, song)
Fetches the lyrics for a given song by an artist using the Genius API.
- *Parameters*:
  - api_token (str): Genius API token.
  - artist (str): Artist's name.
  - song (str): Song title.
- *Returns*:
  - Lyrics of the song if found, otherwise an error message.

##### extract_lyrics()
Handles the button click event to extract lyrics.
- Retrieves inputs from the entry fields.
- Calls get_lyrics to fetch the lyrics.
- Displays the lyrics or error message in the result text box.

### Error Handling
- *Empty Fields*: Displays an error message if any input field is left empty.
- *API Errors*: Catches exceptions during the API call and displays an appropriate error message.

### Example
1. Set the API token:
   python
   api_token = "your_genius_api_token"
   
2. Run the script:
   sh
   python flood_lyrics_extractor.py
   
3. Enter "Taylor Swift" in the Artist field and "Love Story" in the Song field.
4. Click "Extract Lyrics" to retrieve and display the lyrics.

### Customization
To change the window size or background color, modify the window_width, window_height, and window.configure(bg="color") settings.

### Conclusion
Lyrics Extractor provides a simple interface to fetch and display song lyrics using the Genius API. It demonstrates basic GUI design with tkinter and API integration with lyricsgenius.

---

