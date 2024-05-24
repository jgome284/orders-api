# Open API with Swagger

## Overview

This api was created by using the [OpenAPI-Spec](https://github.com/OAI/OpenAPI-Specification). It's [design](./orders-openapi-spec.yaml) was developed by leveraging the [swagger editor.](https://editor.swagger.io/)

## Running the server

To run the server, run:

```npm
npm start
```

## API Requests

### Return all Orders

To test the /orders path, we can simply navigate to <http://localhost:3000/orders> in a browser. The data should appear on the screen.

Otherwise you can run the following command on curl.

```bash
curl http://localhost:3000/orders
```

### Creating a New Order

To test our /neworder path, run the following command:

```bash
curl --header "Content-Type: application/json" -d "@new_order.json" http://localhost:3000/neworder
```

You can replace `new_order.json` with a new json file of your choice.

### Updating an Existing Order

You can use a curl command like the one below to update an existing order:

```bash
curl -X PUT -d {data} http://localhost:3000/update/{id}
```

This command makes a PUT request which modifies the state of the order with an id specified. e.g. replace {id} with 1. It will change it to the text {data}. Use the GET request again by refreshing the server on the browser to see the changes in the first order.

### Deleting an Existing Order

Use this curl command to make a DELETE request to our /delete/{id} endpoint... don't forget to replace {id} with an id of your choice.

```bash
curl -X DELETE http://localhost:3000/delete/{id}
```
