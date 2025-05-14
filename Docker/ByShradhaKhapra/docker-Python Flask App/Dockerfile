# Step 1: Set the base image (Python 3.11 slim version)
FROM python:3.11-slim

# Step 2: Metadata about the image
LABEL maintainer="Ashish <ashish@example.com>"
LABEL version="1.0"
LABEL description="Flask app inside Docker container"

# Step 3: Set environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Step 4: Set the working directory in container
WORKDIR /app

# Step 5: Copy dependency file and install packages
COPY requirements.txt .

# Step 6: Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 7: Copy rest of the application code
COPY . .

# Step 8: Expose the port the app runs on
EXPOSE 5000

# Step 9: Default command to run the app
CMD ["python", "app.py"]
