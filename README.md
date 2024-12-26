# ChatLink Client 🔗✨

Welcome to **ChatLink Client**! This is a lightweight Java client application designed to connect to the [ChatLinkServer](https://github.com/om1cael/ChatLink-Server) for global and private chat communication.

> [!NOTE]  
> This application is not meant to be used for real communication. See [ChatLinkServer README](https://github.com/om1cael/ChatLink-Server/blob/main/README.md)

## Features 🌟

- **User Identification**: Unique client IDs generated using usernames.
- **Real-Time Messaging**: Send and receive messages in real-time.
- **Global and Private Chat Support**: Communicate globally or connect privately with other users.
- **Cross-Platform Compatibility**: Works on any system with Java installed.

## Getting Started ⚙️

Follow these steps to get the ChatLink Client running on your machine.

### Prerequisites

Ensure you have the following installed:

- **Java Development Kit (JDK)**: Version 11 or higher.
- **Gradle**: For build automation.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/om1cael/ChatLinkClient.git
   ```

2. Navigate to the project directory:
   ```bash
   cd ChatLinkClient
   ```

3. Build the project using Gradle:
   ```bash
   ./gradlew build
   ```

4. Run the client application:
   ```bash
   ./gradlew run --args="<server-ip> <server-port>"
   ```
   Replace `<server-ip>` and `<server-port>` with the ChatLinkServer's IP and port.

## Usage ⚡

### Setting Up
- Upon running the client, you will be prompted to enter a **username**.
- A unique ID will be generated based on your username.
- Share your ID with other users to initiate private chats.

### Sending Messages
- **Global Messages**: Type your message and hit `Enter` to send it globally.
- **Private Chat**: Use the `/chat <ID>` command to initiate a private conversation with a specific user.

### Sample Commands
- `/chat 123e4567-e89b-12d3-a456-426614174000` - Start a private chat with the specified ID.
- `<message>` - Send a message globally or privately depending on the chat state.

## Architecture Overview 🎨

### Key Components

1. **SocketChannel**:
   - Manages client-to-server communication.

2. **UUID Generation**:
   - Generates unique IDs for clients based on their usernames.

3. **ExecutorService**:
   - Handles concurrent tasks for sending and receiving messages.

4. **ByteBuffer**:
   - Efficiently processes message data.

## Example Interaction

1. **Startup**:
   ```
   Name: JohnDoe
   To connect with your friend, share your ID: 123e4567-e89b-12d3-a456-426614174000
   ```

2. **Global Messaging**:
   ```
   JohnDoe: Hello everyone!
   ```

3. **Private Chat**:
   ```
   /chat 123e4567-e89b-12d3-a456-426614174001
   You are now in a private chat with 123e4567-e89b-12d3-a456-426614174001
   ```

## Contributing 🌱

We welcome contributions! Here’s how you can get involved:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature Y"
   ```
4. Push your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## License ⚖️

This project is licensed under the MIT License. See the `LICENSE` file for details.

> Made with ❤️ and Java.

