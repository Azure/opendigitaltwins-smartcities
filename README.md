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

# Digital Twins Definition Language (DTDL) based ontology for Smart Cities

<!-- 
Guidelines on README format: https://review.docs.microsoft.com/help/onboard/admin/samples/concepts/readme-template?branch=master

Guidance on onboarding samples to docs.microsoft.com/samples: https://review.docs.microsoft.com/help/onboard/admin/samples/process/onboarding?branch=master

Taxonomies for products and languages: https://review.docs.microsoft.com/new-hope/information-architecture/metadata/taxonomies?branch=master
-->

<!-- Give a short description for your sample here. What does it do and why is it important? --> 

The concept of digital twins—a digital representation of real-world environment brought to life with real time data from sensors and other data sources—has entered the realm of smart cities and promises to enable city administrations and urban planners to make better decisions with the help of data integration and visualization from across the urban space. 

Last year, we announced general availability of [Azure Digital Twins](https://azure.microsoft.com/en-us/blog/azure-digital-twins-now-generally-available-create-iot-solutions-that-model-the-real-world/) platform which enables modeling and creating digital representations of connected environments like buildings, factories, farms, energy networks, railways, stadiums, and cities, then bring these entities to life with a live execution environment that integrates IoT and other data sources. 

To drive openness and interoperability, Azure Digital Twins comes with an open modeling language, [Digital Twins Definition Language (DTDL)](https://github.com/Azure/opendigitaltwins-dtdl), which provides flexibility, ease of use, and integration into the rest of the Azure platform. Using DTDL, developers can describe twins in terms of the telemetry they emit, the properties they report or synchronize and the commands they respond to. Most importantly, DTDL also described relationship between twins.

To accelerate development of digital twins solutions, our goal is to provide DTDL-based ontology definition for various domains, which learns from, builds on, and/or uses industry standards, meets the needs of downstream of developers, and will be adopted and/or extended by the industry. 

For smart cities, we started by evaluating a number of existing standards including ETSI CIM NGSI-LD models for Smart Cities, Saref4City, CityGML, ISOm and others. 

### General Pricinciples

- Driven-by-implementation approach: the ontology will focus on IoT driven use cases and validated in practice via [Azure Digital Twins]().
- Leverage open source royalty-free standards. Please see [Licensing and Credits]().
- Open contribution. Contributuon is open to anybody. Please see [contributions guidlines]().


## Ontology Overview
In domains like Smart City, the lack of open and standardized approach for exchange of context information has been recognized as a hinderance to the widespread adoption of smart services. 
A common representation of places, infrastructure, and assets is paramount for interoperability, re-use, and information sharing across multiple applications. 

We worked with our partners at [Sirus](https://sirus.be/) to provide DTDL-based onotlogy, starting with ETSI CIM NGSI-LD models which have been adopted by organizations like [OASC](https://oascities.org/). The resulting open-source DTDL Smart Cities ontology provides common ground for modeling smart cities solutions, accelerate developers time to results, and enable interoperability between DTDL-based solutions from different solution providers. 

The [ETSI Context Information Management](https://etsi.org/images/files/ETSIWhitePapers/etsi_wp31_NGSI_API.pdf) specification defines an open framework for context information exchange named NGSI-LD which comes with an information model that defines the meaning of the most needed terms and provides the tools to create domain-specific extensions to model any information. 

### Information Model Mapping 


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
## Running a Sample

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
- Use camel case syntax for attribute names (camelcase).
- Entity Type names must start with a Capital letter, for example: Streetlight.
- Use names and not verbs for Attributes of type Property, for example: totalSpotNumber, dateIssued.
- Use verbs for Relationship and optional an object, for example: hasStop, operatedBy.

## Data Types
DTDL provides a full set of [primitive data types, along with support for a variety of complex schemas](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md#schemas)


## Validation 
Use the [DTDL Validator tool](https://docs.microsoft.com/en-us/samples/azure-samples/dtdl-validator/dtdl-validator/) to validate the model document to make sure the DTDL is valid.


# Contributing

This project welcomes contributions and suggestions.  

<!--  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

-->
## Modeling conventions

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
