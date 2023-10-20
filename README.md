# Developing a Simple Webserver
Name: salini
dept: IT

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
Type your code here
```
content="""
<html>
<head>
</head>
<body>
<h1>welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_header()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.server_forever()
```
# OUTPUT:

# RESULT:

The program is executed succesfully
