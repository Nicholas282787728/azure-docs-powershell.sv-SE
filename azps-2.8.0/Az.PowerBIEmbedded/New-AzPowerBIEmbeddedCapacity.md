---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3f2515a1c1039dbf9ff4a0635111c95a610d9834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919542"
---
# <span data-ttu-id="cb299-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cb299-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cb299-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb299-102">SYNOPSIS</span></span>
<span data-ttu-id="cb299-103">Skapar en ny PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="cb299-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="cb299-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb299-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb299-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb299-105">DESCRIPTION</span></span>
<span data-ttu-id="cb299-106">New-AzPowerBIEmbeddedCapacity-cmdleten skapar en ny PowerBI inbyggd kapacitet</span><span class="sxs-lookup"><span data-stu-id="cb299-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="cb299-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb299-107">EXAMPLES</span></span>

### <span data-ttu-id="cb299-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cb299-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="cb299-109">Skapar en kapacitet som heter testcapacity i Azure-regionen Västra Central USA och i resurs grupp testRG.</span><span class="sxs-lookup"><span data-stu-id="cb299-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="cb299-110">SKU-nivån för kapaciteten är a1.</span><span class="sxs-lookup"><span data-stu-id="cb299-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="cb299-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb299-111">PARAMETERS</span></span>

### <span data-ttu-id="cb299-112">-Administratör</span><span class="sxs-lookup"><span data-stu-id="cb299-112">-Administrator</span></span>
<span data-ttu-id="cb299-113">Ett kommaseparerad namn för att ange som administratör för kapaciteten</span><span class="sxs-lookup"><span data-stu-id="cb299-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb299-114">-DefaultProfile</span></span>
<span data-ttu-id="cb299-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb299-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb299-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="cb299-116">-Location</span></span>
<span data-ttu-id="cb299-117">Azure-regionen där den PowerBI inbäddade kapaciteten är värd</span><span class="sxs-lookup"><span data-stu-id="cb299-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb299-118">-Name</span></span>
<span data-ttu-id="cb299-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="cb299-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb299-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb299-121">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="cb299-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="cb299-122">-Sku</span></span>
<span data-ttu-id="cb299-123">SKU för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="cb299-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cb299-124">-Tag</span></span>
<span data-ttu-id="cb299-125">Par med nyckelord i en hash-tabell uppsättning som taggar på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="cb299-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb299-126">-Confirm</span></span>
<span data-ttu-id="cb299-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="cb299-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb299-128">-WhatIf</span></span>
<span data-ttu-id="cb299-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="cb299-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb299-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb299-130">CommonParameters</span></span>
<span data-ttu-id="cb299-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb299-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb299-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb299-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb299-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb299-133">INPUTS</span></span>

### <span data-ttu-id="cb299-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cb299-134">System.String</span></span>

### <span data-ttu-id="cb299-135">System. string []</span><span class="sxs-lookup"><span data-stu-id="cb299-135">System.String[]</span></span>

### <span data-ttu-id="cb299-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cb299-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cb299-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb299-137">OUTPUTS</span></span>

### <span data-ttu-id="cb299-138">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cb299-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cb299-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb299-139">NOTES</span></span>

## <span data-ttu-id="cb299-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb299-140">RELATED LINKS</span></span>

[<span data-ttu-id="cb299-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cb299-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="cb299-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cb299-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
