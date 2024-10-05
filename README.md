# JobJet - devbox

This is a tool to manage the development environment for JobJet.

---

### Getting Started

To get started:

1. Create root directory for JobJet project called `JobJet`
2. Inside this directory, create required directories:
    ```bash
    mkdir backend frontend devbox
    ```
3. For each directory clone the respective repository:
    ```bash
    cd frontend && \
    git clone https://github.com/PatrycjuszNowaczyk/jobjet-frontend.git && \
    cd ../backend && \
    git clone https://github.com/PatrycjuszNowaczyk/jobjet-backend.git && \
    cd ../devbox && \
    git clone https://github.com/PatrycjuszNowaczyk/jobjet-devbox.git
    ```
4. Inside `devbox` directory, run:
    ```bash
    docker compose up -d
   ```
   > flag `-d` is optional to run containers in background
5. To stop docker containers inside `devbox` directory, run:
    ```bash
    `docker compose down`
    ```


After all is done, you can start developing.
