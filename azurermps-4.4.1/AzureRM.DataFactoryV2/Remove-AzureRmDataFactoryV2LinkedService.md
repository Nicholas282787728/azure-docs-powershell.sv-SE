---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586568"
---
# <span data-ttu-id="73a81-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="73a81-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="73a81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73a81-102">SYNOPSIS</span></span>
<span data-ttu-id="73a81-103">Tar bort en länkad tjänst från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="73a81-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73a81-104">SYNTAX</span></span>

### <span data-ttu-id="73a81-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="73a81-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73a81-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="73a81-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73a81-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="73a81-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="73a81-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73a81-108">DESCRIPTION</span></span>
<span data-ttu-id="73a81-109">Remove-AzureRmDataFactoryV2LinkedService-cmdleten tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="73a81-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="73a81-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73a81-110">EXAMPLES</span></span>

### <span data-ttu-id="73a81-111">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="73a81-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="73a81-112">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="73a81-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="73a81-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="73a81-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="73a81-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73a81-114">PARAMETERS</span></span>

### <span data-ttu-id="73a81-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73a81-115">-Confirm</span></span>
<span data-ttu-id="73a81-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73a81-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a81-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="73a81-117">-DataFactoryName</span></span>
<span data-ttu-id="73a81-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="73a81-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="73a81-119">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="73a81-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a81-120">-Force</span><span class="sxs-lookup"><span data-stu-id="73a81-120">-Force</span></span>
<span data-ttu-id="73a81-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="73a81-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="73a81-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73a81-122">-InputObject</span></span>
<span data-ttu-id="73a81-123">Anger det LinkedService-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="73a81-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73a81-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="73a81-124">-Name</span></span>
<span data-ttu-id="73a81-125">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="73a81-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="73a81-126">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="73a81-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a81-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a81-127">-ResourceGroupName</span></span>
<span data-ttu-id="73a81-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="73a81-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="73a81-129">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="73a81-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73a81-130">-ResourceId</span></span>
<span data-ttu-id="73a81-131">Azure Resource ID för den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="73a81-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="73a81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a81-132">-WhatIf</span></span>
<span data-ttu-id="73a81-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73a81-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="73a81-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73a81-134">INPUTS</span></span>

### <span data-ttu-id="73a81-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="73a81-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="73a81-136">System. String</span><span class="sxs-lookup"><span data-stu-id="73a81-136">System.String</span></span>


## <span data-ttu-id="73a81-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73a81-137">OUTPUTS</span></span>

### <span data-ttu-id="73a81-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="73a81-138">System.Object</span></span>

## <span data-ttu-id="73a81-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73a81-139">NOTES</span></span>
<span data-ttu-id="73a81-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="73a81-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="73a81-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73a81-141">RELATED LINKS</span></span>
[<span data-ttu-id="73a81-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="73a81-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="73a81-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="73a81-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

