dataset link: https://drive.google.com/file/d/15ujsgAL8_vhkogwlegRYfHhoEcD4EQes/view?usp=drive_link
video link : https://drive.google.com/folderview?id=1J7xjte7EcFHvFNtyb2N4ELXrmyoTuj-l

📁 Folder Structure
heart_disease_analysis/
│
├── app.py
├── templates/
│   ├── index.html
│   ├── dashboard.html
│   ├── story.html
│   ├── about.html
│   └── contact.html
├── static/
│   ├── css/
│   │   └── style.css
│   └── images/
│       └── logo.png
└── README.md

app.py
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html')

@app.route('/dashboard')
def dashboard():
    return render_template('dashboard.html')

@app.route('/story')
def story():
    return render_template('story.html')

@app.route('/about')
def about():
    return render_template('about.html')

@app.route('/contact')
def contact():
    return render_template('contact.html')

if __name__ == '__main__':
    app.run(debug=True)

templates/index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Disease Analysis</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
    <header>
        <h1>Heart Disease Analysis</h1>
        <nav>
            <a href="/">Home</a>
            <a href="/dashboard">Dashboard</a>
            <a href="/story">Story</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>
    </header>

    <section class="hero">
        <h2>Data-Driven Insights for Better Heart Health</h2>
        <p>Explore interactive dashboards and visual stories that reveal key risk factors and trends in heart disease.</p>
        <a href="/dashboard" class="btn">View Dashboard</a>
    </section>

    <footer>
        <p>© 2026 Heart Disease Analysis Project | Powered by Flask & Tableau</p>
    </footer>
</body>
</html>

templates/dashboard.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard | Heart Disease Analysis</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
    <header>
        <h1>Heart Disease Dashboard</h1>
        <nav>
            <a href="/">Home</a>
            <a href="/dashboard">Dashboard</a>
            <a href="/story">Story</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>
    </header>

    <section class="content">
        <h2>Interactive Tableau Dashboard</h2>
        <p>Explore visual insights into heart disease risk factors, demographics, and lifestyle impacts.</p>

        <div class="tableauPlaceholder" id="vizDashboard">
            <iframe src="https://public.tableau.com/views/HeartDiseaseDashboard/Dashboard1?:showVizHome=no&:embed=true"
                    width="100%" height="800px"></iframe>
        </div>
    </section>

    <footer>
        <p>© 2026 Heart Disease Analysis Project</p>
    </footer>
</body>
</html>

templates/story.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Story | Heart Disease Analysis</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
    <header>
        <h1>Heart Disease Data Story</h1>
        <nav>
            <a href="/">Home</a>
            <a href="/dashboard">Dashboard</a>
            <a href="/story">Story</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>
    </header>

    <section class="content">
        <h2>Interactive Tableau Story</h2>
        <p>Follow the narrative of heart disease analysis through data-driven storytelling.</p>

        <div class="tableauPlaceholder" id="vizStory">
            <iframe src="https://public.tableau.com/views/HeartDiseaseStory/Story1?:showVizHome=no&:embed=true"
                    width="100%" height="800px"></iframe>
        </div>
    </section>

    <footer>
        <p>© 2026 Heart Disease Analysis Project</p>
    </footer>
</body>
</html>

templates/about.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About | Heart Disease Analysis</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
    <header>
        <h1>About the Project</h1>
        <nav>
            <a href="/">Home</a>
            <a href="/dashboard">Dashboard</a>
            <a href="/story">Story</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>
    </header>

    <section class="content">
        <h2>Project Overview</h2>
        <p>This project analyzes heart disease data using Tableau and Flask to uncover key risk factors and trends. It supports healthcare professionals and policymakers in making data-driven decisions for preventive care.</p>
        <ul>
            <li>Data Source: Heart Disease Dataset</li>
            <li>Tools Used: Tableau, MySQL, Flask</li>
            <li>Visualizations: 10 unique charts and dashboards</li>
        </ul>
    </section>

    <footer>
        <p>© 2026 Heart Disease Analysis Project</p>
    </footer>
</body>
</html>

templates/contact.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact | Heart Disease Analysis</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/style.css') }}">
</head>
<body>
    <header>
        <h1>Contact Us</h1>
        <nav>
            <a href="/">Home</a>
            <a href="/dashboard">Dashboard</a>
            <a href="/story">Story</a>
            <a href="/about">About</a>
            <a href="/contact">Contact</a>
        </nav>
    </header>

    <section class="content">
        <h2>Get in Touch</h2>
        <p>For project details or collaboration, reach out via email:</p>
        <p><strong>Email:</strong> heartanalysisproject@gmail.com</p>
    </section>

    <footer>
        <p>© 2026 Heart Disease Analysis Project</p>
    </footer>
</body>
</html>

static/css/style.css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f8f9fa;
    color: #333;
}

header {
    background-color: #b71c1c;
    color: white;
    padding: 15px 0;
    text-align: center;
}

nav a {
    color: white;
    margin: 0 15px;
    text-decoration: none;
    font-weight: bold;
}

nav a:hover {
    text-decoration: underline;
}

.hero {
    text-align: center;
    padding: 60px 20px;
    background-color: #f1f1f1;
}

.btn {
    background-color: #b71c1c;
    color: white;
    padding: 10px 20px;
    text-decoration: none;
    border-radius: 5px;
}

.btn:hover {
    background-color: #d32f2f;
}

.content {
    padding: 40px;
    text-align: center;
}

footer {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 15px 0;
    margin-top: 40px;
}

README.md
# Heart Disease Analysis Web Application

This Flask-based web application integrates Tableau dashboards and stories for analyzing heart disease data.

## Features
- Interactive Tableau dashboards
- Data storytelling
- Responsive design
- Flask-based backend

## How to Run
1. Install dependencies:
   pip install flask
2. Run the app:
   python app.py
3. Open your browser and go to:
   http://127.0.0.1:5000/

This package is ready to run.
Place your Tableau Public dashboard and story links in the <iframe> sections of dashboard.html and story.html.
Then run python app.py to launch your website.
