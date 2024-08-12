# N20 in Soil Prediction System using Cartesi Rollups

## Description

This project implements a decentralized N2O (nitrous oxide) content prediction system for soil samples using Cartesi Rollups. It allows users to submit soil sample data and receive predictions about the N2O content in the soil. The system demonstrates the implementation of notices and reports in a Cartesi DApp.

### Key Features

- Submit soil sample data (nitrate and organic matter content)
- Predict N20 content based on submitted soil samples
- Retrieve all submitted soil samples
- Retrieve N20 predictions for all samples
- Implements notices for publishing predictions
- Uses reports for data retrieval and error handling

## Installation

1. Clone my cartesi-intro repository:

   ```bash
   git clone https://github.com/Lynette7/cartesi-intro
   cd cartesi-intro
   ```

2. Change the directory into the n2o prediction dapp

    ```bash
   cd n20-prediction
   ```

## Running the DApp

1. In one terminal, build the DApp:

   ```bash
   cartesi build
   ```

2. Then run it:

   ```bash
   cartesi run
   ```

3. Follow the inspect url that is <http://localhost:8080/inspect/>:
   use /predictions route to check predictions for all samples
   use /samples route to check all the submitted soil samples

## Testing the DApp

Test the DApp using the `cartesi send` command. For the send subcommand, choose `Send generic input to the application`. Use default options for all the rest.

### Submitting a Soil Sample

To submit a soil sample, your input as a string should look as follows(a JSON string):
`{"nitrate": 40, "organic_matter": 7}`

## Understanding the Output

- When submitting a soil sample, the DApp will return a notice containing the N20 prediction.
- When retrieving samples or predictions, the DApp will return a report containing the requested data.
- Any errors during processing will be returned as reports.

You can view the DApp's output in the Docker logs or by using the Cartesi Rollups web interface, typically available at `http://localhost:5004/graphql`.
