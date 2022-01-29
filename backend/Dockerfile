FROM python:3.6.10

## Step 1:
# Create a working directory
WORKDIR /app
## Step 2:
# Copy source code to working directory
COPY . app.py /app/

## Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip3 install --no-cache-dir --upgrade pip &&\
    pip3 install --no-cache-dir --trusted-host pypi.python.org -r requirements.txt

## Step 4:
# Expose port 80
## Step 5:
EXPOSE 5050
# Run app.py at container launch
CMD ["python", "app.py"]