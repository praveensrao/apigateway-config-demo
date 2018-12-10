# apigateway-config-demo
A repository for demo api gateway configuration

Please update the api-gateway.yml for any configuration changes / addition of new endpoints to be exposed in the gateway.

Make sure that the indentation is appropriate in the yaml file.

To add an additional route, for e.g. shipstation-marketplace-api, add this to the routes section and also ensure that the ribbon configuration for the API is added.

```
    shipstation-marketplace-api:
      path: /esb/shipstation/marketplace
      serviceId: shipstation-marketplace-api
```

```
shipstation-marketplace-api:
  ribbon:
    NIWSServerListClassName: com.netflix.loadbalancer.ConfigurationBasedServerList
listOfServers: http://localhost:20080
```
