# Predicting System Availability with Monte Carlo Simulations
This Python script conducts Monte Carlo simulations to predict system availability based on provided data.

## JSON Data Files
To run the simulations, ensure that the following JSON files are located in the same directory as this notebook.

### components.json
This file contains information about the system components. It consists of two arrays: one containing the names of the components and the other their respective availabilities.

For example, for two components:
```
{
    "name": ["Azure Active Directory B2C", "CosmosDb" ],
    "availability": ["0.9999", "0.9999"]       
}
```

### maintenance.json
This file provides information about scheduled maintenance periods. It includes three arrays:

1. Maintenance names
2. Start time of the scheduled maintenance in the format '%d.%m.%Y %H:%M', e.g., '1.3.2024 9:00'
3. Duration of the maintenance in hours

For example:
```
{
    "name": ["IoT Edge H1", "IoT Edge H2"],
    "start": ["1.3.2024 9:00", "1.9.2024 9:00"],
    "duration": ["5","5"]
}
```

By organizing the data in this manner, the script can effectively conduct availability predictions through Monte Carlo simulations.
