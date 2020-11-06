---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576835"
---
# <span data-ttu-id="3351b-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3351b-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3351b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3351b-102">SYNOPSIS</span></span>
<span data-ttu-id="3351b-103">Skapar en ny PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3351b-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3351b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3351b-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3351b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3351b-105">DESCRIPTION</span></span>
<span data-ttu-id="3351b-106">New-AzureRmPowerBIEmbeddedCapacity-cmdleten skapar en ny PowerBI inbyggd kapacitet</span><span class="sxs-lookup"><span data-stu-id="3351b-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3351b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3351b-107">EXAMPLES</span></span>

### <span data-ttu-id="3351b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3351b-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="3351b-109">Skapar en kapacitet som heter testcapacity i Azure-regionen Västra Central USA och i resurs grupp testRG.</span><span class="sxs-lookup"><span data-stu-id="3351b-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="3351b-110">SKU-nivån för kapaciteten är a1.</span><span class="sxs-lookup"><span data-stu-id="3351b-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="3351b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3351b-111">PARAMETERS</span></span>

### <span data-ttu-id="3351b-112">-Administratör</span><span class="sxs-lookup"><span data-stu-id="3351b-112">-Administrator</span></span>
<span data-ttu-id="3351b-113">En kommaseparerad kapacitets namn att ange som administratör för kapacitet</span><span class="sxs-lookup"><span data-stu-id="3351b-113">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="3351b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3351b-114">-DefaultProfile</span></span>
<span data-ttu-id="3351b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3351b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3351b-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="3351b-116">-Location</span></span>
<span data-ttu-id="3351b-117">Azure-regionen där den PowerBI inbäddade kapaciteten är värd</span><span class="sxs-lookup"><span data-stu-id="3351b-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="3351b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3351b-118">-Name</span></span>
<span data-ttu-id="3351b-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="3351b-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3351b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3351b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3351b-121">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="3351b-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3351b-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="3351b-122">-Sku</span></span>
<span data-ttu-id="3351b-123">SKU för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3351b-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="3351b-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3351b-124">-Tag</span></span>
<span data-ttu-id="3351b-125">Par med nyckelord i en hash-tabell uppsättning som taggar på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="3351b-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="3351b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3351b-126">-Confirm</span></span>
<span data-ttu-id="3351b-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="3351b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3351b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3351b-128">-WhatIf</span></span>
<span data-ttu-id="3351b-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="3351b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3351b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3351b-130">CommonParameters</span></span>
<span data-ttu-id="3351b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3351b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3351b-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3351b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3351b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3351b-133">INPUTS</span></span>

### <span data-ttu-id="3351b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3351b-134">System.String</span></span>

### <span data-ttu-id="3351b-135">System. string []</span><span class="sxs-lookup"><span data-stu-id="3351b-135">System.String[]</span></span>

### <span data-ttu-id="3351b-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3351b-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3351b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3351b-137">OUTPUTS</span></span>

### <span data-ttu-id="3351b-138">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3351b-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3351b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3351b-139">NOTES</span></span>

## <span data-ttu-id="3351b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3351b-140">RELATED LINKS</span></span>

[<span data-ttu-id="3351b-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3351b-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3351b-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3351b-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
