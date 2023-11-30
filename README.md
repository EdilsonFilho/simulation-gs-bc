# Ground Station Simulation

This simulation showcases the positions of 11 ground stations from the AWS Ground Station, simulated using Matlab Satellite Communication. This project was developed as part of the research work for the IEEE paper titled "Advancements in Satellite Communications."

## Introduction
The simulation presents the spatial positions and interactions of 11 ground stations specifically from the AWS Ground Station. It leverages Matlab Satellite Communication tools to model and visualize the dynamics and communication scenarios between these stations.

## Setup
To run this simulation, it is recommended to use a virtual environment to manage dependencies and ensure compatibility. Please set up a virtual environment and install the necessary dependencies before running the simulation.

### Venv
```sh
souce venv/bin/activate
```
## Pseudo-code (smart contracts)
### Ground station network

```python
Function enterNetwork(characteristics):
    sendMessageToServer("GS_ENTERED", characteristics)
    waitForServerResponse()
    # Logic after entering the network

Function exitNetwork():
    sendMessageToServer("GS_EXITED")
    waitForServerResponse()
    # Logic after exiting the network

Function main():
    characteristics = getGroundStationCharacteristics()
    # Function to obtain GS characteristics
    # Ground station enters the network
    enterNetwork(characteristics)
    # Logic for GS while in the network
    # GS decides to exit the network
    exitNetwork()
    # Logic for GS exiting the network

```
### Firmware update
```
Function firmware_version_check(firmware_version, id_blockchain_satellite):
    id_blockchain = QueryBlockchain(blockchain ID)
    # Query blockchain to check if ID is valid
    if id_blockchain exists:
        latest_version = QueryDatabase(id_blockchain)
        # Query database for latest firmware version
        if firmware version == latest_version:
            return 0
            # No new firmware version
        return 1
        # New firmware version available
    return 0
    # Invalid blockchain ID
```

## Balance recharge
```
Function check_balance(estimatedGas):
    if estimatedGas ≤ balance / 3:
        SendGasBCToWallet(200)
        # Send 200 BC to wallet
        return 1
        # Recharge performed
    return 0
    # No recharge performed
```
### Classify ground station
```
Function ClassifyGroundStation(antennaSize, bandwidth, frequency, angle):
    if antennaSize ≥ 3 meters:
        category = "Large Antenna"
    else if antennaSize ≥ 1 meter:
        category = "Medium Antenna"
    else:
        category = "Small Antenna"
    
    if bandwidth ≥ 100 Mbps:
        category = category + ", High Bandwidth"
    else if bandwidth ≥ 10 Mbps:
        category = category + ", Medium Bandwidth"
    else:
        category = category + ", Low Bandwidth"

    if frequency ≥ 10 GHz:
        category = category + ", High Frequency"
    else if frequency ≥ 1 GHz:
        category = category + ", Medium Frequency"
    else:
        category = category + ", Low Frequency"

    if angle ≤ 10 degrees:
        category = category + ", Narrow Angle"
    else if angle ≤ 45 degrees:
        category = category + ", Medium Angle"
    else:
        category = category + ", Wide Angle"

    return category

```

