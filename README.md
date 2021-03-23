<!-- 
---
page_type: sample
languages:
- csharp
products:
- dotnet
description: "Add 150 character max description"
urlFragment: "update-this-to-unique-url-stub"
---
-->

# Digital Twins Definition Language (DTDL) ontology for Smart Cities

<!-- 
Guidelines on README format: https://review.docs.microsoft.com/help/onboard/admin/samples/concepts/readme-template?branch=master

Guidance on onboarding samples to docs.microsoft.com/samples: https://review.docs.microsoft.com/help/onboard/admin/samples/process/onboarding?branch=master

Taxonomies for products and languages: https://review.docs.microsoft.com/new-hope/information-architecture/metadata/taxonomies?branch=master
-->

<!-- Give a short description for your sample here. What does it do and why is it important? --> 

The concept of digital twins—a digital representation of real-world environment brought to life with real time data from sensors and other data sources—has entered the realm of smart cities and promises to enable city administrations and urban planners to make better decisions with the help of data integration and visualization from across the urban space. 

Last year, we announced general availability of [Azure Digital Twins](https://azure.microsoft.com/en-us/blog/azure-digital-twins-now-generally-available-create-iot-solutions-that-model-the-real-world/) platform which enables modeling and creating digital representations of connected environments like buildings, factories, farms, energy networks, railways, stadiums, and cities, then bring these entities to life with a live execution environment that integrates IoT and other data sources. 


Through our collaboration with [Open Agile Smart Cities (OASC)](https://oascities.org/) and [Sirus](https://sirus.be/) we are excited to make this open-source Smart Cities ontology for building Azure Digital Twins solutions available to the ecosystem. 

### Why ontologies

To drive openness and interoperability, Azure Digital Twins comes with an open modeling language, [Digital Twins Definition Language (DTDL)](https://github.com/Azure/opendigitaltwins-dtdl), which provides flexibility, ease of use, and integration into the rest of the Azure platform. Using DTDL, developers can describe twins in terms of the telemetry they emit, the properties they report or synchronize and the commands they respond to. Most importantly, DTDL also allows describing relationship between twins.

Common representation of places, infrastructure, and assets will be paramount for interoperability and enabling data sharing between multiple domains. It’s our goal to partner with industry experts and provide [DTDL-based ontologies](https://docs.microsoft.com/en-us/azure/digital-twins/concepts-ontologies) which learn from, build on, and/or use industry standards, meet the needs of developers, and are adopted by the industry. The resulting open-source ontologies provide common ground for modeling connected environments, accelerate developers’ time to results, and enable interoperability between DTDL-based solutions from different solution providers. 

<!--
#### General Pricinciples

- Driven-by-implementation approach: the ontology will focus on IoT driven use cases and validated in practice via [Azure Digital Twins]().
- Leverage open source royalty-free standards. Please see [Licensing and Credits]().
- Open contribution. Contributuon is open to anybody. Please see [contributions guidlines]().
!-->

## Smart Cities ontology approach overview

We collaborated with [Open Agile Smart Cities (OASC)](https://oascities.org/) and [Sirus](https://sirus.be/) to provide DTDL-based onotlogy, starting with [ETSI CIM NGSI-LD](https://www.etsi.org/committee/cim), and accelerate accelerate development of digital twins-based solutions for smart cities.
In addition to ETSI NGSI-LD, we’ve also evaluated Saref4City, CityGML, ISO and others. 

The ETSI CIM NGSI-LD specification defines an open framework for context information exchange named NGSI-LD which comes with an information model that defines the meaning of the most needed terms, and a domain-specific extension to model any information. The core meta-model provides a basis for representing property graphs using RDF/RDFS/OWL, and is formed of Entities, their Relationships, and their Properties with values, encoded in JSON-LD. 


#### ETSI NGSI-LD to DTDL Information Model Mapping 

The NGSI-LD core meta-model provides a formal basis for representing property graphs using RDF/RDFS/OWL. It represents Entities, their Relationships, and their Properties with values, encoded in JSON-LD. 

The following table shows NGSI-LD core meta-model and mapping to DTDL.

| NGSI-LD     | DTDL                              |
|-------------------|--------------------------------------------|
| `Entity`             | [`Interface`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#interface)|
| `Relationship`      | [`Relationship`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#relationship) [`Component`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#component)    |
| `Property`    | [`Property`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#property) [`Telemetry`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#telemetry)|
| N/A| [`Command`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#command) |



### ETSI NGSI-LD models for Smart Cities mapped in DTDL

In addition to the core meta-model, NGSI-LD compliant open models for aspects of smart cities have been defined by organizations and projects, including OASC, FIWARE, GSMA and the Synchronicity project. The [NGSI-LD models for Smart Cites](https://github.com/smart-data-models/SmartCities) comprise models in the domains of Mobility, Environment, Waste, Parking, Building, Park, Port, etc. 

The property graph nature of NGSI-LD made it quite straightforward to map it to DTDL, and with today’s release, we are making an initial set of DTDL models adapted from the NGSI-LD open models for Smart Cities available to the community.

![DTDLontologyoverview](https://user-images.githubusercontent.com/33332080/109090778-6e3d9b00-76c8-11eb-9472-8a67e581b3c7.PNG)

Some of the use cases that are increasingly relevant to cities given the availability of IoT devices and sensors are measuring their air quality in a neighborhood, understanding the noise level in a district, the crowd flow in a road segment, traffic flow in a road segment, monitoring on-street parking in parking spots, availability of EV-Charging, or monitoring streetlights and reducing energy consumption.

### Extending for Spatial representation, City Administration and City Object

In addition to the ETSI NGSI-LD, we’ve also started adapting in DTDL the constructs of [ETSI SAREF extension for Smart Cities (Saref4City)](https://www.etsi.org/deliver/etsi_ts/103400_103499/10341004/01.01.01_60/ts_10341004v010101p.pdf) ontology for Topology to represent spatial objects, Administrative Area and City Object modeling. Using Saref4City ontology constructs represented in DTDL allowed us to model city objects like poles, their containment within an administrative area of a city, and linked to the smart models in the domain of mobility, environmental, parking adapted in DTDL from NGSI-LD models for Smart Cities described above. 

#### Example on how to bring it all together
![DTDLsmartcitiesontologyextended](https://user-images.githubusercontent.com/33332080/109098768-bebbf500-76d6-11eb-99ed-f100c06e8ae0.PNG)


<!-- 

## Contents

Outline the file contents of the repository. It helps users navigate the codebase, build configuration and any related assets.

| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `src`             | Sample source code.                        |
| `.gitignore`      | Define what to ignore at commit time.      |
| `CHANGELOG.md`    | List of changes to the sample.             |
| `CONTRIBUTING.md` | Guidelines for contributing to the sample. |
| `README.md`       | This README file.                          |
| `LICENSE`         | The license for the sample.                |


-->
## How To Use

Using these models you can now build Azure Digital Twins based solution and bring it to life in a live execution environment. 

You can use [Azure Digital Twins Explorer](https://docs.microsoft.com/en-us/samples/azure-samples/digital-twins-explorer/digital-twins-explorer/) to create a sample easily: upload models, instantiate entities in a twins graph, visualize the graph and run queries against the graph. See a sample instantiated from this Smart Cities ontology. 

![ADTExplorerexample](https://user-images.githubusercontent.com/33332080/109099646-46563380-76d8-11eb-9af6-7a2cf9999b65.PNG)


<!--
### Prerequisities 
Outline the required components and tools that a user might need to have on their machine in order to run the sample. This can be anything from frameworks, SDKs, OS versions or IDE releases.

### Key concepts

Provide users with more context on the tools and services used in the sample. Explain some of the code that is being used and how services interact with each other.


### Set up 
Explain how to prepare the sample once the user clones or downloads the repository. The section should outline every step necessary to install dependencies and set up any settings (for example, API keys and output folders).

-->

# Contributing 
This project welcomes contributions and suggestions. We've focused on an initial set of models and we welcome you to contribute to extend the initial set of use cases, as well as improve the exsisting models. 

For improvements, please fork this repository, make your changes and send a pull request. 

Pull requests will be evaluated based on the applicability for smart cities scenarios, quality of the proposed interface models, adherence to the modeling conventions used in the repo.

For issues or suggestions, file an issue. 



## Modeling guidelines 
Before creating new entities, [check if they exist already in the repo](https://github.com/Azure/opendigitaltwins-smartcities). You can look under each folder based on the use cases (e.g Environment, Mobility, etc.).

To learn how to adopt the ontology for your project, refer to [How to use the ontology](https://github.com/Azure/opendigitaltwins-smartcities#how-to-use).

## Syntax 
- Use English terms, preferably American English.
- Use camel case syntax for attribute names (`camelcase`).
- Entity Type names must start with a Capital letter, for example: `Streetlight`.
- Use names and not verbs for Attributes of type Property, for example: `totalSpotNumber`, `dateIssued`.
- Use verbs for Relationship and optional an object, for example: `hasStop`, `operatedBy`.

## Data Types
DTDL provides a full set of [primitive data types, along with support for a variety of complex schemas](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#schemas).


## Validation 
Use the [DTDL Validator tool](https://docs.microsoft.com/en-us/samples/azure-samples/dtdl-validator/dtdl-validator/) to validate the model document to make sure the DTDL is valid.


<!--  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.



When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

-->

# Credits 
The NGSI-LD data models in this repository have been adapated to DTDL from the open source [Smart Models repository for Smart Cities](https://github.com/smart-data-models/SmartCities) developed by FIWARE Foundation and TM Forum. For more information on the Smart Data Models please visit [https://smartdatamodels.org](https://smartdatamodels.org/).

# Resources
- Smart Cities Ontology for Digital Twins [Blog post]() and [IoT Show](https://www.youtube.com/watch?v=GrwI4GIp7nI&feature=youtu.be).
- Connecting Urban Environments with IoT and Digital Twins [Blog post](https://azure.microsoft.com/en-us/blog/connecting-urban-environments-with-iot-and-digital-twins/).
- [Azure Digital Twins product page](https://azure.microsoft.com/en-us/services/digital-twins/).
- [Azure Digital Twins documentation](https://docs.microsoft.com/en-us/azure/digital-twins/).
- [Azure Digital Twins Tech Deep Dive](https://www.youtube.com/watch?v=5Ku55g1GQG8&feature=youtu.be).
- [Digital Twins Definition Language specification](https://github.com/Azure/opendigitaltwins-dtdl).
- [DTDL Ontologies](https://docs.microsoft.com/en-us/azure/digital-twins/concepts-ontologies).
- [FIWARE Data Models](https://github.com/smart-data-models).
- [ADT Explorer](https://github.com/Azure-Samples/digital-twins-explorer).


This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
