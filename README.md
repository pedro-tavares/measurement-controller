# measurement-controller

## Development

To start application simply run:

    ./gradlew bootRun
    
## Demo scenario

[Use postman collection](measurement-controller.postman_collection.json)
### There are three API
1. POST /api/users - for creating user
2. PUT /api/users - for updating existing user
3. DELETE /api/users/{id} - for removing existing user

## How-to extend configure new vendor
Describe new vendor inside application.yml(could be dynamic configuration in future) [see example 'application.vendor-configurations'](src/main/resources/application.yml).
To register new vendor data storage implement interface [VendorDataStorage](src/main/java/software/entity/measurementcontroller/repository/VendorDataStorage.java).
To register new subscription strategy(e.g. SUBSCRIBER) implement [VendorSubscriptionTask](src/main/java/software/entity/measurementcontroller/service/VendorSubscriptionTask.java)
  