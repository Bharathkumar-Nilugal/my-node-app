# My Node.js App - CI/CD Pipeline Example A simple Node.js web application with automated CI/CD pipeline using GitHub Actions and Docker.
## Features 
Express.js web server Automated testing with Jest Docker containerization CI/CD pipeline with GitHub Actions Automatic Docker image builds and pushes to DockerHub 

### Project Structure 
```
my-node-app/
├── .github/
│ └── workflows/
│ └── main.yml # GitHub Actions workflow
├── test/
│ └── app.test.js # Test files
├── index.js # Main application file
├── package.json # Node.js dependencies
├── Dockerfile # Docker configuration
├── .dockerignore # Docker ignore rules
├── .gitignore
└── README.md # This file
```
# Prerequisites 
Node.js 18+ 
Docker GitHub account
DockerHub account 
### Local Development
#### Clone the repository: git clone https://github.com/Bharathkumar-Nilugal/my-node-app.git
```
cd my-node-app
```
Install dependencies:
```
#bash
npm install
```
Run tests:
```
#bash
npm test
```
Start the application:
#bash 
```
npm start
```
# The app will be available at http://localhost:3000
#Docker Usage 
#Build the image:
```
#bash
docker build -t my-node-app .
```
#Run the container:
#bash 
docker run -p 3000:3000 my-node-app 
```
#Using the published image:
```
#bash 
docker pull YOUR_DOCKERHUB_USERNAME/my-node-app:latest 
docker run -p 3000:3000 YOUR_DOCKERHUB_USERNAME/my-node-app:latest 

## CI/CD Pipeline 
## This project uses GitHub Actions for continuous integration and deployment:
#Workflow Triggers: --> On push to main branch: Automatically runs tests, builds Docker image, and pushes to DockerHub 
#Pipeline Steps: Test:
Runs Jest test suite Build: 
Creates Docker image using Dockerfile Push: 
Pushes image to DockerHub with latest and commit SHA tags
#Required Secrets: DOCKERHUB_USERNAME: Your DockerHub username DOCKERHUB_TOKEN: DockerHub access token 
# API Endpoints 
```
GET / - Returns JSON response: {"ok": true, "message": "Hello from my-node-app"}
```
### Testing Run the test suite:
```
 #bash
npm test
```
### Deployment The application is automatically deployed to DockerHub on every push to the main branch. 
You can find the latest image at: https://hub.docker.com/r/YOUR_DOCKERHUB_USERNAME/my-node-app
Contributing Fork the repository Create a feature branch Make your changes Add tests for new functionality Ensure all tests pass Submit a pull request 
# License
## MIT License - see LICENSE file for details text 
### Navigate to your project directory
```
cd my-node-app
```
# Check the current status
```
git status
```
### Add all new files (README.md and workflow files)
```
git add .
```
### Commit the changes
```
git commit -m "Add complete project with CI/CD pipeline, tests, Docker support, and documentation"
```
### Push to GitHub
```
git push origin main
```
### Verify the push was successful
```
git log --oneline -3
Verification Steps After Push
```

### Check GitHub Repository:

Go to your GitHub repo in browser

Verify all files are present

Check the README.md renders properly

# Monitor GitHub Actions:

1.Click on "Actions" tab in your repo
2.You should see a workflow running (or completed)
3.Check that both "test" and "build-and-push" jobs pass
4.Verify DockerHub:
5.Go to hub.docker.com

### Check your repository has new tags:

latest

Commit SHA (e.g., a1b2c3d)

Test the Deployed Image:

#bash
# Pull and run the image from 
```
docker pull YOUR_DOCKERHUB_USERNAME/my-node-app:latest
docker run -d -p 3000:3000 YOUR_DOCKERHUB_USERNAME/my-node-app:latest
```
# Test the running container
```
curl http://localhost:3000
Should return: {"ok":true,"message":"Hello from my-node-app"}
```
## Complete File Structure Verification
Before pushing, ensure your project has this structure:

```
my-node-app/
├── .github/
│   └── workflows/
│       └── main.yml
├── test/
│   └── app.test.js
├── .dockerignore
├── .gitignore
├── Dockerfile
├── README.md
├── index.js
└── package.json
```
### Quick Final Commands
#### One-liner to add, commit, and push everything
```
git add . && git commit -m "Complete CI/CD pipeline setup with documentation" && git push origin main
```
### Your repository is now complete with:
```
✅ Working Node.js application

✅ Automated tests

✅ Docker configuration

✅ GitHub Actions CI/CD pipeline

✅ Comprehensive documentation

✅ Automated Docker image deployment
```
