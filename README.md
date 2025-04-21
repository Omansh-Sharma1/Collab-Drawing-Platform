# Collaborative Drawing Platform

## Overview

Welcome to the Collaborative Drawing Platform!

This project is a real-time, interactive drawing application built using **Node.js**, **Express**, and frontend web technologies (**HTML**, **CSS**, **JavaScript**). It allows multiple users to draw on a shared canvas simultaneously, offering a seamless collaborative experience using WebSockets.

> ⚠️ **Note:** Persistent storage using MongoDB is a planned feature but is **not yet implemented**.

---

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [About HTML5 Canvas](#about-html5-canvas)
- [Acknowledgement](#acknowledgement)
- [Contributing](#contributing)
- [License](#license)
- [Submission Info](#submission-info)

---

## Features

- ✅ **Real-Time Collaboration:** Multiple users can draw on the same canvas using WebSockets.
- ✅ **Room-Based Sessions:** Users can create or join unique rooms for focused collaboration.
- ✅ **Canvas Drawing Tools:** Includes multiple colors and drawing modes.
- ✅ **Responsive Design:** Works smoothly on desktop, tablet, and mobile.
- 🔄 **Future Support for Saving Work:** Plans to implement MongoDB for drawing storage.

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

- ✅ **Node.js** (v12.x or higher)
- ✅ **npm** (v6.x or higher)
- ⚙️ *(Optional for future use)* MongoDB (local or hosted like MongoDB Atlas)

---

### Installation

#### 📁 Clone the Repository:

```bash
git clone https://github.com/your-username/collaborative-drawing-platform.git
cd collaborative-drawing-platform
```

#### 📦 Install Server Dependencies:

```bash
cd server
npm install
```

#### 🛠️ Set Up Environment Variables (optional - future use):

Create a `.env` file in the server directory with:

```ini
MONGO_URI=your-mongodb-uri
JWT_SECRET=your-secret-key
```

#### 🚀 Run the Server:

```bash
cd server
npm start
```

#### 🌐 Open the Frontend:

Simply open the `index.html` in the frontend folder using your browser or launch using Live Server in VS Code.

## Usage

- 🎨 **Create/Join Room:** Enter a room ID to collaborate with others in real time.
- 🖍️ **Draw Together:** All changes sync across connected users.
- 🎨 **Select Color:** Use the toolbar to pick your color.
- 🧹 **Clear Canvas:** Clear the drawing area for all users in that room.

## Technologies Used

### Frontend
- HTML5
- CSS3
- JavaScript
- Socket.io-client
- HTML5 Canvas API

### Backend
- Node.js
- Express
- Socket.io
- (Planned) MongoDB, Mongoose

## About HTML5 Canvas

The `<canvas>` element in HTML5 allows drawing graphics via JavaScript. It's different from regular HTML because it doesn't use the DOM for rendering—making it ideal for real-time drawing.

**Why Canvas?**
- Draws directly onto a bitmap area
- Enables real-time and free-hand drawing
- Supports complex rendering (shapes, images, paths)
- Handles mouse/touch input naturally
- Lightweight and fast for collaborative drawing

💡 In this project, we use:

```js
const canvas = document.getElementById('canvas');
const context = canvas.getContext('2d');
```

to draw and emit real-time data over sockets.

## Contributing

We welcome contributions! Follow these steps:

```bash
# Step 1: Fork the repo

# Step 2: Create a new branch
git checkout -b feature/your-feature

# Step 3: Make your changes
git commit -m "Added new feature"

# Step 4: Push changes
git push origin feature/your-feature

# Step 5: Create a pull request
```

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
