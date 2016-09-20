[![Build Status](https://travis-ci.org/blockchain-certificates/cert-intro.svg?branch=master)](https://travis-ci.org/blockchain-certificates/cert-intro)
[![](https://images.microbadger.com/badges/version/blockcerts/certintro_web.svg)](http://microbadger.com/images/blockcerts/certintro_web "Get your own version badge on microbadger.com")

# cert-store

Blockchain certificate introduction service


## Quick Start with Docker

1. First ensure you have Docker installed. [See our Docker installation help](https://github.com/blockchain-certificates/developer-common-docs/blob/master/docker_install.md).
    
2. Git clone the repository

    ```
    git clone https://github.com/blockchain-certificates/cert-store.git
    ```

3. From a command line in the cert-store dir, run docker-compose

    ```
    cd cert-store
    docker-compose build
    ```

4. Start the container

    ```
    docker-compose up
    ```

5. Access cert-intro at `http://localhost:5003`.


## Running the CLI locally

1. Ensure you have an python environment. [Recommendations](https://github.com/blockchain-certificates/developer-common-docs/blob/master/virtualenv.md)

2. Install [mongodb](https://docs.mongodb.com/v3.0/installation/)

3. Install the dependencies
    ```bash
    pip install -r requirements.txt
    ```

4. Setup your config.py file

5. Start mongo database. `--dbpath` can be left off if you used the default location
    ```bash
    mongod --dbpath <path to data directory>
    ```
    
6. To run the server, execute the following:
    ```bash
    python run/app.py
    ```

You can see the Swagger API specification at this URL:

```
http://localhost:5003/ui/
```

## API Documentation

The API documentation is currently hosted here:

[http://cert-intro.herokuapp.com/ui/](http://cert-intro.herokuapp.com/ui/)

Updates coming soon!

## Unit tests

This project uses tox to validate against several python environments.

1. Ensure you have an python environment. [Recommendations](https://github.com/blockchain-certificates/developer-common-docs/blob/master/virtualenv.md)

2. Run tests
    ```
    ./run_tests.sh
    ```

## Release Docker image

```
docker build -t blockcerts/certstore:<version> .
docker login
docker push blockcerts/certstore:<version>
```


## Contact

Contact [certs@mit.edu](mailto:certs@mit.edu) with questions