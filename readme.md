Culture Trip EngOps Test

First install dependencies with: 

```
npm install
```

To run the server use the command: 
```
npm start
```

Provide `PORT` and the Open Weather Map Key `API_Key` as environmental variables.
By default the server will start on port `3000`.

To get your Open Weather Map Key sign up here https://home.openweathermap.org/

## Deployment Steps
- Clone down this repo and create a .env file at the root of the repo. Then populate it with the following (replace with your api key)

```
PORT="3000"
API_KEY="<api-key-here>"
```
- Then run docker commands to build app within the root directory
```
docker build -t weather-api .

#Upload to docker hub
docker tag weather-api fayez74/weather-api
docker push fayez74/weather-api

```
- Proceed to https://github.com/Fayez74/weather-infrastructure to continue with deployment