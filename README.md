# Data Service Development Kit Getting Started

Using the Data Service Development Kit app you can develop your own apps based on the Data Service, test your app locally with simulated data to make sure your it behaves the same once you deploy your app to Industrial Edge. - [Data Service Development Kit Getting Started](#data-service-development-kit-getting-started)

- [Data Service Development Kit Getting Started](#data-service-development-kit-getting-started)
  - [Description](#description)
    - [Overview](#overview)
    - [General task](#general-task)
  - [Requirements](#requirements)
    - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Documentation](#documentation)
  - [Application Example](#application-example)
  - [Contribution](#contribution)
  - [License and Legal Information](#license-and-legal-information)

## Description

### Overview

This example introduces the Data Service Device Kit and how to extract data from the Data Service using the available API calls.
The free Development Kit provides you with a Docker Image that launches the Data Service API on the developer's computer and makes it callable. With this tool, you can develop your customer's app entirely without Industrial Edge access on your development computer. Nor do you need to own a real device that provides you with data. With our simulation service, plant data can be simulated without further ado.

- The Development Kit can be started with a few clicks on the development environment
- Immediately testable of your API calls even without access to a real PLC

### General task

The simulation tool - provided by the Development Kit - generates a **Sinus Signal** and stores the data in the **Data Service** container. The Flow of the Node-Red applications accesses the **Data Service** via available API calls and displays the data in a dashboard.

![deploy VFC](docs/graphics/overview.png)  

## Requirements

### Prerequisites

- Data Service Development Kit for Industrial Edge V.1.3.0

You can download the Data Service Development Kit Bundle to your computer from [Siemens Industry Online Support (SIOS ID 109792717)](https://support.industry.siemens.com/cs/ww/en/view/109792717). The bundle includes the following components:

- Docker app: docker-compose.yml
- User documentation
- OpenAPI specification
- Application example
- Docker image
- Data simulator
- MQTT Broker
- Data Service (with external interface (REST API) for non-Siemens applications)

This GitHub-Repository contains:

- adapted [docker-compose.yml](./docker-compose.yml)
- NodeRED flow: [flows.json](./src/NodeRED/flows.json)
- [User documentation](./docs/Visualization_example_value.md#description)

## Installation

The following services must be installed:

- Docker for Linux
  
 > **_NOTE:_**  Linux device is used for this application example

## Usage

The Data Service Development Kit offers you the possibility to make your app  fit for Industrial Edge. Using the integrated API interface, you save your app's data to the Data Service database structure and retrieve it when needed. This means that other apps, such as Performance Insight or Notifier, can easily access the data and use it for themselves.

After the development phase, your app can be handed over to your customer together with the Data Service. In a few steps, the customer connects the Data Service with the already available connectors and thus creates a quick link to his plant.

## Documentation

You can find the further information about the following steps in the [docs](./docs):

- [Visualization of an example sinus in NodeRED](./docs/Visualization_example_value.md#description)

 > **_NOTE - additional Information:_**  If you need more information, you can find them in the user documentation of the [Data Service Development Kit Bundle](https://support.industry.siemens.com/cs/ww/en/view/109792717).

## Application Example

Some examples on how to extract data from Data Service application using the available API calls is provided in the [examples](./examples):

1. _Read and Write Nodes for DataService_

   - [Read Write Subflows Example](./examples/Read_Write_Subflows_Example.md)
   - For **DataService Edge Apps with version < 1.4.0** you need to use the deprecated nodes for V1.3: [Read Write Subflows Example for V1.3](./examples/Read_Write_Subflows_V1.3_Example.md)

2. _Production data extraction and visualization in NodeRED_

   - [Production data extraction and visualization in NodeRED](./examples/Production_data_example.md#description)
   The guide above explains how to extract data from a PLC data source, save data into the **Data Service version >= 1.4.0** database and retrieve them using NodeRED, with the aim of saving the values of the collected data points into a CSV file or exploiting them in other applications for specific purposes.

## Contribution

Thank you for your interest in contributing. Anybody is free to report bugs, unclear documentation, and other problems regarding this repository in the Issues section.
Additionally everybody is free to propose any changes to this repository using Pull Requests.

If you are interested in contributing via Pull Request, please check the [Contribution License Agreement](Siemens_CLA_1.1.pdf) and forward a signed copy to [industrialedge.industry@siemens.com](mailto:industrialedge.industry@siemens.com?subject=CLA%20Agreement%20Industrial-Edge).

## License and Legal Information

Please read the [Legal information](LICENSE.md).
