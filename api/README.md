#!/usr/bin/env bash

# Cache Redis Config

This is a simple application to manage Redis configuration for caching.

# Usage
You can install the package by running the following command:
```bash
pip install -r requirements.txt
```

# Requirements
- redis
- python-dotenv

# Environment Variables
- CACHE_HOST: The host of the Redis server
- CACHE_PORT: The port of the Redis server
- CACHE_DB: The database number to use on the Redis server
- CACHE_PASSWORD: The password to use to connect to the Redis server

# Configuration File
You can configure the application by creating a `.env` file in the root of the project with the following format:
```bash
CACHE_HOST=127.0.0.1
CACHE_PORT=6379
CACHE_DB=0
CACHE_PASSWORD=your_password
```

# API Endpoints
- `GET /config`: Returns the configuration of the Redis server
- `POST /config`: Updates the configuration of the Redis server

# API Response
{
  "status": "success",
  "config": {
    "host": "127.0.0.1",
    "port": 6379,
    "db": 0
  }
}

# API Error Response
{
  "status": "error",
  "message": "Invalid request"
}