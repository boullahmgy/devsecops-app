# Base image
FROM python:3.12-slim

# Working directory
WORKDIR /app

# Copy project files
COPY . .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Start application
CMD ["python", "app.py"]
