
# Codtech_Real_Time_Chat_Application
COMPANY: CODTECH IT SOLUTIONS
NAME: ASMITA RAJENDRA BANDAL 
INTERN ID: CT08JIO 
DOMAIN: FRONT END DEVELOPMENT 
BATCH-DURATION: 5 JANUARY TO 5 FEBRUARY
MENTOR: NEELA SANTOSH KUMAR

WebSocket Server Implementation
A simple WebSocket server implementation using Express.js and Socket.IO that supports room-based messaging.

Features
WebSocket connection handling
Room-based messaging support
CORS enabled for frontend integration
Express.js REST API endpoints
Prerequisites
Node.js (v14 or higher)
npm or yarn
Installation
Clone the repository
Navigate to the server directory
cd server
Install dependencies
npm install
Dependencies
express
socket.io
cors
http
Configuration
The server runs on port 3000 by default and accepts connections from:

Frontend URL: http://localhost:5173 (Vite's default dev server)
Running the Server
node index.js
WebSocket Events
Server Events
connection: Handles new client connections
disconnect: Handles client disconnections
Client Events
message: Receives messages from clients
Parameters:
message: Message content
room: Room identifier
Emitted Events
replay: Broadcasts messages to room members
API Endpoints
GET /: Returns server status
Example Usage
// Client-side connection
const socket = io('http://localhost:3000');

// Send message to a room
socket.emit('message', {
    message: 'Hello Room!',
    room: 'room1'
});

// Listen for messages
socket.on('replay', (message) => {
    console.log('Received:', message);
});

Output:

