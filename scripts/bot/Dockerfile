FROM python:3.9-slim

# Install dependencies
RUN apt-get update && apt-get install -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the script
COPY . .

# Set environment variables
ENV PYTHONUNBUFFERED=1

# Run the script
CMD ["python", "combined-script.py"] 