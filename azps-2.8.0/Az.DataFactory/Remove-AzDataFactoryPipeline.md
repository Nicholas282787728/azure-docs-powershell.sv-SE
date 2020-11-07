---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 6d3353e9f2daead1135b3da4ebde530137d8ae1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744730"
---
# <span data-ttu-id="3285e-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3285e-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="3285e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3285e-102">SYNOPSIS</span></span>
<span data-ttu-id="3285e-103">Tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3285e-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="3285e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3285e-104">SYNTAX</span></span>

### <span data-ttu-id="3285e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3285e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3285e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3285e-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3285e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3285e-107">DESCRIPTION</span></span>
<span data-ttu-id="3285e-108">Cmdleten **Remove-AzDataFactoryPipeline** tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3285e-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="3285e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3285e-109">EXAMPLES</span></span>

### <span data-ttu-id="3285e-110">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="3285e-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="3285e-111">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3285e-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="3285e-112">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="3285e-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="3285e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3285e-113">PARAMETERS</span></span>

### <span data-ttu-id="3285e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3285e-114">-DataFactory</span></span>
<span data-ttu-id="3285e-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3285e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3285e-116">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3285e-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3285e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3285e-117">-DataFactoryName</span></span>
<span data-ttu-id="3285e-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3285e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3285e-119">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3285e-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3285e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3285e-120">-DefaultProfile</span></span>
<span data-ttu-id="3285e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3285e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3285e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3285e-122">-Force</span></span>
<span data-ttu-id="3285e-123">Anger att denna cmdlet tar bort en rörledning utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3285e-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3285e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3285e-124">-Name</span></span>
<span data-ttu-id="3285e-125">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3285e-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3285e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3285e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3285e-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="3285e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3285e-128">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3285e-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3285e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3285e-129">-Confirm</span></span>
<span data-ttu-id="3285e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3285e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3285e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3285e-131">-WhatIf</span></span>
<span data-ttu-id="3285e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3285e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3285e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3285e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3285e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3285e-134">CommonParameters</span></span>
<span data-ttu-id="3285e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3285e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3285e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3285e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3285e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3285e-137">INPUTS</span></span>

### <span data-ttu-id="3285e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3285e-138">System.String</span></span>

### <span data-ttu-id="3285e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3285e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3285e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3285e-140">OUTPUTS</span></span>

### <span data-ttu-id="3285e-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="3285e-141">System.Void</span></span>

## <span data-ttu-id="3285e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3285e-142">NOTES</span></span>
* <span data-ttu-id="3285e-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="3285e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3285e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3285e-144">RELATED LINKS</span></span>

[<span data-ttu-id="3285e-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3285e-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="3285e-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3285e-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="3285e-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3285e-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="3285e-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3285e-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="3285e-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3285e-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


