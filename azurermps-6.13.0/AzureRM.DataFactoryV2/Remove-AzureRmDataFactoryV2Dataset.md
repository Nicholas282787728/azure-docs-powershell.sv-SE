---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 86330711dc9b35c85d87543d2b2ee55e9b1d4a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572832"
---
# <span data-ttu-id="c0b77-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0b77-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="c0b77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0b77-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b77-103">Tar bort en data uppsättning från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="c0b77-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0b77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0b77-104">SYNTAX</span></span>

### <span data-ttu-id="c0b77-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="c0b77-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b77-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0b77-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b77-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b77-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b77-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0b77-108">DESCRIPTION</span></span>
<span data-ttu-id="c0b77-109">Remove-AzureRmDataFactoryV2Dataset cmdlet tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c0b77-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="c0b77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0b77-110">EXAMPLES</span></span>

### <span data-ttu-id="c0b77-111">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="c0b77-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="c0b77-112">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c0b77-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="c0b77-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="c0b77-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="c0b77-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0b77-114">PARAMETERS</span></span>

### <span data-ttu-id="c0b77-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0b77-115">-DataFactoryName</span></span>
<span data-ttu-id="c0b77-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="c0b77-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c0b77-117">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c0b77-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b77-118">-DefaultProfile</span></span>
<span data-ttu-id="c0b77-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b77-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0b77-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c0b77-120">-Force</span></span>
<span data-ttu-id="c0b77-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c0b77-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c0b77-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b77-122">-InputObject</span></span>
<span data-ttu-id="c0b77-123">Anger ett DataSet-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c0b77-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b77-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0b77-124">-Name</span></span>
<span data-ttu-id="c0b77-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c0b77-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b77-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0b77-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="c0b77-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c0b77-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c0b77-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b77-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b77-129">-ResourceId</span></span>
<span data-ttu-id="c0b77-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="c0b77-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c0b77-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0b77-131">-Confirm</span></span>
<span data-ttu-id="c0b77-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0b77-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b77-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b77-133">-WhatIf</span></span>
<span data-ttu-id="c0b77-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0b77-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c0b77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b77-135">CommonParameters</span></span>
<span data-ttu-id="c0b77-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b77-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b77-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b77-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0b77-138">INPUTS</span></span>

### <span data-ttu-id="c0b77-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c0b77-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="c0b77-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0b77-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c0b77-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c0b77-141">System.String</span></span>

## <span data-ttu-id="c0b77-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0b77-142">OUTPUTS</span></span>

### <span data-ttu-id="c0b77-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="c0b77-143">System.Void</span></span>

## <span data-ttu-id="c0b77-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0b77-144">NOTES</span></span>
<span data-ttu-id="c0b77-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="c0b77-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c0b77-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0b77-146">RELATED LINKS</span></span>

[<span data-ttu-id="c0b77-147">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0b77-147">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="c0b77-148">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c0b77-148">Set-AzureRmDataFactoryV2Dataset</span></span>]()
