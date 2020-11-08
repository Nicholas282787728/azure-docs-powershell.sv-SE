---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927730"
---
# <span data-ttu-id="1e64e-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="1e64e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e64e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e64e-103">Anger beskrivningen för en gateway i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1e64e-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="1e64e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e64e-104">SYNTAX</span></span>

### <span data-ttu-id="1e64e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="1e64e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e64e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1e64e-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e64e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e64e-107">DESCRIPTION</span></span>
<span data-ttu-id="1e64e-108">Cmdleten **set-AzDataFactoryGateway** anger beskrivningen för den angivna gatewayen i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1e64e-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="1e64e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e64e-109">EXAMPLES</span></span>

### <span data-ttu-id="1e64e-110">Exempel 1: Ange en beskrivning för en gateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="1e64e-111">Det här kommandot anger beskrivningen för den gateway som heter ContosoGateway i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1e64e-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="1e64e-112">Parametern Description anger den nya beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="1e64e-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="1e64e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e64e-113">PARAMETERS</span></span>

### <span data-ttu-id="1e64e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e64e-114">-DataFactory</span></span>
<span data-ttu-id="1e64e-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1e64e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1e64e-116">Denna cmdlet anger beskrivningen för den gateway i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1e64e-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e64e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e64e-117">-DataFactoryName</span></span>
<span data-ttu-id="1e64e-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1e64e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1e64e-119">Denna cmdlet anger beskrivningen för den gateway i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1e64e-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e64e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e64e-120">-DefaultProfile</span></span>
<span data-ttu-id="1e64e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1e64e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e64e-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1e64e-122">-Description</span></span>
<span data-ttu-id="1e64e-123">Anger en beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="1e64e-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e64e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e64e-124">-Name</span></span>
<span data-ttu-id="1e64e-125">Anger namnet på den gateway som du vill ange en beskrivning för.</span><span class="sxs-lookup"><span data-stu-id="1e64e-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="1e64e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e64e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e64e-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="1e64e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1e64e-128">Denna cmdlet anger beskrivningen för en gateway som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1e64e-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e64e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e64e-129">CommonParameters</span></span>
<span data-ttu-id="1e64e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e64e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e64e-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e64e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e64e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e64e-132">INPUTS</span></span>

### <span data-ttu-id="1e64e-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1e64e-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1e64e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1e64e-134">System.String</span></span>

## <span data-ttu-id="1e64e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e64e-135">OUTPUTS</span></span>

### <span data-ttu-id="1e64e-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="1e64e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e64e-137">NOTES</span></span>
* <span data-ttu-id="1e64e-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="1e64e-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1e64e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e64e-139">RELATED LINKS</span></span>

[<span data-ttu-id="1e64e-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="1e64e-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="1e64e-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1e64e-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

