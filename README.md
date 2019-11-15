# api
TrueGivers API enables partners and direct organizations to get up and running easily with Data Stewardship (https://truegivers.com/data-stewardship/).

- Register your testing account
- Add a default payment method to your testing account (use 4242-4242-4242-4242 CVV 444 ZIP 12345 EXP 12/30)
- If you're a partner, write code to create an organization using: POST /organizations BODY {"Name": "Sample Organization"}, otherwise as a direct customer...
- Write code to upload your data using: POST /records BODY name/value pairs of fields defined here: (https://github.com/TrueGivers/api/wiki/Upload-Fields)
- Submit your data for processing using: PUT /records?status=process
- Wait for processing to complete, using: GET /files, looking for the status of 'Completed'
- Download and use all of the data sets available instantly using: GET /records

# Overview
The TrueGivers API exposes all of the functionality of the truegivers.com application (app.truegivers.com) through the same endpoint.  This includes the following services:
- Batch/file processing
- Real-time/record processing

There is no differentiation between the products you can use through the web interface and the API.  The list of products includes:
- Address standardization (CASS/DPV)
- NCOA processing (18/48-month)
- Deceased suppressions
- Data enhancements
  - Individual attributes
  - Household attributes
  - Address attributes
  - Property attributes

# Usage
No additional user name or password is required, but it is considered best practices to setup a new user to handle all API requests.
