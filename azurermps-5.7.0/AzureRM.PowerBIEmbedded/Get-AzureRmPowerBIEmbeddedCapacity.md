---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755481"
---
# <span data-ttu-id="4475d-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4475d-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4475d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4475d-102">SYNOPSIS</span></span>
<span data-ttu-id="4475d-103">Hämtar information om en inbäddad PowerBI kapacitet.</span><span class="sxs-lookup"><span data-stu-id="4475d-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4475d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4475d-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="4475d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4475d-105">DESCRIPTION</span></span>
<span data-ttu-id="4475d-106">Get-AzureRmPowerBIEmbeddedCapacity cmdlet får information om en inbäddad kapacitet för PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4475d-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4475d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4475d-107">EXAMPLES</span></span>

### <span data-ttu-id="4475d-108">Exempel 1: få resurs grupp kapacitet</span><span class="sxs-lookup"><span data-stu-id="4475d-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="4475d-109">Det här kommandot får all inbyggd Azure PowerBI-kapacitet i resurs gruppen med namnet testRG</span><span class="sxs-lookup"><span data-stu-id="4475d-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="4475d-110">Exempel 2: skaffa en kapacitet</span><span class="sxs-lookup"><span data-stu-id="4475d-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="4475d-111">Det här kommandot får Azure PowerBI Embedded-kapacitet som heter testcapacity i resurs gruppen "testRG.</span><span class="sxs-lookup"><span data-stu-id="4475d-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="4475d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4475d-112">PARAMETERS</span></span>

### <span data-ttu-id="4475d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4475d-113">-ResourceGroupName</span></span>
<span data-ttu-id="4475d-114">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="4475d-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4475d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4475d-115">-Name</span></span>
<span data-ttu-id="4475d-116">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="4475d-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4475d-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4475d-117">-ResourceId</span></span>
<span data-ttu-id="4475d-118">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="4475d-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4475d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4475d-119">CommonParameters</span></span>
<span data-ttu-id="4475d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4475d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4475d-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4475d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4475d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4475d-122">INPUTS</span></span>

### <span data-ttu-id="4475d-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="4475d-123">None</span></span>
<span data-ttu-id="4475d-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4475d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4475d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4475d-125">OUTPUTS</span></span>

### <span data-ttu-id="4475d-126">List<Microsoft. Azure. kommandon. PowerBI. Models. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="4475d-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="4475d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4475d-127">NOTES</span></span>

## <span data-ttu-id="4475d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4475d-128">RELATED LINKS</span></span>

[<span data-ttu-id="4475d-129">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="4475d-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4475d-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="4475d-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
