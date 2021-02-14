# Music-Genre-Classification-Model-REST-API

## Development

It is recommended to use a virtual python environment in order to install every dependency.

Create a virtual environment the _venv_ directory at the root of this project.

### Installing dependencies

``` 

python3 -m venv venv
```

To activate the created virtual environment

``` 

source venv/bin/activate
```

Installing dependencies:

``` 

pip install -r requirements.txt
```

### Running the APP

``` 
uvicorn app.main:app --reload --port 5000
```
*note*: any other availabel port can be used

## Production

The Fast API for production uses Docker, python and uvicorn and is deployed on a kubernetes cluster.

### Locally build Docker Image

``` 
docker build -t music-genre-prediction-model-rest-api .
```

### Run Docker image

```
docker run -p 5000:5000  music-genre-prediction-model-rest-api .
```
