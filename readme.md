# Argentina States and Localities

This repository contains JSON files that provide data on the states and localities of Argentina. The dataset is structured into two main files:

- `argentina-states.json`: Contains a list of the states/provinces in Argentina, each with a unique code and name.
- `argentina_localities.json`: Contains a list of localities within each state, also identified by a state code and locality name.

## File Descriptions

### `argentina-states.json`
This file provides an array of state objects. Each object represents a state in Argentina and includes the following fields:
- `code`: A unique code for the state (e.g., "BSA" for Buenos Aires).
- `name`: The full name of the state (e.g., "Buenos Aires").

Example entry:

{
  "code": "BSA",
  "name": "Buenos Aires"
}
argentina_localities.json
This file contains an array of locality objects, where each object represents a locality within a state. The localities are associated with the states through the code field.

Example entry:

{
  "code": "TUC",
  "name": "San Pedro"
}
Usage
These JSON files can be used to build applications that require data on the administrative divisions of Argentina, such as:

Mapping applications.
Government or public service platforms.
Geographic information systems (GIS).
Example Usage in Code
Here’s a simple example of how you might load and parse these JSON files in JavaScript:

const states = require('./argentina-states.json');
const localities = require('./argentina_localities.json');

// Example: Find all localities in a specific state
const stateCode = 'TUC'; // Example: Tucumán
const tucumanLocalities = localities.filter(locality => locality.code === stateCode);

console.log(`Localities in ${stateCode}:`, tucumanLocalities);
Contributing
If you find any errors or have suggestions for additional data or improvements, feel free to open an issue or submit a pull request.
