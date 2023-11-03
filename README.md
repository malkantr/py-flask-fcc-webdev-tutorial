# Introduction - Web Development with Python Tutorial – Flask & Dynamic Database-Driven Web Apps by FreeCodeCamp

## jovian-careers-website

Instructor & Notes : Aakash N S

Learn how to develop Dynamic Database-Driven Web Apps with Python, Flask, and MySQL. This course is broken up into two parts. In part one, you will learn how to build and deploy a site using the Flask Python web framework. In part two, you will connect the Flask application from the first part to a cloud MySQL database and learn how to deploy a production-ready database-driven web application.

- https://youtu.be/yBDHkveJUf4?si=Z6dCAa0RbiTUeFhu
- https://jovian.com/aakashns/web-development-with-python
- https://jovian.com/aakashns/database-driven-web-applications

## ⭐️ Contents ⭐️

Part 1

- ⌨️ (0:00:00) Introduction
- ⌨️ (0:02:07) 1.1 Project Setup & Flask Basics
- ⌨️ (0:22:25) 1.2 Building Web Pages using HTML
- ⌨️ (0:40:57) 1.3 Styling with CSS & Bootstrap
- ⌨️ (1:08:25) 1.4 Dynamic Data using Templates
- ⌨️ (1:27:22) 1.5 Deploying to the Cloud with Render
- ⌨️ (1:42:39) 1.6 Functional and Aesthetic Improvements
- ⌨️ (1:58:44) 1.7 Summary & Future Work

Part 2

- ⌨️ (2:04:19) Database-Driven Web Applications
- ⌨️ (2:07:24) 2.1 Project Setup & Deployment
- ⌨️ (2:21:44) 2.2 Cloud MySQL Database Setup
- ⌨️ (2:36:20) 2.3 DB Connection with SQLAlchemy
- ⌨️ (2:56:22) 2.4 Display DB Data on Web Page
- ⌨️ (3:20:04) 2.5 Dynamic Database-Driven Pages
- ⌨️ (3:49:23) 2.6 HTML Form for Applications
- ⌨️ (4:15:37) 2.7 Saving Applications to DB
- ⌨️ (4:26:23) 2.8 Summary & Future Work

- ⌨️ (4:37:50) Conclusion


## Replit.com setup
Run command python app.py

## Setup & Tools

```bash
pip install flask
```

- render.com : hosting

```
pip install -r requirements.txt
gunicorn app:app
```

- mailtolink.me : create mail link template

- PlanetSchale : mysql on cloud 
  - https://planetscale.com/

- SQLAlchemy : ORM
  ```bash
  pip install pymysql
  pip install sqlalchemy==1.4.23
  ```

 

## DB Scripts

```sql
CREATE TABLE jobs(
    id INT NOT NULL AUTO_INCREMENT,
    title VARCHAR(120) NOT NULL,
    location VARCHAR(120) NOT NULL,
    salary INT,
    currency VARCHAR(10),
    responsibilities VARCHAR(2000),
    requirements VARCHAR(2000),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    PRIMARY KEY (id)
);

CREATE TABLE applications (
  id INT NOT NULL AUTO_INCREMENT,
  job_id INT NOT NULL,
  full_name VARCHAR(250) NOT NULL,
  email VARCHAR(250) NOT NULL,
  linkedin_url VARCHAR(500) NOT NULL,
  education VARCHAR(2000),
  work_experience VARCHAR(2000),
  resume_url VARCHAR(500),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (id)
);

```

## Static Data

```python
  
JOBS = [
      {
          'id': 1,
          'title': 'Data Analyst',
          'location': 'Bengaluru, India',
          'salary': 'Rs. 10,00,000'
      },
      {
          'id': 2,
          'title': 'Data Scientist',
          'location': 'Delhi, India',
          'salary': 'Rs. 15,00,000'
      },
      {
          'id': 3,
          'title': 'Frontend Engineer',
          'location': 'Remote'
      },
      {
          'id': 4,
          'title': 'Backend Engineer',
          'location': 'San Francisco, US',
          'salary': '$120,000'
      },
  ]

```


## TODO

validate inputs, sanitize before querying the database
use capthca