# Base image
FROM python:3.12-slim

# Working directory
WORKDIR /app

# Copy requirements first
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Start application
CMD ["python", "app.py"]
