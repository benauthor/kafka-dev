# workspace for local librdkafka development

- checkout librdkafka
- `./configure --install-deps`
- `make`
- `sudo make install`


```sh
# terminal 1
docker-compose up

# terminal 2
docker-compose exec kafka /bin/bash
kafka-console-producer --bootstrap-server=localhost:9092 --topic myTopic
# type some gobbledygook

# terminal 3
cd consumer
go run -tags dynamic .
# now you are using local librdkafka!
```
