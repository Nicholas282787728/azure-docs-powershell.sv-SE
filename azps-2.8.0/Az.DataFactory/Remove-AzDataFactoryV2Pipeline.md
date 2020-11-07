---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 636ba1466eb0c5c0e8fda0433c74ec2291d2db9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744713"
---
# <span data-ttu-id="8be44-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8be44-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8be44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8be44-102">SYNOPSIS</span></span>
<span data-ttu-id="8be44-103">Tar bort en rörledning från data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8be44-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="8be44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8be44-104">SYNTAX</span></span>

### <span data-ttu-id="8be44-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8be44-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be44-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8be44-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be44-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8be44-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8be44-108">DESCRIPTION</span></span>
<span data-ttu-id="8be44-109">Remove-AzDataFactoryV2Pipeline cmdlet tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8be44-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8be44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8be44-110">EXAMPLES</span></span>

### <span data-ttu-id="8be44-111">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="8be44-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="8be44-112">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8be44-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="8be44-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="8be44-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8be44-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8be44-114">PARAMETERS</span></span>

### <span data-ttu-id="8be44-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8be44-115">-DataFactoryName</span></span>
<span data-ttu-id="8be44-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8be44-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8be44-117">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be44-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be44-118">-DefaultProfile</span></span>
<span data-ttu-id="8be44-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8be44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be44-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8be44-120">-Force</span></span>
<span data-ttu-id="8be44-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8be44-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8be44-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be44-122">-InputObject</span></span>
<span data-ttu-id="8be44-123">Anger ett pipeline-objekt.</span><span class="sxs-lookup"><span data-stu-id="8be44-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="8be44-124">Denna cmdlet tar bort pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be44-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be44-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="8be44-125">-Name</span></span>
<span data-ttu-id="8be44-126">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8be44-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8be44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be44-127">-ResourceGroupName</span></span>
<span data-ttu-id="8be44-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8be44-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8be44-129">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be44-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be44-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be44-130">-ResourceId</span></span>
<span data-ttu-id="8be44-131">Azure Resource ID för den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8be44-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8be44-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8be44-132">-Confirm</span></span>
<span data-ttu-id="8be44-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8be44-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be44-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be44-134">-WhatIf</span></span>
<span data-ttu-id="8be44-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8be44-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8be44-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be44-136">CommonParameters</span></span>
<span data-ttu-id="8be44-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be44-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be44-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be44-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be44-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8be44-139">INPUTS</span></span>

### <span data-ttu-id="8be44-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8be44-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="8be44-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8be44-141">System.String</span></span>

## <span data-ttu-id="8be44-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8be44-142">OUTPUTS</span></span>

### <span data-ttu-id="8be44-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8be44-143">System.Boolean</span></span>

## <span data-ttu-id="8be44-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8be44-144">NOTES</span></span>
<span data-ttu-id="8be44-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8be44-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8be44-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8be44-146">RELATED LINKS</span></span>

[<span data-ttu-id="8be44-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8be44-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8be44-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8be44-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8be44-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8be44-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

