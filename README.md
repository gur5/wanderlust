
# Wanderlust - Your Ultimate Travel Blog 🌍✈️

WanderLust is a simple MERN travel blog website ✈ This project is aimed to help people to contribute in open source, upskill in react and also master git.

## 🎯 Goal of this project

At its core, this project embodies two important aims:

1. **Start Your Open Source Journey**: It's aimed to kickstart your open-source journey. Here, you'll learn the basics of Git and get a solid grip on the MERN stack and I strongly believe that learning and building should go hand in hand.
2. **React Mastery**: Once you've got the basics down, a whole new adventure begins of mastering React. This project covers everything, from simple form validation to advanced performance enhancements. And I've planned much more cool stuff to add in the near future if the project hits more number of contributors.

_I'd love for you to make the most of this project - it's all about learning, helping, and growing in the open-source world._

## Setting up the project locally

### Setting up the Backend

1. **Fork and Clone the Repository**

   ```bash
   git clone https://github.com/{your-username}/wanderlust.git
   ```

2. **Navigate to the Backend Directory**

   ```bash
   cd backend
   ```

3. **Install Required Dependencies**

   ```bash
   npm i # if not found goto https://nodejs.org/en/download
   ```

4. **Set up your MongoDB Database**

   **goto** https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/#std-label-install-mdb-community-ubuntu

         sudo systemctl start mongod
         sudo systemctl enable mongod
         mongod --version
         sudo systemctl status mongod
         mongosh
   - Open MongoDB Compass and connect MongoDB locally at `mongodb://localhost:27017`.

6. **Import sample data**

   > To populate the database with sample posts, you can copy the content from the `backend/data/sample_posts.json` file and insert it as a document in the `wanderlust/posts` collection in your local MongoDB database using either MongoDB Compass or `mongoimport`.

   ```bash
   mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray 
   ```

7. **Configure Environment Variables**

   ```bash
   cp .env.sample .env  # cd backend
   ```

8. **Start the Backend Server**

   ```bash
   npm start # sometime show redis error

   sudo apt update
   sudo apt install redis-server
   sudo systemctl enable redis-server
   sudo systemctl start redis-server 
   sudo systemctl status redis-server
   ```
   

   > You should see the following on your terminal output on successful setup.
   >
   > ```bash
   > [BACKEND] Server is running on port 5000
   > [BACKEND] Database connected: mongodb://127.0.0.1/wanderlust
   > ```

### Setting up the Frontend

1. **Open a New Terminal**

   ```bash
   cd frontend
   ```

2. **Install Dependencies**

   ```bash
   npm i
   ```

3. **Configure Environment Variables**

   ```bash
   cp .env.sample .env.local
   ```

4. **Launch the Development Server**

   ```bash
   npm run dev # if expose then

   npm run dev -- --host
   
   ```
5. **If database not connected**

         vi /forntend/.env.sample
<change localhost to <your_public_ip>

      cp .env.sample .env.local
   
### Setting up with Docker

1.  **Ensure Docker and Docker Compose are Installed**
    
2.  **Clone the Repository**
    
   ``` bash
    
    git clone https://github.com/{your-username}/wanderlust.git
   ``` 
3.  **Navigate to the Project Directory**
    
    ```bash
    
    cd wanderlust
    
    ```
4.  **Update Environment Variables**  - If you anticipate the IP address of the instance might change, update the `.env.sample` file with the new IP address.

5.  **Run Docker Compose**
    
    ```bash
    
    docker-compose up
    ```
    This command will build the Docker images and start the containers for the backend and frontend, enabling you to access the Wanderlust application.

