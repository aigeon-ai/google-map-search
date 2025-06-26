# Aigeon AI Google Map Search

## Overview

Aigeon AI Google Map Search is a Python-based server application designed to facilitate the scraping of Google Maps data using the SerpApi service. This tool allows users to perform detailed searches on Google Maps by leveraging various query parameters, providing a flexible and powerful means to extract location-based information programmatically.

## Features Overview

- **Google Maps Data Scraping**: The application enables users to scrape data from Google Maps using a variety of search parameters.
- **Flexible Query Parameters**: Supports multiple parameters such as query string, location coordinates, Google domain, country, language, pagination, and caching options.
- **Integration with SerpApi**: Utilizes SerpApi to fetch Google Maps search results, ensuring reliable and up-to-date data retrieval.
- **Asynchronous Search Capability**: Offers the option to perform searches asynchronously, allowing users to retrieve results at a later time.

## Main Features and Functionality

1. **Search Functionality**: The core feature of the application is the ability to perform searches on Google Maps. Users can define their search queries using a variety of parameters to tailor the results to their specific needs.

2. **Parameter Customization**: The application supports a wide range of parameters:
   - **Query (`q`)**: Defines the search query, similar to a regular Google Maps search.
   - **Location (`ll`)**: Specifies the GPS coordinates and zoom level for the search origin.
   - **Google Domain (`google_domain`)**: Allows selection of a specific Google domain for the search.
   - **Country (`gl`)**: Sets the country context for the search using a two-letter country code.
   - **Language (`hl`)**: Determines the language for the search results using a two-letter language code.
   - **Pagination (`start`)**: Manages result pagination by skipping a specified number of results.
   - **Cache Control (`no_cache`)**: Controls whether to use cached results or force a fresh fetch from SerpApi.
   - **Asynchronous Search (`aasync`)**: Enables submitting searches asynchronously for later retrieval.

3. **Integration with SerpApi**: The application interfaces with SerpApi to perform the actual data retrieval, ensuring that the results are accurate and up-to-date.

4. **Server Execution**: The application runs as a server using the FastMCP framework, allowing it to handle requests and process searches efficiently.

## Main Functions Description

### `search_map`

This function is the primary tool for interacting with Google Maps data. It constructs a payload based on the provided parameters and sends a request to the SerpApi endpoint to retrieve search results. The function supports the following parameters:

- **`q`**: The search query string.
- **`ll`**: The GPS coordinates and zoom level for the search.
- **`google_domain`**: The Google domain to use for the search.
- **`gl`**: The country code for the search context.
- **`hl`**: The language code for the search results.
- **`start`**: The result offset for pagination.
- **`no_cache`**: A boolean to control cache usage.
- **`aasync`**: A boolean to enable asynchronous search submission.

The function constructs a request payload, filters out any `None` values, and sends a GET request to the SerpApi endpoint. The response is returned in JSON format, providing the search results.

---

This documentation provides a comprehensive overview of the Aigeon AI Google Map Search application, detailing its features, functionality, and primary operations. For more detailed usage and examples, please refer to the source code and accompanying documentation.