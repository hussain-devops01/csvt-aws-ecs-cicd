# Use an official Python runtime as a parent image
FROM python:3.11.4

# Set the working directory in the container
WORKDIR /fast_api

# Copy the requirements file into the container
COPY requirements.txt .

# Install Python dependencies
RUN pip install  psycopg2
RUN pip install --no-cache-dir -r requirements.txt
RUN pip install pydantic_settings
RUN pip install fastapi==0.104.1

# Copy your FastAPI application code into the container
COPY . .

# Expose the port that your FastAPI app listens on (e.g., 8000)
EXPOSE 8000

# Define the command to run your FastAPI application

CMD ["uvicorn", "run:app", "--host", "0.0.0.0", "--port", "8000", "--reload", "--root-path='/fastapi'"]