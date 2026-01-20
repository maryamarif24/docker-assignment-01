# Install python version 3.12
FROM python:3.12-slim 

# Set working directory means (where the commands will be executed)
WORKDIR /app 

# Copy all files to working directory
COPY . . 

# Install uv using pip
RUN pip install uv 

# Install all dependencies in a project
RUN uv sync 

# Application access port, localhost:8000 or 127.0.0.1:8000
EXPOSE 8000 

# Run the application
CMD ["uv", "run", "fastapi", "dev", "main.py", "--host", "0.0.0.0"]