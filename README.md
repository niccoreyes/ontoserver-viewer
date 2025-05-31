# Ontoserver FHIR Browser

This project is a simple web-based browser for searching and exploring ValueSets from the Ontoserver FHIR terminology server.

## Features

- Search ValueSets by title using the Ontoserver FHIR API.
- Display search results with ValueSet title, URL, and optional description.
- Expand individual ValueSets to view their contained codes.
- Drill down into codes to see detailed properties and child codes.
- Interactive UI with expandable/collapsible lists for easy navigation.

## How It Works

- The main page (`index.html`) provides a search input box and a search button.
- When a search is performed, it queries the Ontoserver FHIR endpoint (`https://tx.fhirlab.net/fhir`) for ValueSets matching the search term.
- Results are displayed as clickable items. Clicking a ValueSet expands it to show its codes by calling the `$expand` operation on the ValueSet.
- Codes can be further expanded to show detailed properties and child codes by querying the CodeSystem lookup operation.
- The UI uses plain JavaScript and CSS for styling and interactivity.

## Usage

1. Open `index.html` in a modern web browser.
2. Enter a search term (e.g., "blood pressure") and click "Search" or press Enter.
3. Browse the search results and click on any ValueSet to expand and explore its codes.
4. Click on individual codes to view their properties and child codes.

## Technologies

- HTML5
- CSS3
- JavaScript (ES6+)
- Fetch API for HTTP requests
- Ontoserver FHIR Terminology Server API

## Endpoint

The application uses the public Ontoserver FHIR endpoint:

```
https://tx.fhirlab.net/fhir
```

## License

This project is open source and free to use.