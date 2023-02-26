# Food Store Search API

This API provides two endpoints for searching food stores based on various criteria, using data stored in an Elasticsearch engine. The API includes two endpoints: `searchNearestStores` and `searchByPartialNameOrAddress`.

## Requirements

To run the API locally, you need to have the following installed:

- Docker
- Docker Compose
- Java 11

## Getting Started

To get started with the API, follow these steps:

1. Clone this repository to your local machine.
2. In the root directory of the project, run `docker-compose up` to start the Elasticsearch instance and the API instance. The instances will be able to communicate with each other.
3. To access the API, navigate to `http://localhost:8080`.
4. The API provides two endpoints:
   - `/searchNearestStores`: Expects 2 required arguments, latitude and longitude, and two optional parameters distance and batch size. It returns stores that are within a radius of the provided distance (in kilometers). The default batch size is 10, and the default distance is 1.
   - `/searchByPartialNameOrAddress`: Expects an input parameter `string`, which is required, and an optional `batch size`.
5. To stop the instances, run `docker-compose down`.

If you want to use a standalone Elasticsearch instance, download the version 7.15 from the [Elasticsearch website](https://www.elastic.co/downloads/past-releases/elasticsearch-7-15-0) and run the following command:


## Libraries

The application uses the following libraries:

- Spring Boot version 2.7.8
- opencsv version 5.7

## Data

The data used by the API is loaded from a provided CSV file.
