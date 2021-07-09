# Fire Watch Application Backend

## About Fire Watch

Fire Watch is an open source product to help prevent forest fires in different climatic zones.
Our sensor stations will track the environmental conditions in your forest to give you all the information you need to prevent a fire.


## Installation

### 1) customize Dockerfile
```
LABEL traefik.http.routers.<PROJECT_NAME>.rule="Host(`<PROJECT_NAME>.<YOUR_SERVER_ADRESS>`)"
```
### 2) create Docker Container
1. create Docker image
2. create Container out of the image
     
### 3) define environmental variables
DB_USER: <YOUR_DATABASE_USER><br>
DB_PWD:  <YOUR_DATABASE_PWD>




## Usage

1) contact us to buy our Service and we will install our sensors in your forest
2) register Forest via your individual forest Code
3) track your sensor data to prevent forest fires
4) feel free to share your Fire Watch data with other Fire Watch Users

## Communication Technologie
### HTTP
Framework:<br>
express https://expressjs.com/


## Software Architecture

### Frontend Application
https://github.com/tobiasraab/FireWatch_App_Frontend


### Backend Application

#### User Service

https://github.com/tobiasraab/FireWatch_App_Backend_userService

#### Database Service
https://github.com/tobiasraab/FireWatch_APP_Backend_databaseService




#### Weather Service
// weatherService.js
1) OpenWeather API call:
   ```
      'https://api.openweathermap.org/data/2.5/weather?lat=<LATITUDE>&lon=<LONGITUDE>6&units=metric&appid=<API_KEY>'
   ```
   (OpenWeather https://openweathermap.org/)
2) save API response in database collection 'weather'
3) delete old weather data in collection 'weather'
<br><br><br><br><br><br><br>








### Sensor Backend
https://github.com/tobiasraab/FireWatch_Sensors_Backend


### MongoDB Database
https://www.mongodb.com/
#### Collection forests:<br>
* 0.2kB per forest
#### Collection sensorDatas:<br>
* 0.45kB per Sensor
#### Collection userData:<br>
* 0.5kB per user
#### Collection weather:<br>
* 0.8kB per forest






## Future Work
* get more weather data
* save data history
