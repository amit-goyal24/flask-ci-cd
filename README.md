In this project :
I am using Github, Docker ,and jerkins for showing the ci/cd pipelining working on the browser.  
After completing these code in Vs code and making files then I pushed these files on Github.
I am going to local host port 8080     "http://localhost:8080"

Now i follows for steps given below for making pipeline :-


Open Jenkins: http://localhost:8080

Click New Item

Name: flask-windows-ci-cd

Choose: Pipeline

Scroll down to Pipeline Script from SCM

SCM: Git

Repo URL:

Local: file:///C:/Users/<YourUsername>/path/to/flask-ci-cd-windows

Or GitHub URL

Credentials: only needed if it's private repo

Branch: main or master

Save

🧪 5. Run the Pipeline
Click Build Now

Open Console Output

Check for:
Docker build success
Container starts on port 5000


Now go to your browser and reached to the "http://localhost:5000"   And then 

 you successfully see "Hello, Local CI/CD with Jenkins on Windows! "



* This is showing the success of  ci/cd pipeline * 



