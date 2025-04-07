# Mood-based-song-detection-using-facial-expression-

Facial Expression Mood Song Generator
A web application that detects user facial expressions or accepts manual mood input to recommend songs tailored to the user's emotional state.

Features

Facial Expression Detection: Uses the device camera to analyze facial expressions and detect the user's mood
Manual Mood Selection: Alternative option to select mood via buttons or free text input
Intelligent Mood Mapping: Maps various mood descriptions to core emotional categories
Personalized Song Recommendations: Suggests songs based on detected or selected mood
Interactive Music Player: Simple music player interface for playback control

Technology Stack

Frontend: HTML5, CSS3, JavaScript (Vanilla)
UI Design: Custom CSS with responsive design
Media Handling: HTML5 Canvas and MediaDevices API
Audio: HTML5 Audio API

Setup Instructions

Clone the repository to your local machine:
bashCopygit clone https://github.com/yourusername/mood-song-generator.git
cd mood-song-generator

Open index.html in your web browser.
Note: For local development, you may need to run a local web server due to camera access restrictions in some browsers when using the file:// protocol.
If using a local web server:
bashCopy# Using Python 3
python -m http.server 8000

# Then open http://localhost:8000 in your browser


Usage Guide

Start Camera Detection:

Click "Start Camera" to enable facial expression detection
Allow camera access when prompted by your browser
Wait for the app to analyze your expression and display your detected mood


Manual Mood Input (Alternative):

Click "Or enter your mood manually" to expand the manual entry section
Either select a mood button or type your mood in the text field


Generate Song Recommendation:

Click "Find My Song" to receive a personalized song recommendation
The app will display song details and a playback interface


Playback Controls:

Use play/pause button to control song playback
Track progress is displayed in the progress bar



Important Notes for Developers

Song Database: The current implementation uses a static songDatabase object. In a production environment, this should be replaced with a proper backend API or database.
Audio Files: Replace the example audio sources with legitimate, licensed audio files for a production application.
Face Detection: The current implementation simulates facial expression detection. For a production app, integrate a proper facial recognition library such as:

face-api.js
TensorFlow.js with the face-landmarks-detection model
A cloud provider's facial recognition API



Customization
Adding New Moods
To add new mood categories:

Add the new mood to the songDatabase object:
javascriptCopynewMood: [
    { title: "Song Title", artist: "Artist Name", src: "path/to/audio.mp3", cover: "path/to/cover.jpg" },
    // Add additional songs
]

Add mappings for related terms in the moodMap object:
javascriptCopy"related-term-1": "newMood",
"related-term-2": "newMood"

Add an emoji for the new mood in the moodEmojis object:
javascriptCopy"newMood": "😎"


Styling
The application uses custom CSS with a purple gradient background. To modify the theme:

Edit the background property in the body selector in the CSS section
Adjust button colors in the .camera-btn and .generate-btn selectors
Modify the song player appearance in the .result-section and related selectors

Credits

Developed by Karthik Ganesan 
Icons and design inspiration from Google 
Sample placeholder images provided by placeholder.com

Future Enhancements

Integration with music streaming services API
User accounts to save favorite songs and mood history
More advanced facial expression recognition
Mobile app version with native camera integration
Social sharing features
