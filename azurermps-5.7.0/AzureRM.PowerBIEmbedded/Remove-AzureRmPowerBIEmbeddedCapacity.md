---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756484"
---
# <span data-ttu-id="8972a-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8972a-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8972a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8972a-102">SYNOPSIS</span></span>
<span data-ttu-id="8972a-103">Tar bort en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="8972a-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8972a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8972a-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="8972a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8972a-105">DESCRIPTION</span></span>
<span data-ttu-id="8972a-106">Remove-AzureRmPowerBIEmbeddedCapacity-cmdleten tar bort en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="8972a-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="8972a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8972a-107">EXAMPLES</span></span>

### <span data-ttu-id="8972a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8972a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="8972a-109">Det här kommandot tar bort kapaciteten som heter testcapacity i resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="8972a-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="8972a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8972a-110">PARAMETERS</span></span>

### <span data-ttu-id="8972a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8972a-111">-ResourceGroupName</span></span>
<span data-ttu-id="8972a-112">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="8972a-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8972a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8972a-113">-Name</span></span>
<span data-ttu-id="8972a-114">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="8972a-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8972a-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8972a-115">-ResourceId</span></span>
<span data-ttu-id="8972a-116">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="8972a-116">Azure resource ID</span></span>

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

### <span data-ttu-id="8972a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8972a-117">-InputObject</span></span>
<span data-ttu-id="8972a-118">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="8972a-118">Input object for Piping</span></span>

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

### <span data-ttu-id="8972a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8972a-119">-PassThru</span></span>
<span data-ttu-id="8972a-120">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="8972a-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8972a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8972a-121">-Confirm</span></span>
<span data-ttu-id="8972a-122">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="8972a-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8972a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8972a-123">-WhatIf</span></span>
<span data-ttu-id="8972a-124">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="8972a-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8972a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8972a-125">CommonParameters</span></span>
<span data-ttu-id="8972a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8972a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8972a-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8972a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8972a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8972a-128">INPUTS</span></span>

### <span data-ttu-id="8972a-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="8972a-129">None</span></span>
<span data-ttu-id="8972a-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8972a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8972a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8972a-131">OUTPUTS</span></span>

### <span data-ttu-id="8972a-132">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8972a-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8972a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8972a-133">NOTES</span></span>

## <span data-ttu-id="8972a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8972a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8972a-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8972a-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8972a-136">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8972a-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
