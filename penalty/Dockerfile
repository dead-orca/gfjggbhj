FROM python:3.11-slim

WORKDIR /app

# Copy requirements first for better caching
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy all application files
COPY . .

# Make start.sh executable
RUN chmod +x start.sh

# Run the bot
CMD ["python", "bot.py"]

