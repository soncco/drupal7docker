$ docker build . -t ${CONTAINER_IMAGE}:latest

$ docker run -d --env-file ./.env -p ${PORT}:80 -v ${PWD}/drupal-data/modules:/var/www/html/sites/all/modules -v ${PWD}/drupal-data/themes:/var/www/html/sites/all/themes -v ${PWD}/drupal-data/files:/var/www/html/sites/default/files --network ${NETWORK} --name ${CONTAINER_NAME} ${CONTAINER_IMAGE}

docker run -d --name phpmyadmin -e PMA_ARBITRARY=1 -p 8800:80 phpmyadmin
