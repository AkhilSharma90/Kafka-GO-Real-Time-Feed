# Realtime Feed

This example features a very busy blogging platform, with thousands of messages showing up on your feed.

There are two separate applications (microservices) integrating over a Kafka topic. The [`producer`](producer/) generates
thousands of "posts" and publishes them to the topic. The [`consumer`](consumer/) subscribes to this topic and 
displays each post on the standard output.

The consumer has a throttling middleware enabled, so you have a chance to actually read the posts.

To understand the background and internals, see [getting started guide](https://watermill.io/docs/getting-started/).

## Requirements

To run this example you will need Docker and docker-compose installed. See the [installation guide](https://docs.docker.com/compose/install/).

## Running

```bash
docker-compose up
```

You should see the live feed of posts on the standard output.
