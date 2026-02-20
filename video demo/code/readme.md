# CODE
@app.route('/')
def home():
    return render_template('index.html')

@app.route("/contact")
def contact():
    return render_template("contact.html")


if __name__=='__main__':
    app.run(debug=True)

    #WEBSITE
    https://127.0.0.1:5000
