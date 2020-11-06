---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 5239f2143eefe40b777ad1077bbd26d6d645754c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574318"
---
# <span data-ttu-id="f54d9-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="f54d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f54d9-102">SYNOPSIS</span></span>
<span data-ttu-id="f54d9-103">Anger beskrivningen för en gateway i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f54d9-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f54d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f54d9-104">SYNTAX</span></span>

### <span data-ttu-id="f54d9-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="f54d9-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f54d9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f54d9-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f54d9-107">DESCRIPTION</span></span>
<span data-ttu-id="f54d9-108">Cmdleten **set-AzureRmDataFactoryGateway** anger beskrivningen för den angivna gatewayen i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f54d9-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="f54d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f54d9-109">EXAMPLES</span></span>

### <span data-ttu-id="f54d9-110">Exempel 1: Ange en beskrivning för en gateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="f54d9-111">Det här kommandot anger beskrivningen för den gateway som heter ContosoGateway i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f54d9-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="f54d9-112">Parametern Description anger den nya beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="f54d9-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="f54d9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f54d9-113">PARAMETERS</span></span>

### <span data-ttu-id="f54d9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f54d9-114">-DataFactory</span></span>
<span data-ttu-id="f54d9-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f54d9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f54d9-116">Denna cmdlet anger beskrivningen för den gateway i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f54d9-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f54d9-117">-DataFactoryName</span></span>
<span data-ttu-id="f54d9-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f54d9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f54d9-119">Denna cmdlet anger beskrivningen för den gateway i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f54d9-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54d9-120">-DefaultProfile</span></span>
<span data-ttu-id="f54d9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f54d9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f54d9-122">-Description</span></span>
<span data-ttu-id="f54d9-123">Anger en beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f54d9-123">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f54d9-124">-Name</span></span>
<span data-ttu-id="f54d9-125">Anger namnet på den gateway som du vill ange en beskrivning för.</span><span class="sxs-lookup"><span data-stu-id="f54d9-125">Specifies the name of the gateway for which to set a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="f54d9-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f54d9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f54d9-128">Denna cmdlet anger beskrivningen för en gateway som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f54d9-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54d9-129">CommonParameters</span></span>
<span data-ttu-id="f54d9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54d9-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54d9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54d9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f54d9-132">INPUTS</span></span>

### <span data-ttu-id="f54d9-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="f54d9-133">None</span></span>
<span data-ttu-id="f54d9-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f54d9-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f54d9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f54d9-135">OUTPUTS</span></span>

### <span data-ttu-id="f54d9-136">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="f54d9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f54d9-137">NOTES</span></span>
* <span data-ttu-id="f54d9-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f54d9-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f54d9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f54d9-139">RELATED LINKS</span></span>

[<span data-ttu-id="f54d9-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="f54d9-141">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="f54d9-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f54d9-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


