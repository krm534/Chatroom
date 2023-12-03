# Chatroom Client
Java application that runs the client portion of a chatroom.

## Prerequisites
- The compatible Chatroom Server located [here](https://github.com/krm534/Chatroom-Server) must be started first for the Chatroom Client application to work correctly.
- At least Java JDK 11 must be installed to use this since JavaFX depends on this JDK version.

## How to Use?
- Enter the IP address of the Chatroom Server instance on the landing page once the client is started.
- If the connection is made correctly, you should be taken to the chatroom page where messages and images can be sent to anyone connected to the Chatroom Server instance.

## Notes
- This application works fine by just building / running the Gradle Shadow plugin's fat .jar file on a Linux-based OS. But, on Windows OS, the following command had to be used to run the application's .jar file: `java --module-path <path_to_javafx_11_sdk_lib_directory> --add-modules=javafx.base,javafx.controls,javafx.fxml,javafx.graphics,javafx.media,javafx.swing,javafx.web -jar <jar_file>`
- The client's chatroom page currently only allows for 1 image to be attached to a message.
- The message field is mandatory and the Chatroom Server will not process the request unless it is complete.
- Images that are sent by yourself or other client users are stored in the /images directory in the directory where the .jar file is run from.
- Log files are stored in the /log directory in the directory where the .jar file is run from.

## TODO
- Add update to the client's landing page UI to have checkbox for enabling TLS support so messages between client / server are encrypted.

