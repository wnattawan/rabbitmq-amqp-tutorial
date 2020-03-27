# Build
`
mvnw clean package
`

# Start RabbitMQ
`
docker-compose up
`

# Run a Sender application
`
java -jar target/rabbitmq-amqp-tutorial-0.0.1.jar --spring.profiles.active=hello-world,sender
`

# Run a Receiver application
`
java -jar target/rabbitmq-amqp-tutorial-0.0.1.jar --spring.profiles.active=hello-world,receiver
`

# Run different tutorials
This tutorial application use Spring Profile to select a tutorial module to execute. 
Specify different tutorial module name in spring.profiles.active to run different tutorials

## Default exchange tutorial
spring.profiles.active=hello-world 

## Work queues (competing consumers) tutorial
spring.profiles.active=work-queues

## Publish/Subscribe tutorial
spring.profiles.active=pub-sub
