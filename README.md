Titanic Dataset: PostgreSQL + Streamlit App

This is a web app that reads the Titanic passenger data from a PostgreSQL database. It shows charts, lets you filter the data, and lets you practice SQL. It also has a short quiz on PostgreSQL and Streamlit.

Tech Stack
Python
Streamlit
PostgreSQL
psycopg2
pandas
Plotly
Matplotlib
Real-World Problem It Solves

Many beginners learn SQL from books and never see it work with a real app. It is also hard to know if your queries give the right answer. This project connects a real database to a simple web page. A learner can look at the Titanic data, write SELECT queries, and see the results at once. The SQL Lab only allows read-only queries, so the data stays safe. It is a learning tool, not a production system.

How to Run
Clone the repo.
bash
git clone https://github.com/Hemasree1738/Titanic_dataset_streamlit_app.git
Go into the project folder.
bash
cd Titanic_dataset_streamlit_app
Install the libraries.
bash
pip install streamlit pandas psycopg2-binary plotly matplotlib
Set up PostgreSQL. The app expects a schema named titanic_project with two tables: passengers and titanic_staging. Both tables should hold the Titanic data (891 rows).
Add your database details. Create the file .streamlit/secrets.toml and write this inside:
toml
[db]
host = "localhost"
port = 5432
dbname = "titanic_db"
user = "titanic_app"
password = "your_password"

You can also use environment variables instead: PGHOST, PGPORT, PGDATABASE, PGUSER, PGPASSWORD, and optionally PGSSLMODE.

Run the app.
bash
streamlit run app.py
Author

Made by Hemasree Randhi.

Contributing

This project is open to contributions. If you have an idea or find a bug, feel free to fork the repo and open a pull request.
