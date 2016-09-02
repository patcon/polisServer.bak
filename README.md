# Polis
pol.is an AI powered sentiment gathering platform. More organic than surveys, less effort than focus groups.

If you don't want to deploy your own instance of Polis, you can use our SaaS version [here](https://pol.is/home)
Polis [can be easily embedded](http://docs.pol.is/usage/Embedding.html) on your page as an iframe.

### Getting Started

The following are required:

* `nvm`
* MongoDB
* PostgreSQL
* Heroku Toolbelt

Prepare databases:

```
createdb polis
psql polis < postgres/db_setup_draft.sql
```

Ensure you're running the proper version of Node.js:

```
cat package.json | grep engines -A3
--  "engines": {
--    "node": "6.2.0",
--    "npm": "3.3.8"
--  },
nvm install 6.3.1
nvm use 6.3.1
-- Now using node v6.3.1 (npm v3.10.3)
```

Install and run:

```
npm install --no-optional
cp sample.env .env
heroku local
```
