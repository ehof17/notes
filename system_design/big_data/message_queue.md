If application cannot process a ton of events its better to queue each event and process later

Event to queue, queue to app server

Decoupled its event

Queue is durable. if the queue crashes it usually will be good.

App server may not be able to process 

There is a way for server to update the queue
Server will need to send an acknowledgement

Queue can have multiple pubs and multiple subs

Multiple applications can receive from the same topic
One topic is payment info
One topic is analytics info.
Analytics might only have one subscriber

RabbitMQ, Kafka, GCP Pub/sub
