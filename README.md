# Air Quality Analyser

A web client for Air Quality Analyser(https://github.com/UnremittingEncore/air-quality-analyser)

# Local Setup

## Run the following command to install node_modules
```
npm install
```

## After installing node modules run this command to fix depriciated dependencies
```
npm audit fix --force 
```
## Run the following command to launch the web application
```
npm start
```

The above instructions will install all the dependencies and start a server at `http://localhost:3000/`.

# API

## OpenAQ
OpenAQ is a non-profit organization empowering communities around the globe to clean their air by harmonizing, sharing, and using open air quality data.

## We are using the data from OpenAQ API to display Air-Quality
Any parameters should be passed as an optional `params` object as seen in the examples.
Complete documentation for OpenAQ's API is provided here: https://docs.openaq.org

### [.countries(params)](https://docs.openaq.org/#api-Countries)
- example:
```javascript
countries().then(results => {
  //results here
})

//with optional parameters
countries({limit:10, page:2}).then(results => {
  //results here
})
```

### [.locations(params)](https://docs.openaq.org/#api-Locations)
- example:
```javascript
locations().then(results => {
  //results here
})

//with optional parameters
locations({location:'Bowling Green', parameter:'o3'}).then(results => {
  //results here
})
```

### [.measurements(params)](https://docs.openaq.org/#api-Measurements)
- example:
```javascript
measurements().then(results => {
  //results here
})

//with optional parameters
measurements({location:'Bowling Green', parameter:'o3'}).then(results => {
  //results here
})
```

### [.parameters()](https://docs.openaq.org/#api-Parameters)
- example:
```javascript
parameters().then(results => {
  //results here
})
```

### [.sources(params)](https://docs.openaq.org/#api-Sources)
- example:
```javascript

sources().then(results => {
  //results here
})

//with optional parameters
sources({limit:10, page:2}).then(results => {
  //results here
})
```

