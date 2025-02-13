---
title: Get started with the MedTech service - Azure Health Data Services
description: This article describes the basic steps for deploying the MedTech service.
author: msjasteppe
ms.service: healthcare-apis
ms.subservice: fhir
ms.topic: quickstart
ms.date: 04/25/2023
ms.author: jasteppe
ms.custom: mode-api
---

# Get started with the MedTech service 

> [!NOTE]
> [Fast Healthcare Interoperability Resources (FHIR&#174;)](https://www.hl7.org/fhir/) is an open healthcare specification.

This article and diagram outlines the basic steps to get started with the MedTech service in the [Azure Health Data Services](../healthcare-apis-overview.md). These steps may help you analyze the MedTech service deployment options and determine which deployment method is best for you.

As a prerequisite, you need an Azure subscription and have been granted the proper permissions to deploy Azure resource groups and resources. You can follow all the steps, or skip some if you have an existing environment. Also, you can combine all the steps and complete them in Azure PowerShell, Azure CLI, and REST API scripts.

:::image type="content" source="media/get-started/get-started-with-medtech-service.png" alt-text="Diagram showing the MedTech service deployment overview." lightbox="media/get-started/get-started-with-medtech-service.png":::

> [!TIP]
> See the MedTech service article, [Choose a deployment method for the MedTech service](deploy-choose-method.md), for a description of the different deployment methods that can help to simply and automate the deployment of the MedTech service. 

## Deploy resources

After you obtain the required subscription prerequisites, the first step is to create and deploy the MedTech service prerequisite resources:

* Azure resource group.
* Azure Event Hubs namespace and event hub.
* Azure Health Data services workspace.
* Azure Health Data Services FHIR service.

Once the prerequisite resources are available, deploy:
 
* Azure Health Data Services MedTech service.

### Deploy a resource group 

Deploy a [resource group](../../azure-resource-manager/management/manage-resource-groups-portal.md) to contain the prerequisite resources and the MedTech service.

### Deploy an Event Hubs namespace and event hub

Deploy an Event Hubs namespace into the resource group. Event Hubs namespaces are logical containers for event hubs. Once the namespace is deployed, you can deploy an event hub, which the MedTech service reads from. For information about deploying Event Hubs namespaces and event hubs, see [Create an event hub using Azure portal](../../event-hubs/event-hubs-create.md).

### Deploy a workspace

 Deploy a [workspace](../workspace-overview.md). After you create a workspace using the [Azure portal](../healthcare-apis-quickstart.md), a FHIR service and MedTech service can be deployed from the workspace.

### Deploy a FHIR service

Deploy a [FHIR service](../fhir/fhir-portal-quickstart.md) into your resource group using your workspace. The MedTech service persists transformed device data into the FHIR service. 

### Deploy a MedTech service

If you have successfully deployed the prerequisite resources, you're now ready to deploy a [MedTech service](deploy-manual-prerequisites.md) using your workspace.

## Next steps

This article described the basic steps needed to get started using the MedTech service. 

To learn about methods of deploying the MedTech service, see

> [!div class="nextstepaction"]
> [Choose a deployment method for the MedTech service](deploy-new-choose.md)

For an overview of the MedTech service device mapping, see

> [!div class="nextstepaction"]
> [Overview of the MedTech service device mapping](overview-of-device-mapping.md)

For an overview of the MedTech service FHIR destination mapping, see

> [!div class="nextstepaction"]
> [Overview of the MedTech service FHIR destination mapping](overview-of-fhir-destination-mapping.md)

FHIR&#174; is a registered trademark of Health Level Seven International, registered in the U.S. Trademark Office and is used with their permission.
