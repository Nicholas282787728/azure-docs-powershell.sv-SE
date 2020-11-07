---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: da5ae19a03b34a04fc9928d684910e759303cedd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754397"
---
# <span data-ttu-id="645f4-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="645f4-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="645f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="645f4-102">SYNOPSIS</span></span>
<span data-ttu-id="645f4-103">Hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="645f4-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="645f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="645f4-104">SYNTAX</span></span>

### <span data-ttu-id="645f4-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="645f4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="645f4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="645f4-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="645f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="645f4-107">DESCRIPTION</span></span>
<span data-ttu-id="645f4-108">Cmdleten **Get-AzDataFactoryGateway** hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="645f4-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="645f4-109">Om du anger namnet på en gateway får denna cmdlet information om den gatewayen.</span><span class="sxs-lookup"><span data-stu-id="645f4-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="645f4-110">Om du inte anger ett namn får den här cmdleten information om alla gateways för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="645f4-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="645f4-111">Om du vill lägga till en lokal Microsoft SQL Server som en länkad tjänst i en data fabrik måste du installera en gateway på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="645f4-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="645f4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="645f4-112">EXAMPLES</span></span>

### <span data-ttu-id="645f4-113">Exempel 1: Hämta alla logiska gateways i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="645f4-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="645f4-114">Med det här kommandot får du information om alla logiska gateways för data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="645f4-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="645f4-115">Exempel 2: skaffa en specifik logisk gateway i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="645f4-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="645f4-116">Med det här kommandot får du information om den logiska gateway som heter Gateway01 i data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="645f4-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="645f4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="645f4-117">PARAMETERS</span></span>

### <span data-ttu-id="645f4-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="645f4-118">-DataFactory</span></span>
<span data-ttu-id="645f4-119">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="645f4-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="645f4-120">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="645f4-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="645f4-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="645f4-121">-DataFactoryName</span></span>
<span data-ttu-id="645f4-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="645f4-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="645f4-123">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="645f4-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="645f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645f4-124">-DefaultProfile</span></span>
<span data-ttu-id="645f4-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="645f4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="645f4-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="645f4-126">-Name</span></span>
<span data-ttu-id="645f4-127">Anger namnet på den logiska gateway som ska få information om.</span><span class="sxs-lookup"><span data-stu-id="645f4-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="645f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="645f4-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="645f4-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="645f4-130">Denna cmdlet får information om logiska gateways som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="645f4-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="645f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645f4-131">CommonParameters</span></span>
<span data-ttu-id="645f4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645f4-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645f4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645f4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="645f4-134">INPUTS</span></span>

### <span data-ttu-id="645f4-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="645f4-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="645f4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="645f4-136">System.String</span></span>

## <span data-ttu-id="645f4-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="645f4-137">OUTPUTS</span></span>

### <span data-ttu-id="645f4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="645f4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="645f4-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="645f4-139">NOTES</span></span>
* <span data-ttu-id="645f4-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="645f4-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="645f4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="645f4-141">RELATED LINKS</span></span>

[<span data-ttu-id="645f4-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="645f4-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="645f4-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="645f4-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="645f4-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="645f4-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

