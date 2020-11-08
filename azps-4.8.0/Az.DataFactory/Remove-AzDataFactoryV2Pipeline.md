---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260566"
---
# <span data-ttu-id="e30ba-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e30ba-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e30ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e30ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e30ba-103">Tar bort en rörledning från data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e30ba-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="e30ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e30ba-104">SYNTAX</span></span>

### <span data-ttu-id="e30ba-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e30ba-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e30ba-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e30ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e30ba-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e30ba-108">DESCRIPTION</span></span>
<span data-ttu-id="e30ba-109">Remove-AzDataFactoryV2Pipeline cmdlet tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e30ba-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="e30ba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e30ba-110">EXAMPLES</span></span>

### <span data-ttu-id="e30ba-111">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="e30ba-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="e30ba-112">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e30ba-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="e30ba-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="e30ba-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="e30ba-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e30ba-114">PARAMETERS</span></span>

### <span data-ttu-id="e30ba-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e30ba-115">-DataFactoryName</span></span>
<span data-ttu-id="e30ba-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e30ba-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e30ba-117">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e30ba-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e30ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30ba-118">-DefaultProfile</span></span>
<span data-ttu-id="e30ba-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e30ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e30ba-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e30ba-120">-Force</span></span>
<span data-ttu-id="e30ba-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e30ba-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e30ba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e30ba-122">-InputObject</span></span>
<span data-ttu-id="e30ba-123">Anger ett pipeline-objekt.</span><span class="sxs-lookup"><span data-stu-id="e30ba-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="e30ba-124">Denna cmdlet tar bort pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e30ba-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e30ba-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e30ba-125">-Name</span></span>
<span data-ttu-id="e30ba-126">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e30ba-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="e30ba-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e30ba-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e30ba-129">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e30ba-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e30ba-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e30ba-130">-ResourceId</span></span>
<span data-ttu-id="e30ba-131">Azure Resource ID för den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e30ba-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="e30ba-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e30ba-132">-Confirm</span></span>
<span data-ttu-id="e30ba-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e30ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e30ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30ba-134">-WhatIf</span></span>
<span data-ttu-id="e30ba-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e30ba-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e30ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30ba-136">CommonParameters</span></span>
<span data-ttu-id="e30ba-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e30ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30ba-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30ba-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30ba-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e30ba-139">INPUTS</span></span>

### <span data-ttu-id="e30ba-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e30ba-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="e30ba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e30ba-141">System.String</span></span>

## <span data-ttu-id="e30ba-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e30ba-142">OUTPUTS</span></span>

### <span data-ttu-id="e30ba-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e30ba-143">System.Boolean</span></span>

## <span data-ttu-id="e30ba-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e30ba-144">NOTES</span></span>
<span data-ttu-id="e30ba-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e30ba-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e30ba-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e30ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="e30ba-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e30ba-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e30ba-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e30ba-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e30ba-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e30ba-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

