# TypingFightMultiplayer

A Multiplayer Typing Game for playing with friends and also helpful for increasing the typing speed.

## Run Locally

Go to the server folder in project directory

```bash
  cd TypingFight_Master/server/
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  node server.js or SERVER_BASE_URL=http://localhost:8080 node server.js
```

Finally try it in a Browser !

```bash
  Open http://localhost:3000/ on any Browser
```

## API Reference

Api Used : https://api.chucknorris.io

### Get Random Line

```http
  GET /jokes/random
```

### Get item with specified category

```http
  GET /jokes/random?category=${randomCategory}
```

| Parameter        | Type              | Description                                     |
| :--------------- | :---------------- | :---------------------------------------------- |
| `randomCategory` | `List of Strings` | List of Category to chose from of item to fetch |

```javascript
const apiUrl = `https://api.chucknorris.io/jokes/random?category=${randomCategory}`;
fetch(apiUrl)
  .then((response) => response.json())
  .then((data) => {
    return data.value;
  })
  .catch((err) => {
    console.error(err.message);
  });
```

Fetches a random joke from the specified category list.

## Tech Stack

**Client:** HTML, CSS, VanilaJS, Scoket-io

**Server:** Node, Express, ScoketIO

**Server Dev Dependencies:** nodemon
