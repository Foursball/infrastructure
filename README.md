## Foursball Infrastructure
Consolidated Foursball infrastructure for use locally.

## Setup
Copy `example.env` to `.env` and replace the values with your own.

There is also a local IP needed for the UI proxy, so replace `<local-ip>` with you local IP in the `docker-compose.yml` file.

## Running
To run with native Docker run `docker-compose up -d`. Wait for the environment to initialize then access http://log.localhost for logging, http://portainer.localhost for Docker management, and http://api.localhost for the Foursball REST API.

If you are running Docker using Docker Machine use the native ports to access the services. Update the API `SERVER_URL` environment variable to use http://[docker-machine-ip]:8000. Make sure to update your OAuth application URLs as well. You can then access http://[docker-machine-ip]:5601 for logging, http://[docker-machine-ip]:9000 for Docker management, and http://[docker-machine-ip]:8000 for the Foursball REST API.

## Logging Setup
The first time you run the logging service you'll be presented with a page to set up the index. As long as the API has been running for a couple minutes you should have a green **Create** button at the bottom of the page. Click this then go back to the **Discover** tag to start exploring logs.
