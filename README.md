# FastAPI-Blog-API
A RESTful API built with FastAPI and PostgreSQL, allowing CRUD operations on blog posts.

# Features
Retrieve all posts or a specific post by ID.
Create, update, and delete posts.
Get the latest post.

# Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install fastapi psycopg2-binary uvicorn

# Configure PostgreSQL:

** Create a database .

** Use the following table schema:

CREATE TABLE posts (

    id SERIAL PRIMARY KEY,
    
    title VARCHAR(255),
    
    content TEXT,
    
    published BOOLEAN DEFAULT TRUE,
    
    created_at TIMESTAMP DEFAULT NOW()
    
);

**Update database credentials in the code.

# Run the app:

uvicorn main:app --reload

# API Endpoints
 GET /posts: Fetch all posts.
 
 POST /posts: Create a new post.
 
 GET /posts/{id}: Fetch a post by ID.
 
 GET /posts/latest: Fetch the most recently created post.
 
 PUT /posts/{id}: Update a post.
 
 DELETE /posts/{id}: Delete a post.

# Notes
Ensure your database is running before starting the app.
Activate the virtual environment (venv) for all commands.
