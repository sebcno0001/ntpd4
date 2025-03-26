````Uruchamianie aplikacji````

***Lokalnie (bez Dockera)***
Zainstaluj wymagane zależności:
pip install -r requirements.txt
Uruchom serwer FastAPI:
uvicorn main:app --host 0.0.0.0 --port 8000
API będzie dostępne pod adresem http://localhost:8000.

***Za pomocą Dockera***
Zbuduj obraz:
docker build -t fastapi-ml .
Uruchom kontener:
docker run -p 8000:8000 fastapi-ml

***Za pomocą Docker Compose***
Uruchom aplikację i bazę Redis:
docker-compose up --build

Zmienne środowiskowe:
PORT – port serwera (domyślnie 8000)
REDIS_HOST – adres hosta Redis
REDIS_PORT – port Redis (domyślnie 6379)

Wymagania
Python 3.9+
FastAPI, Uvicorn, Scikit-learn
Docker & Docker Compose
