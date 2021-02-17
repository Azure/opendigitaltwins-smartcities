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

The concept of digital twins—a digital model and representation of real-world environment brought to life with real time data from sensors and other data sources—has entered the realm of smart cities and promises to enable city administrations and urban planners to make better decisions with the help of data integration and visualization from across the urban space. 

Last year, we announced general availability of [Azure Digital Twins](https://azure.microsoft.com/en-us/blog/azure-digital-twins-now-generally-available-create-iot-solutions-that-model-the-real-world/) platform which enables modeling and creating digital representations of connected environments like buildings, factories, farms, energy networks, railways, stadiums, and cities, then bring these entities to life with a live execution environment that integrates IoT and other data sources. To drive openness and interoperability, Azure Digital Twins comes with an open modeling language, [Digital Twins Definition Language (DTDL)](https://github.com/Azure/opendigitaltwins-dtdl), which provides flexibility, ease of use, and integration into the rest of the Azure platform. Using DTDL, developers can describe entities and their models for digital twins: the telemetry they emit, the properties they report or synchronize, the commands they respond to, and the relationship between them.

To accelerate DTDL based digital twins solutions for smart cities we worked with our partners to provide DTDL-based smart cities ontologies leveraging well-established industry stardards, starting with ETSI CIM NGSI-LD models which have been adopted by organizations like OASC. The goals of the resulting open-source DTDL Smart Cities ontology is to provide common ground for modeling smart cities solutions, accelerate developers time to results, and enable interoperability between DTDL-based solutions from different solution providers. 


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

## Prerequisites

Outline the required components and tools that a user might need to have on their machine in order to run the sample. This can be anything from frameworks, SDKs, OS versions or IDE releases.

## Setup

Explain how to prepare the sample once the user clones or downloads the repository. The section should outline every step necessary to install dependencies and set up any settings (for example, API keys and output folders).

## Running the sample

Outline step-by-step instructions to execute the sample and see its output. Include steps for executing the sample from the IDE, starting specific services in the Azure portal or anything related to the overall launch of the code.

## Key concepts

Provide users with more context on the tools and services used in the sample. Explain some of the code that is being used and how services interact with each other.


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
