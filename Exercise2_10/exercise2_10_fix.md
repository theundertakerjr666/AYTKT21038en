- Reverse proxy uses port 80, this causes an issue as we defined the frontend container to be port 5000.
- CORS error thrown 
- recompile backend Dockerfile 'REQUEST_ORIGIN=http://127.0.0.1'
