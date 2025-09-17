# flask-deploy-demo
Rohit Patil — simple Flask app to demonstrate CI/CD with GitHub Actions, Docker and Render.

Steps:
- Run locally with venv: (see below)
- Build Docker image and run locally
- Push to GitHub main → Actions runs tests, builds and pushes image, triggers deploy

Local:
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py

Docker:
docker build -t youruser/flask-deploy-demo .
docker run -p 5000:5000 youruser/flask-deploy-demo