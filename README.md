# kafka
tested docker-compose.yml

Зайти в контейнер
docker container exec -it kafka /bin/bash
Создать топик
./kafka-topics --create --topic registrations --bootstrap-server localhost:29092
Посмотреть инфу по топику
./kafka-topics --describe --topic registrations --bootstrap-server localhost:29092
Отправить сообщение
./kafka-console-producer --topic registrations --bootstrap-server localhost:29092
Получить сообщение
./kafka-console-consumer --topic registrations --bootstrap-server localhost:29092 --consumer-property auto.offset.reset=earliest
Прочитать в группе
./kafka-console-consumer --topic registrations --bootstrap-server localhost:29092 --consumer-property auto.offset.reset=earliest --group slurm
информация по группе
./kafka-consumer-groups --bootstrap-server localhost:29092 --group slurm --describe
