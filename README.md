 ### Connect local host service_1 Run with Go:

```bash
go run main.go
```

# Create Dockerfile run with go lang

```golang:1.20-alpine
CMD ["nginx", "-g", "daemon off;"]

CMD will be  Run time compile
```

### Second run app.py file using Run with Python:

```bash
uv run app.py
```

This will start the server on port `8002`.

---
# Create Dockerfile run the app.py

``` FROM python:3.9-alpine
RUN pip install -r requirements.txt
```

### Third Create Docker-compose.yml file 

- Docker
- Docker Compose v2

Verify installation:
```bash
docker --version
docker compose version
```
### Helth cleck
#!/bin/bash

echo "Checking Service 1..."
curl -f http://localhost:8080/service1 || exit 1

echo "Checking Service 2..."
curl -f http://localhost:8080/service2 || exit 1

echo " All services are healthy"

```
chmod +x healthcheck.sh
./healthcheck.sh
```
## Logging Clarity
docker compose logs -f nginx
docker compose logs -f service1
docker compose logs -f service2