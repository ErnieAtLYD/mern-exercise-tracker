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

Inside .gitignore:

```
.env
/node_modules
```
