# Quick-fed-app
Quick Feed App
This is a simple, cloud-connected mobile application built using MIT App Inventor. It allows users to quickly save "posts" (short thoughts or phrases) to a central database and then retrieve those posts later. The app leverages Text-to-Speech technology to read the post content aloud upon selection.
This project demonstrates proficiency with: Cloud data storage using the CloudDB component (Firebase Realtime Database), unique data tagging using the Clock component for timestamps, basic UI/UX for saving, refreshing, and retrieving content, and accessibility features using the Text-to-Speech component.
How to Use the App
The "Quick Feed App" is designed for simple, one-touch interaction for posting and listening back to your saved thoughts.
1. Posting a Thought
This function saves your message to the cloud database.
To post, first, tap the TextBox_Post field. The keyboard will appear. Type your message or phrase (your "post"). Then, tap the Post button (or Button_Post). The message is saved to the Firebase database, and the text box immediately clears, ready for a new post.
2. Refreshing and Viewing the Feed
To see what you (or others) have posted, you must refresh the list.
To refresh, tap the Refresh Feed button (Button_Refresh). The app sends a request to the cloud database for a list of all posts. The ListView1 will then populate and display the unique timestamp (date and time) of every post that is currently saved in the database.
3. Reading the Post Aloud
This is the main function—retrieving the saved message and having it read to you.
To listen to a post, tap any timestamp from the list displayed in ListView1. The app sends a request to the cloud database for the content associated with that timestamp. Once the app receives the message, your device's TextToSpeech1 component will instantly read the post's content aloud to you.
4. Clearing the Entire Database
⚠️ CAUTION: This button will delete all data currently stored in your section of the CloudDB, which means all posts will be permanently deleted. Use this button carefully!
To clear all posts, tap the Clear My Posts button (Button_Clear). The app sends a command to the database to remove all data from the root tag. You can tap Refresh Feed again afterward to confirm the list is empty.
