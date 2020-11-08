---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919545"
---
# <span data-ttu-id="521a1-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="521a1-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="521a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="521a1-102">SYNOPSIS</span></span>
<span data-ttu-id="521a1-103">Hämtar information om en inbäddad PowerBI kapacitet.</span><span class="sxs-lookup"><span data-stu-id="521a1-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="521a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="521a1-104">SYNTAX</span></span>

### <span data-ttu-id="521a1-105">ByCapacityOrResourceGroupOrSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="521a1-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="521a1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="521a1-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="521a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="521a1-107">DESCRIPTION</span></span>
<span data-ttu-id="521a1-108">Get-AzPowerBIEmbeddedCapacity cmdlet får information om en inbäddad kapacitet för PowerBI.</span><span class="sxs-lookup"><span data-stu-id="521a1-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="521a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="521a1-109">EXAMPLES</span></span>

### <span data-ttu-id="521a1-110">Exempel 1: få resurs grupp kapacitet</span><span class="sxs-lookup"><span data-stu-id="521a1-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="521a1-111">Det här kommandot får all inbyggd Azure PowerBI-kapacitet i resurs gruppen med namnet testRG</span><span class="sxs-lookup"><span data-stu-id="521a1-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="521a1-112">Exempel 2: skaffa en kapacitet</span><span class="sxs-lookup"><span data-stu-id="521a1-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="521a1-113">Det här kommandot får Azure PowerBI Embedded-kapacitet som heter testcapacity i resurs gruppen "testRG.</span><span class="sxs-lookup"><span data-stu-id="521a1-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="521a1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="521a1-114">PARAMETERS</span></span>

### <span data-ttu-id="521a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521a1-115">-DefaultProfile</span></span>
<span data-ttu-id="521a1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="521a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521a1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="521a1-117">-Name</span></span>
<span data-ttu-id="521a1-118">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="521a1-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="521a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="521a1-120">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="521a1-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="521a1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="521a1-121">-ResourceId</span></span>
<span data-ttu-id="521a1-122">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="521a1-122">Azure resource ID</span></span>

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

### <span data-ttu-id="521a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521a1-123">CommonParameters</span></span>
<span data-ttu-id="521a1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521a1-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521a1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521a1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="521a1-126">INPUTS</span></span>

### <span data-ttu-id="521a1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="521a1-127">System.String</span></span>

## <span data-ttu-id="521a1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="521a1-128">OUTPUTS</span></span>

### <span data-ttu-id="521a1-129">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="521a1-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="521a1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="521a1-130">NOTES</span></span>

## <span data-ttu-id="521a1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="521a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="521a1-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="521a1-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="521a1-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="521a1-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)