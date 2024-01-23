# Projekt "Node.js API + HTML Frontend + Docker"

## Opis projektu

Projekt jest kompleksową aplikacją internetową, zawierającą API w Node.js, frontend w HTML i konteneryzację za pomocą Docker.

## Struktura projektu

project-root

│

├── api

│ ├── app.js

│ ├── routes

│ │ ├── apiRoutes.js

│ │ └── ...

│ └── package.json

│

├── frontend

│ ├── index.html

│ ├── styles.css

│ └── scripts.js

│

├── Dockerfile

└── docker-compose.yml


- **api**: Zawiera kod dla API w Node.js.
- **frontend**: Zawiera plik HTML, style i skrypty dla frontendu.
- **Dockerfile**: Plik do tworzenia obrazu Docker.
- **docker-compose.yml**: Plik do konfiguracji Docker Compose.

## Zależności

- Node.js
- npm
- Docker

## Instalacja i Uruchamianie

1. **API:**

    ```bash
    cd api
    npm install
    node app.js
    ```

    API będzie dostępne pod adresem `http://localhost:3000`.

2. **Frontend:**

    Otwórz `frontend/index.html` w swojej przeglądarce.

3. **Docker:**

    ```bash
    docker-compose up --build
    ```

    Aplikacja będzie dostępna pod adresem `http://localhost:8080`.

## Trasy API

- **GET /api/data**: Pobierz dane.
- **POST /api/data**: Wyślij dane.

## Frontend

Otwórz `frontend/index.html` w przeglądarce, aby korzystać z interfejsu frontendowego.

## Docker

Projekt obsługuje konteneryzację za pomocą Docker. Możesz użyć `docker-compose` do łatwej instalacji i uruchomienia.

## Uwagi

- Upewnij się, że wszystkie zależności są zainstalowane przed uruchomieniem aplikacji.
- W celu rozwoju, można używać narzędzi takich jak Nodemon do automatycznego ponownego uruchamiania serwera po wprowadzeniu zmian w kodzie.
- Dla frontendu można użyć narzędzi do budowania, takich jak Webpack, do zarządzania zależnościami i budowania.

