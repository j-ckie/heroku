# Heroku Demo
## For the Jan 2020 DigitalCrafts Cohort

1. install the Heroku CLI globally (only needs to be done once) `npm i heroku -g`
2. setup heroku app 
    a. Create New App 
    b. App name
3. `heroku login`
4. `heroku git:remote -a <HEROKU_APP_NAME>`
5. Add Procfile with web:node index.js in contents
6. In *package.json* file, add `"start": "node index.js"` to `"scripts"`
7. Change port on *index.js* to `const PORT = process.env.PORT || 8080;`
8. Commit like normal
9. Make sure local master branch is up to date - if not, `git pull origin master`
10. `git push heroku master` This pushes local master branch to heroku and deploys
11. Add environment/config variables to heroku with `heroku config:set <ENVIRONMENT_VARIABLE>=<SOMETHING_SECRET>`
11. Debug with `heroku logs --tail` if app is experiencing issues