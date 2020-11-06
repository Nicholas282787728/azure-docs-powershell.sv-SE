---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 5685fc013639aac49511f56586952552eba20e47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573483"
---
# <span data-ttu-id="53566-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="53566-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="53566-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53566-102">SYNOPSIS</span></span>
<span data-ttu-id="53566-103">Hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="53566-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53566-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53566-104">SYNTAX</span></span>

### <span data-ttu-id="53566-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="53566-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53566-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="53566-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53566-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53566-107">DESCRIPTION</span></span>
<span data-ttu-id="53566-108">Cmdleten **Get-AzureRmDataFactoryGateway** hämtar information om logiska gateways i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="53566-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="53566-109">Om du anger namnet på en gateway får denna cmdlet information om den gatewayen.</span><span class="sxs-lookup"><span data-stu-id="53566-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="53566-110">Om du inte anger ett namn får den här cmdleten information om alla gateways för en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="53566-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="53566-111">Om du vill lägga till en lokal Microsoft SQL Server som en länkad tjänst i en data fabrik måste du installera en gateway på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="53566-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="53566-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53566-112">EXAMPLES</span></span>

### <span data-ttu-id="53566-113">Exempel 1: Hämta alla logiska gateways i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="53566-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="53566-114">Med det här kommandot får du information om alla logiska gateways för data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="53566-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="53566-115">Exempel 2: skaffa en specifik logisk gateway i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="53566-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="53566-116">Med det här kommandot får du information om den logiska gateway som heter Gateway01 i data fabriken med namnet WikiADF i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="53566-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="53566-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53566-117">PARAMETERS</span></span>

### <span data-ttu-id="53566-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="53566-118">-DataFactory</span></span>
<span data-ttu-id="53566-119">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53566-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="53566-120">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53566-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="53566-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="53566-121">-DataFactoryName</span></span>
<span data-ttu-id="53566-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="53566-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="53566-123">Denna cmdlet får information om logiska gateways i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53566-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="53566-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53566-124">-DefaultProfile</span></span>
<span data-ttu-id="53566-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="53566-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53566-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="53566-126">-Name</span></span>
<span data-ttu-id="53566-127">Anger namnet på den logiska gateway som ska få information om.</span><span class="sxs-lookup"><span data-stu-id="53566-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53566-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53566-128">-ResourceGroupName</span></span>
<span data-ttu-id="53566-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="53566-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="53566-130">Denna cmdlet får information om logiska gateways som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53566-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53566-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53566-131">CommonParameters</span></span>
<span data-ttu-id="53566-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53566-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53566-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53566-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53566-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53566-134">INPUTS</span></span>

### <span data-ttu-id="53566-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="53566-135">None</span></span>
<span data-ttu-id="53566-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="53566-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53566-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53566-137">OUTPUTS</span></span>

### <span data-ttu-id="53566-138">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="53566-138">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="53566-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53566-139">NOTES</span></span>
* <span data-ttu-id="53566-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="53566-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="53566-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53566-141">RELATED LINKS</span></span>

[<span data-ttu-id="53566-142">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="53566-142">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="53566-143">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="53566-143">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="53566-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="53566-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


