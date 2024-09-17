# personal_assistant

1. HTML (Structure of the Web Page):
   
The HTML provides the skeleton for the project. It sets up a basic webpage where the user can interact with the virtual assistant.

Key Elements:
Logo: A company or assistant-specific logo (logo.png), which appears at the top of the page.
Main Heading: Introduces the assistant with the name "Shifra" and specifies that it's a virtual assistant. This heading is dynamic, so the name and role can be styled individually.
Voice GIF: This image is hidden by default and is shown when the assistant is actively listening.
Microphone Button: A clickable button with a microphone icon that triggers voice recognition. When clicked, it starts listening for voice commands from the user.
JavaScript Link: The page is linked to an external JavaScript file (app.js), which provides the logic for voice interaction.



2. CSS (Styling of the Web Page):
   
The CSS defines how the web page looks and feels. It is used to make the page visually appealing by providing layout control, colors, fonts, and animations.

Key Features:
Background and Layout: The webpage has a black background, and elements like the logo, heading, and button are centered on the screen. This is achieved using Flexbox, making the page responsive and well-aligned.
Fonts and Colors:
The text is styled with custom fonts (Protest Guerrilla) and different colors for the assistant's name ("Shifra") and the virtual assistant title.
The button uses a gradient background that transitions between two colors, giving it a modern look.
Button Hover Effects: When hovering over the microphone button, the shadow intensifies, and the letters have a slight animation, creating a sense of interactivity.
Voice GIF Visibility: The GIF (representing the assistant listening) is hidden by default and only appears when voice recognition starts.




3. JavaScript (Functional Core of the Project):
   
The JavaScript file (app.js) provides the main functionality of the voice assistant. It uses Web APIs like Speech Recognition and Speech Synthesis to interact with the user.

Key Functionalities:
Speech Synthesis (Speaking Function):

The speak() function converts text into speech using the browser’s speech synthesis capabilities. It takes a string as input and speaks it aloud with predefined settings for rate, pitch, and volume.
Example: When the user says "what's the time?", the assistant will speak the current time.
Greeting Function (wishMe()):

This function greets the user based on the time of day:
"Good Morning" for early hours (0-12).
"Good Afternoon" for the afternoon (12-16).
"Good Evening" for later in the day (16 and above).
The greeting is spoken aloud when the webpage is loaded.
Speech Recognition (Listening to User):

The SpeechRecognition API is used to capture voice commands from the user.
The recognition starts when the user clicks the microphone button (btn), and the recorded speech is processed into text.
Command Handling (takeCommand()):

After receiving a voice command, this function checks for specific phrases and executes the corresponding actions.
Some common commands and responses:
"Hello" or "Hey": Responds with a greeting, e.g., "Hello sir, what can I help you with?"
"Who are you?": Introduces the assistant by saying, "I am a virtual assistant, created by Abhishek Kumar."
"Open YouTube/Google/Instagram": Opens these websites in a new browser tab.
"What's the time?": Tells the current time using the toLocaleString() method.
"What's the date?": Tells the current date.
If a command is not recognized, it performs a Google search for the phrase.
Button Interaction:

Clicking the button starts voice recognition.
While listening, the button is hidden, and the voice GIF is shown to indicate that the assistant is active.
After processing the voice command, the button is restored, and the GIF is hidden.




How the Project Works:

Page Load:

When the page is loaded, the assistant greets the user based on the current time of day (morning, afternoon, or evening).
User Interaction:

The user clicks on the microphone button, triggering the voice recognition process.
The assistant listens for the user’s speech and converts it into text.
Command Execution:

Depending on what the user says, the assistant performs predefined actions like opening web pages, telling the time, or answering questions.
If the assistant doesn’t understand the command, it performs a Google search for the phrase.
Visual Feedback:

The assistant shows visual feedback when it is listening (via the voice GIF) and responds with synthesized speech for certain commands.




Project Files:

index.html: Defines the structure of the page and links to the external CSS and JavaScript files.\n
style.css: Provides the styles for the layout, colors, fonts, and animations.
app.js: Implements the logic for voice commands, speech synthesis, and interactions with external resources.
