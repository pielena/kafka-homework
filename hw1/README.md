Порядок действий:

- запустить docker-compose файл:

docker compose -f docker-compose.yml up -d


- зайти в контейнер:

docker exec -it kafka /bin/bash

cd ..

cd ..

cd bin

- создание топика: 

kafka-topics --create --topic test1  --bootstrap-server kafka:19092

kafka-topics --list --bootstrap-server kafka:19092

- запись в топик:

kafka-console-producer --topic test --bootstrap-server kafka:19092

- чтение из топика:

kafka-console-consumer --topic test --bootstrap-server kafka:19092 --from-beginning

- завершение работы, удаление контейнеров

exit

docker-compose down

