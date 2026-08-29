# Stage 1: Build / dependency stage
FROM python:3.12-slim AS base

WORKDIR /app

# Copy dependency file first
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application source code
COPY . .


#######################################################
# Stage 2: Runtime stage
FROM python:3.12-slim

WORKDIR /app

# Copy installed Python packages
COPY --from=base /usr/local/lib/python3.12/site-packages \
    /usr/local/lib/python3.12/site-packages

# Copy Python executable/scripts if required
COPY --from=base /usr/local/bin \
    /usr/local/bin

# Copy application code
COPY --from=base /app .

# Application port
EXPOSE 5000

# Start application
CMD ["python", "app.py"]