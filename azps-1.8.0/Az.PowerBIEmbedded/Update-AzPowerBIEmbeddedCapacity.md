---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747514"
---
# <span data-ttu-id="7359f-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7359f-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7359f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7359f-102">SYNOPSIS</span></span>
<span data-ttu-id="7359f-103">Ändrar en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="7359f-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7359f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7359f-104">SYNTAX</span></span>

### <span data-ttu-id="7359f-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="7359f-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7359f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7359f-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7359f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7359f-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7359f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7359f-108">DESCRIPTION</span></span>
<span data-ttu-id="7359f-109">Update-AzPowerBIEmbeddedCapacity cmdlet ändrar en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="7359f-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7359f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7359f-110">EXAMPLES</span></span>

### <span data-ttu-id="7359f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7359f-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="7359f-112">Ändrar kapaciteten som heter testcapacity i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 och Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7359f-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="7359f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7359f-113">PARAMETERS</span></span>

### <span data-ttu-id="7359f-114">-Administratör</span><span class="sxs-lookup"><span data-stu-id="7359f-114">-Administrator</span></span>
<span data-ttu-id="7359f-115">En kommaseparerad kapacitets namn att ange som administratör för kapacitet</span><span class="sxs-lookup"><span data-stu-id="7359f-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7359f-116">-DefaultProfile</span></span>
<span data-ttu-id="7359f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7359f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7359f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7359f-118">-InputObject</span></span>
<span data-ttu-id="7359f-119">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="7359f-119">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7359f-120">-Name</span></span>
<span data-ttu-id="7359f-121">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="7359f-121">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7359f-122">-PassThru</span></span>
<span data-ttu-id="7359f-123">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="7359f-123">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7359f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7359f-125">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="7359f-125">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7359f-126">-ResourceId</span></span>
<span data-ttu-id="7359f-127">PowerBI inbyggd kapacitet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7359f-127">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="7359f-128">-Sku</span></span>
<span data-ttu-id="7359f-129">SKU för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="7359f-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7359f-130">-Tag</span></span>
<span data-ttu-id="7359f-131">Par med nyckelord i en hash-tabell uppsättning som taggar på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="7359f-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7359f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7359f-132">-Confirm</span></span>
<span data-ttu-id="7359f-133">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="7359f-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7359f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7359f-134">-WhatIf</span></span>
<span data-ttu-id="7359f-135">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="7359f-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7359f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7359f-136">CommonParameters</span></span>
<span data-ttu-id="7359f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7359f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7359f-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7359f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7359f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7359f-139">INPUTS</span></span>

### <span data-ttu-id="7359f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7359f-140">System.String</span></span>

### <span data-ttu-id="7359f-141">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7359f-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7359f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7359f-142">OUTPUTS</span></span>

### <span data-ttu-id="7359f-143">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7359f-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7359f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7359f-144">NOTES</span></span>

## <span data-ttu-id="7359f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7359f-145">RELATED LINKS</span></span>

[<span data-ttu-id="7359f-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7359f-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7359f-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7359f-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
