📄 Project Summary
This project showcases a complete CI/CD pipeline for a Python Flask web application, built using Jenkins, GitHub, Docker, and deployed on an AWS EC2 instance.

The workflow is fully automated:

Jenkins pulls the latest code from GitHub.

It builds a Docker image and pushes it to Docker Hub.

Then it SSHs into an EC2 server and deploys the containerized app.

With this setup, every code push triggers a fresh deployment — continuous integration and delivery at its best.

🎯 Key Benefits
🔁 Hands-Free Deployment
Your app gets updated instantly after every commit — no more manual uploading or restarting.

🐳 Docker Consistency
Say goodbye to "it works on my machine" drama. The Docker container guarantees the same environment everywhere.

☁️ Cloud Deployment Ready
Hosting on AWS EC2 mirrors real-world cloud production setups, giving you experience that actually matters.

🔐 Secure & Configurable
Uses SSH keys and Jenkins credentials securely — no hardcoded passwords or shady scripts.

📚 Career-Boosting DevOps Skills
You’ll gain real experience with industry tools like Jenkins pipelines, Docker, Git, and cloud infrastructure.

📦 Future-Proof Design
Want to scale to Kubernetes, add monitoring, or test multiple environments? This setup is ready for upgrades.







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



