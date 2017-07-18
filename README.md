# WebProtégé - Docker
Lite-weight docker image for webprotege that runs on alpine.

## Usage
- Pull Image

        docker pull v1shwa/webprotege
- Start mongo db instance

        docker run -it -d -p 27017:27017 -v $(pwd)/mongo_data:/data/db --name mongodb mongo
- Start the web-protege instance

        docker run -ti -d -p 9899:8080 --link mongo:mongo -v $(pwd)/protege_data:/data/webprotege --name protege v1shwa/webprotege

- Done. You can now access the webprotege at [localhost:9899](http://localhost:9899/) 