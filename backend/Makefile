## The Makefile includes instructions on environment setup and lint tests
# Create and activate a virtual environment
# Install dependencies in requirements.txt
# Dockerfile should pass hadolint
# app.py should pass pylint
# (Optional) Build a simple integration test

setup:
	# Create python virtualenv & source it
	# source ~/.backend/bin/activate
	python3 -m venv ~/.backend

env:
	# Show information about environment
	which python3
	python3 --version
	which pylint


install:
	# This should be run from inside a virtualenv
	pip install --upgrade pip &&\
	pip install -r requirements.txt

test:
	# Additional, optional, tests could go here
	#python -m pytest -vv --cov=myrepolib tests/*.py
	#python -m pytest --nbval notebook.ipynb

lint:
	#See local hadolint install instructions:   https://github.com/hadolint/hadolint
	#This is linter for Dockerfiles
	hadolint Dockerfile
	#This is a linter for Python source code linter: https://www.pylint.org/
	#This should be run from inside a virtualenv
	#pylint --disable=R,C,W1203 app/app.py
	pylint --disable=C0114,C0116,C0103,W1514,R1732,C0103,W1514,R1732,C0304,C0411,W0702,E0401,R1710  app.py

all: install lint test