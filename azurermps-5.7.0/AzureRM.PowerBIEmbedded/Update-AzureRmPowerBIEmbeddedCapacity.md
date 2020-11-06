---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573391"
---
# <span data-ttu-id="940e3-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="940e3-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="940e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="940e3-102">SYNOPSIS</span></span>
<span data-ttu-id="940e3-103">Ändrar en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="940e3-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="940e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="940e3-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="940e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="940e3-105">DESCRIPTION</span></span>
<span data-ttu-id="940e3-106">Update-AzureRmPowerBIEmbeddedCapacity cmdlet ändrar en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="940e3-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="940e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="940e3-107">EXAMPLES</span></span>

### <span data-ttu-id="940e3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="940e3-108">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}

```

<span data-ttu-id="940e3-109">Ändrar kapaciteten som heter testcapacity i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 och Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="940e3-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="940e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="940e3-110">PARAMETERS</span></span>

### <span data-ttu-id="940e3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="940e3-111">-Name</span></span>
<span data-ttu-id="940e3-112">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="940e3-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="940e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="940e3-114">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="940e3-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="940e3-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="940e3-115">-Sku</span></span>
<span data-ttu-id="940e3-116">SKU för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="940e3-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="940e3-117">-Tagg</span><span class="sxs-lookup"><span data-stu-id="940e3-117">-Tag</span></span>
<span data-ttu-id="940e3-118">Par med nyckelord i en hash-tabell uppsättning som taggar på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="940e3-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="940e3-119">-Administratör</span><span class="sxs-lookup"><span data-stu-id="940e3-119">-Administrator</span></span>
<span data-ttu-id="940e3-120">En kommaseparerad kapacitets namn att ange som administratör för kapacitet</span><span class="sxs-lookup"><span data-stu-id="940e3-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="940e3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940e3-121">-ResourceId</span></span>
<span data-ttu-id="940e3-122">PowerBI inbyggd kapacitet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="940e3-122">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="940e3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="940e3-123">-InputObject</span></span>
<span data-ttu-id="940e3-124">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="940e3-124">Input object for Piping</span></span>

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

### <span data-ttu-id="940e3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="940e3-125">-PassThru</span></span>
<span data-ttu-id="940e3-126">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="940e3-126">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="940e3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="940e3-127">-Confirm</span></span>
<span data-ttu-id="940e3-128">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="940e3-128">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="940e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940e3-129">-WhatIf</span></span>
<span data-ttu-id="940e3-130">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="940e3-130">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="940e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940e3-131">CommonParameters</span></span>
<span data-ttu-id="940e3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940e3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940e3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940e3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="940e3-134">INPUTS</span></span>

### <span data-ttu-id="940e3-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="940e3-135">None</span></span>
<span data-ttu-id="940e3-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="940e3-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="940e3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="940e3-137">OUTPUTS</span></span>

### <span data-ttu-id="940e3-138">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="940e3-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="940e3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="940e3-139">NOTES</span></span>

## <span data-ttu-id="940e3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="940e3-140">RELATED LINKS</span></span>

[<span data-ttu-id="940e3-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="940e3-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="940e3-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="940e3-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
