# Gaming Session Logger (Wireless)
A project for tracking and maintaining player stats using a wireless logging device built on a Raspberry Pi. 
While designed for a laser maze, it can be adapted for other physical gaming spaces such as escape rooms, or similar environments. 
The system logs session activity, calculates points based on performance, and provides a web interface to view and manage player profiles and statistics.


## 🔹 Overview

- **Client**: Runs on the Raspberry Pi and sends session data (player code, start & end times) to the server.
- **Server**: Receives session data, calculates duration and points, and updates the MongoDB database.
- **Web Application**: Built with Flask, provides a frontend for players to view profiles, points, and session stats. Includes pages like login, registration, gallery, FAQ, and contact form.

The system allows for:
- Tracking player sessions wirelessly
- Automatic points calculation based on task completion time
- Viewing and managing player profiles via a web interface


## 📂 Repository Structure

- `client.py`  
  Python script running on the Raspberry Pi to log player sessions and send data to the server.

- `server2.py`  
  Server-side Python script that receives session data, calculates points, and updates the MongoDB database.

- `webapp/`  
  Flask-based web application to view player profiles, stats, and other related pages.
  
  - `web2.py` – Main Flask application script.  
  - `templates/` – HTML templates for web pages.  
  - `static/img/` – Images used in the web application.  
  - `description` – Additional description files for the web app.


## 🔹 Dependencies

- Python 3.x  
- Flask  
- PyMongo  
- MongoDB  
- Yagmail (for email contact form)  


## 🔹 How it Works

1. Player starts a gaming session, enters their player code on the client.  
2. Client sends the start and end timestamps to the server.  
3. Server calculates session duration and awards points based on completion time.  
4. Player stats are updated in MongoDB.  
5. Web interface allows players to register, login, and view their stats.
