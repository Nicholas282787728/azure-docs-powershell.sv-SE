---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573395"
---
# <span data-ttu-id="d74cb-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d74cb-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d74cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d74cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d74cb-103">Avbryter instansen av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="d74cb-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d74cb-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d74cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d74cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d74cb-106">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet avbryter en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="d74cb-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d74cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d74cb-107">EXAMPLES</span></span>

### <span data-ttu-id="d74cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d74cb-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="d74cb-109">Det här kommandot avaktiverar en aktiv kapacitet som heter testcapacity i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="d74cb-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d74cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d74cb-110">PARAMETERS</span></span>

### <span data-ttu-id="d74cb-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d74cb-111">-Name</span></span>
<span data-ttu-id="d74cb-112">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="d74cb-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d74cb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74cb-113">-ResourceGroupName</span></span>
<span data-ttu-id="d74cb-114">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="d74cb-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d74cb-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74cb-115">-ResourceId</span></span>
<span data-ttu-id="d74cb-116">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="d74cb-116">Azure resource ID</span></span>

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

### <span data-ttu-id="d74cb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74cb-117">-InputObject</span></span>
<span data-ttu-id="d74cb-118">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="d74cb-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74cb-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d74cb-119">-Confirm</span></span>
<span data-ttu-id="d74cb-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="d74cb-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74cb-121">-WhatIf</span></span>
<span data-ttu-id="d74cb-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="d74cb-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74cb-123">CommonParameters</span></span>
<span data-ttu-id="d74cb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74cb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d74cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74cb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d74cb-126">INPUTS</span></span>

### <span data-ttu-id="d74cb-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="d74cb-127">None</span></span>
<span data-ttu-id="d74cb-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d74cb-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d74cb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d74cb-129">OUTPUTS</span></span>

### <span data-ttu-id="d74cb-130">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d74cb-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d74cb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d74cb-131">NOTES</span></span>

## <span data-ttu-id="d74cb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d74cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d74cb-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d74cb-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d74cb-134">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d74cb-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

