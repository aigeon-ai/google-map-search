```markdown
# Aigeon AI Google Map Search

Aigeon AI Google Map Search is a Python-based server application designed to facilitate the scraping of Google Maps data using the SerpApi service. This application leverages the FastMCP framework to provide a robust and efficient tool for querying and retrieving location-based information from Google Maps.

## Features Overview

- **Google Maps Data Scraping**: The application is capable of scraping data from Google Maps using the SerpApi service.
- **Flexible Query Parameters**: Supports a wide range of query parameters to customize searches, including location coordinates, language, and country settings.
- **Pagination Support**: Allows for result pagination to navigate through multiple pages of search results.
- **Cache Management**: Offers options to utilize cached results or force fresh data retrieval.
- **Asynchronous Search Submission**: Provides the ability to submit searches asynchronously, optimizing performance and resource usage.

## Main Features and Functionality

### Google Maps Search

The core functionality of the application is to perform searches on Google Maps using the SerpApi. The `search_map` function serves as the primary tool for executing these searches. It accepts several parameters to customize the search:

- **Query (`q`)**: The main search query, similar to what you would use in a regular Google Maps search.
- **Location Coordinates (`ll`)**: Specifies the GPS coordinates to originate the search from, formatted as `@latitude,longitude,zoom`.
- **Google Domain (`google_domain`)**: Defines the Google domain to use for the search, defaulting to `google.com`.
- **Country (`gl`)**: Sets the country context for the search using a two-letter country code.
- **Language (`hl`)**: Determines the language for the search results using a two-letter language code.
- **Result Offset (`start`)**: Used for pagination, allowing the skipping of a specified number of results.
- **Cache Control (`no_cache`)**: Controls whether to use cached results or fetch new data.
- **Asynchronous Execution (`aasync`)**: Specifies whether to perform the search asynchronously.

### API Endpoints or Main Functions Description

#### `search_map`

This function is the primary entry point for executing Google Maps searches. It constructs a request payload based on the provided parameters and sends a GET request to the SerpApi endpoint. The response is returned in JSON format, containing the search results.

- **Parameters**:
  - `q`: The search query string.
  - `ll`: Optional GPS coordinates for search origin.
  - `google_domain`: Optional Google domain for the search.
  - `gl`: Optional country code for the search.
  - `hl`: Optional language code for the search.
  - `start`: Optional result offset for pagination.
  - `no_cache`: Optional boolean to control cache usage.
  - `aasync`: Optional boolean for asynchronous search submission.

- **Returns**: JSON response containing the search results from Google Maps.

### Execution

The server is designed to run using the FastMCP framework, which handles the transport and execution of the `search_map` tool. By default, the server listens on port 9997, but this can be customized via command-line arguments.

---

This README provides an overview of the Aigeon AI Google Map Search application, detailing its features, functionality, and usage. For further details on configuration and deployment, please refer to the source code and accompanying documentation.
```