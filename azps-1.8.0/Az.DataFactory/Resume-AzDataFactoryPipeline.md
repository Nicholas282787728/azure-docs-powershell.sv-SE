---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754352"
---
# <span data-ttu-id="7b483-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7b483-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="7b483-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b483-102">SYNOPSIS</span></span>
<span data-ttu-id="7b483-103">Återupptar en pausad rörledning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="7b483-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="7b483-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b483-104">SYNTAX</span></span>

### <span data-ttu-id="7b483-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="7b483-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b483-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7b483-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b483-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b483-107">DESCRIPTION</span></span>
<span data-ttu-id="7b483-108">Cmdleten **Resume-AzDataFactoryPipeline** återupptar en pausad pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7b483-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="7b483-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b483-109">EXAMPLES</span></span>

### <span data-ttu-id="7b483-110">Exempel 1: återuppta en rörledning</span><span class="sxs-lookup"><span data-stu-id="7b483-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="7b483-111">Det här kommandot återupptar pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7b483-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="7b483-112">Använd cmdleten **suspend-AzDataFactoryPipeline** för att skjuta upp en rörledning.</span><span class="sxs-lookup"><span data-stu-id="7b483-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="7b483-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="7b483-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="7b483-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b483-114">PARAMETERS</span></span>

### <span data-ttu-id="7b483-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b483-115">-DataFactory</span></span>
<span data-ttu-id="7b483-116">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7b483-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7b483-117">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7b483-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b483-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7b483-118">-DataFactoryName</span></span>
<span data-ttu-id="7b483-119">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="7b483-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7b483-120">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7b483-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b483-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b483-121">-DefaultProfile</span></span>
<span data-ttu-id="7b483-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7b483-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b483-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b483-123">-Name</span></span>
<span data-ttu-id="7b483-124">Anger namnet på pipeline till Fortsätt.</span><span class="sxs-lookup"><span data-stu-id="7b483-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="7b483-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b483-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b483-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="7b483-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7b483-127">Denna cmdlet återupptar en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7b483-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b483-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b483-128">-Confirm</span></span>
<span data-ttu-id="7b483-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b483-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b483-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b483-130">-WhatIf</span></span>
<span data-ttu-id="7b483-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b483-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b483-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b483-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b483-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b483-133">CommonParameters</span></span>
<span data-ttu-id="7b483-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b483-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b483-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b483-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b483-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b483-136">INPUTS</span></span>

### <span data-ttu-id="7b483-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7b483-137">System.String</span></span>

### <span data-ttu-id="7b483-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7b483-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="7b483-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b483-139">OUTPUTS</span></span>

### <span data-ttu-id="7b483-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b483-140">System.Boolean</span></span>

## <span data-ttu-id="7b483-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b483-141">NOTES</span></span>
* <span data-ttu-id="7b483-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="7b483-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7b483-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b483-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b483-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7b483-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="7b483-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7b483-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="7b483-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7b483-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="7b483-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="7b483-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="7b483-148">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7b483-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


