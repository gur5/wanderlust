1. Clone or fork the repo

       git clone https://github.com/gur5/wanderlust.git
2. Navigate to the backend directory

       cd /backend
3. Install require dependencies

        npm i # if not install goto https://nodejs.org/en/download
   
4. Setup your mongodb database

       https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-red-hat/
5. Import sample data

>To populate the database with sample posts, you can copy the content from the backend/data/sample_posts.json file and insert it as a document in the wanderlust/posts collection in your local MongoDB database using either MongoDB Compass or mongoimport.
   

          mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray
7.  
