---
id: thrift
title: Apache Thrift
sidebar_label: Apache Thrift
---
![image](https://user-images.githubusercontent.com/20847995/79219986-e4903080-7e5b-11ea-8220-e69ae73e7966.png)

This handler allows you to consume [Apache Thrift](https://thrift.apache.org/) `.thrift` files and generate a remote executable schema for those services.

To get started, install the handler library from NPM:

```
$ yarn add @graphql-mesh/thrift
```

Now, you can use it directly in your Mesh config file:

```yml
sources:
    - name: Calculator
      handler:
        thrift:
          idl: ./src/thrift/calculator.thrift
          hostName: localhost
          port: 8080
          path: /thrift
          serviceName: calculator-service
```

> You can check out our example that uses Thrift Handler.
[Click here to open the example on GitHub](https://github.com/Urigo/graphql-mesh/tree/master/examples/thrift-calculator)

## Config API Reference

{@import ../generated-markdown/ThriftHandler.generated.md}
