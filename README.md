# Web Development Project (ESD VI): User Records CRUD App

Academic web development project (2022), B.E. Electronics & Telecommunication, Thakur College of Engineering and Technology (TCET), University of Mumbai.

A small full-stack application for managing user records (name, age, city): a REST API on Node.js with a MongoDB Atlas database, and a Bootstrap front end that lists, adds, edits and deletes records.

## Structure

| Folder | What it contains |
|---|---|
| `ESD_Day_3_/` | Backend: Express server (`index.js`) and the `/user` routes with a Mongoose model (`users_module.js`) |
| `ESD_Day_5/` | Frontend: `index.html` (listing), `add.html`, `edit.html`, `script.js` (fetch calls to the API), Bootstrap 5 |

## API

Base URL: `http://localhost:8080/user`

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/user` | List all users |
| GET | `/user/:id` | Get one user |
| POST | `/user` | Create a user (`name`, `age`, `city`) |
| PUT | `/user` | Update a user (`id`, `name`, `age`, `city`) |
| DELETE | `/user?id=<id>` | Delete a user |

CORS is enabled so the front end can call the API from another origin. The endpoints can be tried with Postman or any HTTP client.

## Run it locally

You need Node.js and your own free MongoDB Atlas cluster.

```bash
cd ESD_Day_3_
npm install

# set your own connection string (see .env.example)
# Windows (PowerShell):   $env:MONGO_URI="your-connection-string"
# macOS/Linux:            export MONGO_URI="your-connection-string"

npm start        # API on http://localhost:8080
```

Then open `ESD_Day_5/index.html` in a browser. It calls `http://localhost:8080/user` (set at the top of `script.js`).

## Notes

- No database credentials are stored in this repository. Earlier versions contained a hard-coded connection string; it has been removed from the code.
- Built with: HTML, CSS (Bootstrap 5), JavaScript (fetch), Node.js, Express, Mongoose, MongoDB Atlas.

## Author

Het Dani, [LinkedIn](https://www.linkedin.com/in/het-dani-0b6767220/)
