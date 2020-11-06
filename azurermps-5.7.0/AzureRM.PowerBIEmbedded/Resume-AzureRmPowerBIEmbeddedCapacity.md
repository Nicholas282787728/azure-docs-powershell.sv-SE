---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573408"
---
# <span data-ttu-id="4cf6a-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cf6a-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4cf6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf6a-103">Återupptar en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="4cf6a-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cf6a-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="4cf6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cf6a-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf6a-106">Resume-AzureRmPowerBIEmbeddedCapacity cmdlet återupptar en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="4cf6a-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4cf6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cf6a-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf6a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4cf6a-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="4cf6a-109">Det här kommandot återupptar en pausad kapacitet som heter testcapacity i resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="4cf6a-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="4cf6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cf6a-110">PARAMETERS</span></span>

### <span data-ttu-id="4cf6a-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cf6a-111">-Name</span></span>
<span data-ttu-id="4cf6a-112">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="4cf6a-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4cf6a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf6a-113">-ResourceGroupName</span></span>
<span data-ttu-id="4cf6a-114">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="4cf6a-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4cf6a-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf6a-115">-ResourceId</span></span>
<span data-ttu-id="4cf6a-116">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="4cf6a-116">Azure resource ID</span></span>

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

### <span data-ttu-id="4cf6a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf6a-117">-InputObject</span></span>
<span data-ttu-id="4cf6a-118">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="4cf6a-118">Input object for Piping</span></span>

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

### <span data-ttu-id="4cf6a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cf6a-119">-Confirm</span></span>
<span data-ttu-id="4cf6a-120">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="4cf6a-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4cf6a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf6a-121">-WhatIf</span></span>
<span data-ttu-id="4cf6a-122">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="4cf6a-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4cf6a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf6a-123">CommonParameters</span></span>
<span data-ttu-id="4cf6a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf6a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf6a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf6a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf6a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cf6a-126">INPUTS</span></span>

### <span data-ttu-id="4cf6a-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="4cf6a-127">None</span></span>
<span data-ttu-id="4cf6a-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4cf6a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4cf6a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cf6a-129">OUTPUTS</span></span>

### <span data-ttu-id="4cf6a-130">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cf6a-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4cf6a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cf6a-131">NOTES</span></span>

## <span data-ttu-id="4cf6a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cf6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4cf6a-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cf6a-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4cf6a-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4cf6a-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
