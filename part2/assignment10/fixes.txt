The API url pointed directly to the backend server on localhost:8000. This caused the proxy to be bypassed. When the browser tried to contact the server directly, on a different port, this caused the CORS check to fail, preventing the browser from getting a response from the server.

To fix this, I changed the API_URL in docker-compose.yml to /api.
