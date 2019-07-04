# docker-compose-with-image-building
docker-compose for run-time image building and multi-container dev

This is a docker-compose example in which a custom image is built to have a drupal container with bootstrap them on it. To test it follow the following steps:

## Start Containers, Configure Drupal
- Create the containers via the following command: `docker-compose up`
- Go to http://localhost:8080, configure Drupal web install.
- After website comcck on `Appearance` in top bar, and notice a new theme called `Bootstrap` is there. That's the one we added with our custom Dockerfile.
- Click `Install and set as default`. Then click `Back to site` (in top left) and the website interface should look different. You've successfully installed and activated a new theme in your own custom image without installing anything on your host other then Docker!
- If you exit (ctrl-c) and then `docker-compose down` it will delete containers, but not the volumes, so on next `docker-compose up` everything will be as it was.
- To totally clean up volumes, add `-v` to `down` command.
