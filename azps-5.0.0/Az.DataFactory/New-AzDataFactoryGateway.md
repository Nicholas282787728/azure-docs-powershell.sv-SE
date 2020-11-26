---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320948"
---
# <span data-ttu-id="a6e10-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a6e10-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="a6e10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6e10-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e10-103">Skapar en gateway för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a6e10-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="a6e10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6e10-104">SYNTAX</span></span>

### <span data-ttu-id="a6e10-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a6e10-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e10-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a6e10-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6e10-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6e10-107">DESCRIPTION</span></span>
<span data-ttu-id="a6e10-108">Cmdleten **New-AzDataFactoryGateway** skapar en gateway i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a6e10-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="a6e10-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6e10-109">EXAMPLES</span></span>

### <span data-ttu-id="a6e10-110">Exempel 1: skapa en gateway</span><span class="sxs-lookup"><span data-stu-id="a6e10-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="a6e10-111">Det här kommandot skapar en gateway med namnet ContosoGateway i data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="a6e10-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="a6e10-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6e10-112">PARAMETERS</span></span>

### <span data-ttu-id="a6e10-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e10-113">-DataFactory</span></span>
<span data-ttu-id="a6e10-114">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a6e10-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a6e10-115">Denna cmdlet skapar en gateway för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6e10-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e10-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a6e10-116">-DataFactoryName</span></span>
<span data-ttu-id="a6e10-117">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a6e10-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a6e10-118">Denna cmdlet skapar en gateway för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6e10-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e10-119">-DefaultProfile</span></span>
<span data-ttu-id="a6e10-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a6e10-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e10-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a6e10-121">-Description</span></span>
<span data-ttu-id="a6e10-122">Anger en beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a6e10-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="a6e10-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6e10-123">-Name</span></span>
<span data-ttu-id="a6e10-124">Anger namnet på den gateway som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a6e10-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="a6e10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e10-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6e10-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a6e10-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a6e10-127">Denna cmdlet skapar en gateway som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6e10-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6e10-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e10-128">CommonParameters</span></span>
<span data-ttu-id="a6e10-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e10-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e10-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e10-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e10-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6e10-131">INPUTS</span></span>

### <span data-ttu-id="a6e10-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6e10-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a6e10-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6e10-133">System.String</span></span>

## <span data-ttu-id="a6e10-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6e10-134">OUTPUTS</span></span>

### <span data-ttu-id="a6e10-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a6e10-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="a6e10-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6e10-136">NOTES</span></span>
* <span data-ttu-id="a6e10-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="a6e10-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a6e10-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6e10-138">RELATED LINKS</span></span>

[<span data-ttu-id="a6e10-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a6e10-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="a6e10-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a6e10-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

