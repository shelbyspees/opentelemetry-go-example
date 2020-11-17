# OpenTelemetry Example -- Go

This Fibonacci example demonstrates how to use OpenTelemetry to generate traces.

## Instrument with OpenTelemetry

We're using the OpenTelemetry core trace functionality along with the [OTel HTTP autoinstrumentation](https://github.com/open-telemetry/opentelemetry-go-contrib/tree/master/instrumentation) for Go.

## Send to Honeycomb

The app already has the [Honeycomb exporter](https://github.com/honeycombio/opentelemetry-exporter-go) set up so that you just need to include your Honeycomb API key as an environment variable when you start the server.

Get your API key via https://ui.honeycomb.io/account after signing up for Honeycomb.

## Make a request

Once you get the app running you can make a request at the root:

```console
$ curl localhost:3000
```

You can also set a value for `i` to see what the Fibonacci return value is:
```
$ curl http://localhost:3000/fib?i=1
```

[Go to the Honeycomb UI](https://ui.honeycomb.io/home) and watch your data arrive!

## Troubleshooting

If you don't see data coming in, make sure your API key has permission to create datasets. You can check your API key permissions at https://ui.honeycomb.io/account.

For other questions, please ask the Honeycomb team in Slack.
