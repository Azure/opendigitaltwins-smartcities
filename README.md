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


#### General Pricinciples

- Driven-by-implementation approach: the ontology will focus on IoT driven use cases and validated in practice via [Azure Digital Twins]().
- Leverage open source royalty-free standards. Please see [Licensing and Credits]().
- Open contribution. Contributuon is open to anybody. Please see [contributions guidlines]().


## Smart Cities ontology approach overview

WE collaborated with [Open Agile Smart Cities (OASC)](https://oascities.org/) and [Sirus](https://sirus.be/) to provide DTDL-based onotlogy, starting with [ETSI CIM NGSI-LD](https://www.etsi.org/deliver/etsi_gs/CIM/001_099/006/01.01.01_60/gs_CIM006v010101p.pdf), and accelerate accelerate development of digital twins-based solutions for smart cities.

In addition to ETSI NGSI-LD, we’ve also evaluated Saref4City, CityGML, ISO and others. 

The ETSI CIM NGSI-LD specification defines an open framework for context information exchange named NGSI-LD which comes with an information model that defines the meaning of the most needed terms, and a domain-specific extension to model any information. The core meta-model provides a basis for representing property graphs using RDF/RDFS/OWL, and is formed of Entities, their Relationships, and their Properties with values, encoded in JSON-LD. In addition to the core meta-model, NGSI-LD compliant open models for aspects of smart cities have been defined by organizations and projects, including OASC, FIWARE, GSMA and the Synchronicity project. The NGSI-LD models for Smart Cites comprise models in the domains of Mobility, Environment, Waste, Parking, Building, Park, Port, etc. 

The property graph nature of NGSI-LD made it quite straightforward to map it to DTDL, and with today’s release, we are making an initial set of DTDL models adapted from the NGSI-LD open models for Smart Cities available to the community

#### Information Model Mapping 

The NGSI-LD core meta-model provides a formal basis for representing property graphs using RDF/RDFS/OWL. It represents Entities, their Relationships, and their Properties with values, encoded in JSON-LD. 

The following table shows NGSI-LD core meta-model and mapping to DTDL.

| NGSI-LD     | DTDL                              |
|-------------------|--------------------------------------------|
| `Entity`             | [`Interface`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#interface)|
| `Relationship`      | [`Relationship`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#relationship) [`Component`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#component)    |
| `Property`    | [`Property`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#property) [`Telemetry`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#telemetry)|
| N/A| [`Command`](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#command) |




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

Outline step-by-step instructions to execute the sample and see its output. Include steps for executing the sample from the IDE, starting specific services in the Azure portal or anything related to the overall launch of the code.

### Prerequisities 
Outline the required components and tools that a user might need to have on their machine in order to run the sample. This can be anything from frameworks, SDKs, OS versions or IDE releases.

### Key concepts

Provide users with more context on the tools and services used in the sample. Explain some of the code that is being used and how services interact with each other.


### Set up 
Explain how to prepare the sample once the user clones or downloads the repository. The section should outline every step necessary to install dependencies and set up any settings (for example, API keys and output folders).


# Modeling guidelines 
Before creating new entities, [check if they exist already in the repo](https://github.com/Azure/opendigitaltwins-smartcities). You can look under each folder based on the use cases (e.g Environment, Mobility, etc.).

To learn how to adopt the ontology for your project, refer to [How to use the ontology]().

## Sytanx 
- Use English terms, preferably American English.
- Use camel case syntax for attribute names (`camelcase`).
- Entity Type names must start with a Capital letter, for example: `Streetlight`.
- Use names and not verbs for Attributes of type Property, for example: `totalSpotNumber`, `dateIssued`.
- Use verbs for Relationship and optional an object, for example: `hasStop`, `operatedBy`.

## Data Types
DTDL provides a full set of [primitive data types, along with support for a variety of complex schemas](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#schemas).


## Validation 
Use the [DTDL Validator tool](https://docs.microsoft.com/en-us/samples/azure-samples/dtdl-validator/dtdl-validator/) to validate the model document to make sure the DTDL is valid.


# Contributing

This project welcomes contributions and suggestions.  

<!--  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

-->

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
