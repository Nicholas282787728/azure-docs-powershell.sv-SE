---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758114"
---
# <span data-ttu-id="8b57e-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8b57e-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="8b57e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b57e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b57e-103">Hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8b57e-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b57e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b57e-104">SYNTAX</span></span>

### <span data-ttu-id="8b57e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8b57e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b57e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8b57e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b57e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b57e-107">DESCRIPTION</span></span>
<span data-ttu-id="8b57e-108">Cmdleten **Get-AzureRmDataFactoryGateway** hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8b57e-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="8b57e-109">Om du anger namnet på en gateway får denna cmdlet information om den gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8b57e-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="8b57e-110">Om du inte anger ett namn får den här cmdleten information om alla gateways för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8b57e-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="8b57e-111">Om du vill lägga till en lokal Microsoft SQL Server som en länkad tjänst i en data fabrik måste du installera en gateway på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="8b57e-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="8b57e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b57e-112">EXAMPLES</span></span>

### <span data-ttu-id="8b57e-113">Exempel 1: Hämta alla logiska gateways i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="8b57e-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="8b57e-114">Med det här kommandot får du information om alla logiska gateways för data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="8b57e-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="8b57e-115">Exempel 2: skaffa en specifik logisk gateway i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="8b57e-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="8b57e-116">Med det här kommandot får du information om den logiska gateway som heter Gateway01 i data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="8b57e-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="8b57e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b57e-117">PARAMETERS</span></span>

### <span data-ttu-id="8b57e-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b57e-118">-DataFactory</span></span>
<span data-ttu-id="8b57e-119">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8b57e-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8b57e-120">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8b57e-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b57e-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b57e-121">-DataFactoryName</span></span>
<span data-ttu-id="8b57e-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8b57e-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8b57e-123">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8b57e-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b57e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b57e-124">-Name</span></span>
<span data-ttu-id="8b57e-125">Anger namnet på den logiska gateway som ska få information om.</span><span class="sxs-lookup"><span data-stu-id="8b57e-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="8b57e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b57e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b57e-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8b57e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8b57e-128">Denna cmdlet får information om logiska gateways som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8b57e-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b57e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b57e-129">-DefaultProfile</span></span>
<span data-ttu-id="8b57e-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b57e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b57e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b57e-131">CommonParameters</span></span>
<span data-ttu-id="8b57e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b57e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b57e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b57e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b57e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b57e-134">INPUTS</span></span>

## <span data-ttu-id="8b57e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b57e-135">OUTPUTS</span></span>

### <span data-ttu-id="8b57e-136">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8b57e-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="8b57e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b57e-137">NOTES</span></span>
* <span data-ttu-id="8b57e-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8b57e-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8b57e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b57e-139">RELATED LINKS</span></span>

[<span data-ttu-id="8b57e-140">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8b57e-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="8b57e-141">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8b57e-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="8b57e-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="8b57e-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


