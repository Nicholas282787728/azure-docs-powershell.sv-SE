---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575153"
---
# <span data-ttu-id="3ee3f-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ee3f-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ee3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ee3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee3f-103">Hämtar information om en inbäddad PowerBI kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3ee3f-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ee3f-104">SYNTAX</span></span>

### <span data-ttu-id="3ee3f-105">ByCapacityOrResourceGroupOrSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="3ee3f-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee3f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ee3f-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ee3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ee3f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee3f-108">Get-AzureRmPowerBIEmbeddedCapacity cmdlet får information om en inbäddad kapacitet för PowerBI.</span><span class="sxs-lookup"><span data-stu-id="3ee3f-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3ee3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ee3f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ee3f-110">Exempel 1: få resurs grupp kapacitet</span><span class="sxs-lookup"><span data-stu-id="3ee3f-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="3ee3f-111">Det här kommandot får all inbyggd Azure PowerBI-kapacitet i resurs gruppen med namnet testRG</span><span class="sxs-lookup"><span data-stu-id="3ee3f-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="3ee3f-112">Exempel 2: skaffa en kapacitet</span><span class="sxs-lookup"><span data-stu-id="3ee3f-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="3ee3f-113">Det här kommandot får Azure PowerBI Embedded-kapacitet som heter testcapacity i resurs gruppen "testRG.</span><span class="sxs-lookup"><span data-stu-id="3ee3f-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="3ee3f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ee3f-114">PARAMETERS</span></span>

### <span data-ttu-id="3ee3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee3f-115">-DefaultProfile</span></span>
<span data-ttu-id="3ee3f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee3f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ee3f-117">-Name</span></span>
<span data-ttu-id="3ee3f-118">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="3ee3f-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee3f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ee3f-120">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="3ee3f-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee3f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ee3f-121">-ResourceId</span></span>
<span data-ttu-id="3ee3f-122">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="3ee3f-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee3f-123">CommonParameters</span></span>
<span data-ttu-id="3ee3f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee3f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee3f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee3f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ee3f-126">INPUTS</span></span>

### <span data-ttu-id="3ee3f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3ee3f-127">System.String</span></span>

## <span data-ttu-id="3ee3f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ee3f-128">OUTPUTS</span></span>

### <span data-ttu-id="3ee3f-129">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ee3f-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ee3f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ee3f-130">NOTES</span></span>

## <span data-ttu-id="3ee3f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ee3f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ee3f-132">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="3ee3f-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3ee3f-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="3ee3f-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
