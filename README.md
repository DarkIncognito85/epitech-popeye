## Popeye
![docker logo](./images/docker.png)

The application is composed of 5 elements:
- **Poll**, a Flask Python web application that gathers votes and push them into a Redis queue.
- **A Redis queue**, which holds the votes sent by the Poll application, awaiting for them to be
consumed by the Worker.
- **The Worker**, a Java application which consumes the votes being in the Redis queue, and stores
them into a PostgreSQL database.
- **Database**, a PostgreSQL database , which (persistently) stores the votes stored by the Worker.
- **Result**, a Node.js web application that fetches the votes from the database and displays the result

## Usage
```
docker build && docker-compose up
```
Go to `localhost:5001` on you brower to show result page and `localhost:5000` to show vote page

## Results screen
![vote](./images/vote.png)
![result](./images/result.png)
