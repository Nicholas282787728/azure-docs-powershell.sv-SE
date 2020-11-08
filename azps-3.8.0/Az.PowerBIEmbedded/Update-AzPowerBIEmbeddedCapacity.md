---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092195"
---
# <span data-ttu-id="6220a-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6220a-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6220a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6220a-102">SYNOPSIS</span></span>
<span data-ttu-id="6220a-103">Ändrar en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="6220a-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="6220a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6220a-104">SYNTAX</span></span>

### <span data-ttu-id="6220a-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="6220a-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6220a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6220a-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6220a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6220a-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6220a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6220a-108">DESCRIPTION</span></span>
<span data-ttu-id="6220a-109">Update-AzPowerBIEmbeddedCapacity cmdlet ändrar en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="6220a-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="6220a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6220a-110">EXAMPLES</span></span>

### <span data-ttu-id="6220a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6220a-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="6220a-112">Ändrar kapaciteten som heter testcapacity i resourcegroup testgroup för att ställa in taggarna som KEY1: värde1 and key2: värde2 and Administrator to och testuser1@contoso.com testuser2@contoso.com tjänstens huvud namn: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="6220a-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="6220a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6220a-113">PARAMETERS</span></span>

### <span data-ttu-id="6220a-114">-Administratör</span><span class="sxs-lookup"><span data-stu-id="6220a-114">-Administrator</span></span>
<span data-ttu-id="6220a-115">Ett kommaseparerad namn som ska anges som administratörer på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="6220a-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="6220a-116">För tjänstens huvud namn: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="6220a-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="6220a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6220a-117">-DefaultProfile</span></span>
<span data-ttu-id="6220a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6220a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6220a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6220a-119">-InputObject</span></span>
<span data-ttu-id="6220a-120">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="6220a-120">Input object for Piping</span></span>

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

### <span data-ttu-id="6220a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6220a-121">-Name</span></span>
<span data-ttu-id="6220a-122">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="6220a-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="6220a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6220a-123">-PassThru</span></span>
<span data-ttu-id="6220a-124">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="6220a-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="6220a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6220a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6220a-126">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="6220a-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="6220a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6220a-127">-ResourceId</span></span>
<span data-ttu-id="6220a-128">PowerBI inbyggd kapacitet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6220a-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="6220a-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="6220a-129">-Sku</span></span>
<span data-ttu-id="6220a-130">SKU för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="6220a-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="6220a-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6220a-131">-Tag</span></span>
<span data-ttu-id="6220a-132">Par med nyckelord i en hash-tabell uppsättning som taggar på kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="6220a-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="6220a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6220a-133">-Confirm</span></span>
<span data-ttu-id="6220a-134">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="6220a-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6220a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6220a-135">-WhatIf</span></span>
<span data-ttu-id="6220a-136">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="6220a-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6220a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6220a-137">CommonParameters</span></span>
<span data-ttu-id="6220a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6220a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6220a-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6220a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6220a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6220a-140">INPUTS</span></span>

### <span data-ttu-id="6220a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6220a-141">System.String</span></span>

### <span data-ttu-id="6220a-142">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6220a-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6220a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6220a-143">OUTPUTS</span></span>

### <span data-ttu-id="6220a-144">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6220a-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6220a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6220a-145">NOTES</span></span>

## <span data-ttu-id="6220a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6220a-146">RELATED LINKS</span></span>

[<span data-ttu-id="6220a-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6220a-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6220a-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6220a-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
