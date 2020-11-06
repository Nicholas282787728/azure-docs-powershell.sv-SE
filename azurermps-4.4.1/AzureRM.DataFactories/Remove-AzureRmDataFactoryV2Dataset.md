---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 36ee24fea327828247336d7f9c983515ced9deb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579735"
---
# <span data-ttu-id="2df13-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2df13-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="2df13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2df13-102">SYNOPSIS</span></span>
<span data-ttu-id="2df13-103">Tar bort en data uppsättning från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2df13-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2df13-104">SYNTAX</span></span>

### <span data-ttu-id="2df13-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="2df13-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2df13-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2df13-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2df13-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2df13-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2df13-108">DESCRIPTION</span></span>
<span data-ttu-id="2df13-109">Remove-AzureRmDataFactoryV2Dataset cmdlet tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2df13-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="2df13-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2df13-110">EXAMPLES</span></span>

### <span data-ttu-id="2df13-111">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="2df13-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="2df13-112">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2df13-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="2df13-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="2df13-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="2df13-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2df13-114">PARAMETERS</span></span>

### <span data-ttu-id="2df13-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2df13-115">-Confirm</span></span>
<span data-ttu-id="2df13-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2df13-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df13-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2df13-117">-DataFactoryName</span></span>
<span data-ttu-id="2df13-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2df13-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2df13-119">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2df13-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2df13-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2df13-120">-InputObject</span></span>
<span data-ttu-id="2df13-121">Anger ett DataSet-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2df13-121">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="2df13-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2df13-122">-Force</span></span>
<span data-ttu-id="2df13-123">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2df13-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2df13-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="2df13-124">-Name</span></span>
<span data-ttu-id="2df13-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2df13-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="2df13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df13-126">-ResourceGroupName</span></span>
<span data-ttu-id="2df13-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="2df13-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2df13-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2df13-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2df13-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2df13-129">-ResourceId</span></span>
<span data-ttu-id="2df13-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="2df13-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2df13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df13-131">-WhatIf</span></span>
<span data-ttu-id="2df13-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2df13-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2df13-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df13-133">-DefaultProfile</span></span>
<span data-ttu-id="2df13-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2df13-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2df13-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df13-135">CommonParameters</span></span>
<span data-ttu-id="2df13-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df13-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df13-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df13-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df13-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2df13-138">INPUTS</span></span>

### <span data-ttu-id="2df13-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="2df13-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="2df13-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2df13-140">System.String</span></span>

## <span data-ttu-id="2df13-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2df13-141">OUTPUTS</span></span>

### <span data-ttu-id="2df13-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="2df13-142">System.Object</span></span>

## <span data-ttu-id="2df13-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2df13-143">NOTES</span></span>
<span data-ttu-id="2df13-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="2df13-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2df13-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2df13-145">RELATED LINKS</span></span>

[<span data-ttu-id="2df13-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2df13-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="2df13-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2df13-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
