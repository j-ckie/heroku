# Heroku Demo
## For the Jan 2020 DigitalCrafts Cohort

Try out the steps below with this repo! Make sure you add a *.env* file to the root folder, with the contents: `SESSION_SECRET=cat`

1. Install the Heroku CLI globally (only needs to be done once) `npm i heroku -g`
2. Setup heroku app here: https://dashboard.heroku.com/
    <br />
    a. Create New App
    <br /> 
    b. App name
3. `heroku login`
4. `heroku git:remote -a <HEROKU_APP_NAME>`
5. `touch Procfile` and add ```web:node index.js``` to file
6. In *package.json* file, add ```"start": "node index.js"``` to ```"scripts"```
    <br />
    <br />
    ```JavaScript
    "scripts": {
        "start": "node index.js"
    }
    ```
    <br />
7. Change port on *index.js* to `const PORT = process.env.PORT || 8080;`
8. Commit like normal
9. Make sure local master branch is up to date - if not, `git pull origin master`
10. `git push heroku master` This pushes local master branch to heroku and deploys
11. Add environment/config variables to heroku with `heroku config:set <ENVIRONMENT_VARIABLE>=<SOMETHING_SECRET>`
11. Debug with `heroku logs --tail` if app is experiencing issues
