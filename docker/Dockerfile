# Base image
FROM python:3.12-slim

# Working directory
WORKDIR /app

# Copy requirements from repo root to /app
COPY requirements.txt /app/requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copy project files
COPY . .

# Start application
CMD ["python", "app.py"]
