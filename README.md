# Express Gateway in Docker Compose

A docker compose for Express Gateway containing the preview ratelimit I-D implementation.

There is no web-ui for now.

# What is Express Gateway?

Express Gateway is a [Microservices and Serverless to Production Insanely Fast](https://www.express-gateway.io/)

# How to use this template

This Docker Compose template provisions a Kong container with a Postgres database, plus a nginx load-balancer and Consul for service discovery. After running the template, the `nginx-lb` load-balancer will be the entrypoint to Kong.

To run this template execute:

```shell
$ docker-compose -d up
```

You can invoke the service on port 8080 and passing the `host` http header field
that is used by express-gateway to dispatch the request to the appropriate
backend.

```
$ curl -i http://localhost:8080/ip -H "host: hb.example.com"
```

Scaling features are not currently supported

TODO: the port where to listen

TODO: link Express Gateway docuemntation.

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue][github-new-issue].
