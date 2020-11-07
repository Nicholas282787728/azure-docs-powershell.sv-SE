---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 9f5bac03f9c1d59e2d2fc271f462e1e08ca6349b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755250"
---
# <span data-ttu-id="8956b-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8956b-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8956b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8956b-102">SYNOPSIS</span></span>
<span data-ttu-id="8956b-103">Tar bort en rörledning från data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8956b-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8956b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8956b-104">SYNTAX</span></span>

### <span data-ttu-id="8956b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8956b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8956b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8956b-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8956b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8956b-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8956b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8956b-108">DESCRIPTION</span></span>
<span data-ttu-id="8956b-109">Remove-AzureRmDataFactoryV2Pipeline cmdlet tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8956b-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8956b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8956b-110">EXAMPLES</span></span>

### <span data-ttu-id="8956b-111">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="8956b-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="8956b-112">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8956b-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="8956b-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="8956b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8956b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8956b-114">PARAMETERS</span></span>

### <span data-ttu-id="8956b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8956b-115">-DataFactoryName</span></span>
<span data-ttu-id="8956b-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8956b-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8956b-117">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8956b-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8956b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8956b-118">-DefaultProfile</span></span>
<span data-ttu-id="8956b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8956b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8956b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8956b-120">-Force</span></span>
<span data-ttu-id="8956b-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8956b-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8956b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8956b-122">-InputObject</span></span>
<span data-ttu-id="8956b-123">Anger ett pipeline-objekt.</span><span class="sxs-lookup"><span data-stu-id="8956b-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="8956b-124">Denna cmdlet tar bort pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8956b-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8956b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="8956b-125">-Name</span></span>
<span data-ttu-id="8956b-126">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8956b-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8956b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8956b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8956b-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8956b-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8956b-129">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8956b-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8956b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8956b-130">-ResourceId</span></span>
<span data-ttu-id="8956b-131">Azure Resource ID för den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8956b-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8956b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8956b-132">-Confirm</span></span>
<span data-ttu-id="8956b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8956b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8956b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8956b-134">-WhatIf</span></span>
<span data-ttu-id="8956b-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8956b-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8956b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8956b-136">CommonParameters</span></span>
<span data-ttu-id="8956b-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8956b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8956b-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8956b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8956b-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8956b-139">INPUTS</span></span>

### <span data-ttu-id="8956b-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8956b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="8956b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8956b-141">System.String</span></span>

## <span data-ttu-id="8956b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8956b-142">OUTPUTS</span></span>

### <span data-ttu-id="8956b-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="8956b-143">System.Object</span></span>

## <span data-ttu-id="8956b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8956b-144">NOTES</span></span>
<span data-ttu-id="8956b-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8956b-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8956b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8956b-146">RELATED LINKS</span></span>

[<span data-ttu-id="8956b-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8956b-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8956b-148">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8956b-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8956b-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8956b-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
