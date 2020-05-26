```
touch README.md
touch .gitignore
cd backend

# now in /mern-exercise-tracker/backend
mv package.json ..
mv server.js ..
mv .env ..
rm -rf node_modules
rm yarn.lock
cd ..

# back in /mern-exercise-tracker
mv mern-exercise-tracker client
```

Inside `.gitignore`:

```
.env
/node_modules
```

```
# in /mern-exercise-tracker
yarn
cp .env .env.sample
```

Clean up `.env.sample` to remove any API keys from GitHub.

Add scripts to run nodemon in `package.json`:

```
  "scripts": {
    "client": "cd client && yarn start",
    "server": "nodemon server.js",
    "dev": "concurrently --kill-others-on-fail \"yarn server\" \"yarn client\""
  },
```
