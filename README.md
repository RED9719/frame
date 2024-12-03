# frame
Create a web page having two frames, Frame 1 containing links and another with contents of the 
link. When a link is clicked appropriate contents should be displayed on Frame 2. Also, insert an iframe 
in the same page.
CODE
           <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Ramanujan College - Frames Example</title>
    <style>
        body {
            margin: 0;
            padding: 0;
        }
        frameset {
            border: none;
        }
        iframe {
            width: 100%;
            height: 200px;
            border: none;
        }
        h3 {
            text-align: center;
        }
        ul {
            list-style-type: none;
            padding: 0;
            text-align: center;
        }
        ul li {
            margin: 10px 0;
        }
        ul li a {
            text-decoration: none;
            color: #007bff;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>About Ramanujan College</h1>
    <p>Welcome to Ramanujan College. We are dedicated to providing quality education and fostering research in various fields.</p>
</body>
    <frameset cols="30%,70%">
        <frame name="frame1" srcdoc="
        
    
        <body>
            <h3>Ramanujan College Links</h3>
            <ul>
            
                <li><a href="#" onclick="parent.frames['frame2'].location='about.html'">About Us</a></li>
                <li><a href="#" onclick="parent.frames['frame2'].location='courses.html'">Courses</a></li>
                <li><a href="#" onclick="parent.frames['frame2'].location='contact.html'">Contact Us</a></li>
                
            </ul>
        </body>
        
        ">

        <!-- Frame 2: Content -->
        <frame name="frame2">
    </frameset>
    <noframes>
        <body>
            <h1>This page requires frames.</h1>
        </body>
    </noframes>

    
    <body>
        <h1>Welcome to the Iframe Section</h1>
        <p>This section is displayed inside an iframe for additional information.</p>
    </body>
    
</body>
</html>
