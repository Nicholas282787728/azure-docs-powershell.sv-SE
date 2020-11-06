---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 6e6f444b76b258be576e13efa2f036329bf0fafd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583575"
---
# <span data-ttu-id="8a00b-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8a00b-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="8a00b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a00b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a00b-103">Skapar en gateway för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8a00b-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a00b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a00b-104">SYNTAX</span></span>

### <span data-ttu-id="8a00b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8a00b-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a00b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8a00b-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a00b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a00b-107">DESCRIPTION</span></span>
<span data-ttu-id="8a00b-108">Cmdleten **New-AzureRmDataFactoryGateway** skapar en gateway i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8a00b-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="8a00b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a00b-109">EXAMPLES</span></span>

### <span data-ttu-id="8a00b-110">Exempel 1: skapa en gateway</span><span class="sxs-lookup"><span data-stu-id="8a00b-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="8a00b-111">Det här kommandot skapar en gateway med namnet ContosoGateway i data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="8a00b-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="8a00b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a00b-112">PARAMETERS</span></span>

### <span data-ttu-id="8a00b-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8a00b-113">-DataFactory</span></span>
<span data-ttu-id="8a00b-114">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8a00b-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8a00b-115">Denna cmdlet skapar en gateway för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8a00b-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8a00b-116">-DataFactoryName</span></span>
<span data-ttu-id="8a00b-117">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8a00b-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8a00b-118">Denna cmdlet skapar en gateway för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8a00b-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a00b-119">-DefaultProfile</span></span>
<span data-ttu-id="8a00b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a00b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8a00b-121">-Description</span></span>
<span data-ttu-id="8a00b-122">Anger en beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8a00b-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a00b-123">-Name</span></span>
<span data-ttu-id="8a00b-124">Anger namnet på den gateway som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8a00b-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a00b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a00b-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8a00b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8a00b-127">Denna cmdlet skapar en gateway som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8a00b-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a00b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a00b-128">CommonParameters</span></span>
<span data-ttu-id="8a00b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a00b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a00b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a00b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a00b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a00b-131">INPUTS</span></span>

### <span data-ttu-id="8a00b-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a00b-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8a00b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a00b-133">System.String</span></span>

## <span data-ttu-id="8a00b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a00b-134">OUTPUTS</span></span>

### <span data-ttu-id="8a00b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8a00b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="8a00b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a00b-136">NOTES</span></span>
* <span data-ttu-id="8a00b-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8a00b-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8a00b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a00b-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a00b-139">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8a00b-139">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="8a00b-140">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8a00b-140">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


