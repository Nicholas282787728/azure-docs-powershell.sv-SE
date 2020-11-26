---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 237e91df7826e1d524e352e9d2502b7edac8c271
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320867"
---
# <span data-ttu-id="52fbe-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="52fbe-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="52fbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="52fbe-103">Återupptar en pausad rörledning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="52fbe-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="52fbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52fbe-104">SYNTAX</span></span>

### <span data-ttu-id="52fbe-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="52fbe-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52fbe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="52fbe-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fbe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="52fbe-108">Cmdleten **Resume-AzDataFactoryPipeline** återupptar en pausad pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="52fbe-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="52fbe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="52fbe-110">Exempel 1: återuppta en rörledning</span><span class="sxs-lookup"><span data-stu-id="52fbe-110">Example 1: Resume a pipeline</span></span>
```powershell
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="52fbe-111">Det här kommandot återupptar pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="52fbe-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="52fbe-112">Använd cmdleten **suspend-AzDataFactoryPipeline** för att skjuta upp en rörledning.</span><span class="sxs-lookup"><span data-stu-id="52fbe-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="52fbe-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="52fbe-113">The command returns a value of $True.</span></span>

### <span data-ttu-id="52fbe-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52fbe-114">Example 2</span></span>

<span data-ttu-id="52fbe-115">Återupptar en pausad rörledning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="52fbe-115">Resumes a suspended pipeline in Data Factory.</span></span> <span data-ttu-id="52fbe-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="52fbe-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Resume-AzDataFactoryPipeline -DataFactory $DataFactory -Name 'DPWikisample'
```

## <span data-ttu-id="52fbe-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52fbe-117">PARAMETERS</span></span>

### <span data-ttu-id="52fbe-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="52fbe-118">-DataFactory</span></span>
<span data-ttu-id="52fbe-119">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="52fbe-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="52fbe-120">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="52fbe-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52fbe-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="52fbe-121">-DataFactoryName</span></span>
<span data-ttu-id="52fbe-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="52fbe-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="52fbe-123">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="52fbe-123">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52fbe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fbe-124">-DefaultProfile</span></span>
<span data-ttu-id="52fbe-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52fbe-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52fbe-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="52fbe-126">-Name</span></span>
<span data-ttu-id="52fbe-127">Anger namnet på pipeline till Fortsätt.</span><span class="sxs-lookup"><span data-stu-id="52fbe-127">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="52fbe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fbe-128">-ResourceGroupName</span></span>
<span data-ttu-id="52fbe-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="52fbe-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="52fbe-130">Denna cmdlet återupptar en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="52fbe-130">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52fbe-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52fbe-131">-Confirm</span></span>
<span data-ttu-id="52fbe-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52fbe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fbe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fbe-133">-WhatIf</span></span>
<span data-ttu-id="52fbe-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52fbe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52fbe-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52fbe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fbe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fbe-136">CommonParameters</span></span>
<span data-ttu-id="52fbe-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fbe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fbe-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fbe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fbe-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52fbe-139">INPUTS</span></span>

### <span data-ttu-id="52fbe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="52fbe-140">System.String</span></span>

### <span data-ttu-id="52fbe-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="52fbe-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="52fbe-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52fbe-142">OUTPUTS</span></span>

### <span data-ttu-id="52fbe-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52fbe-143">System.Boolean</span></span>

## <span data-ttu-id="52fbe-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52fbe-144">NOTES</span></span>
* <span data-ttu-id="52fbe-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="52fbe-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="52fbe-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52fbe-146">RELATED LINKS</span></span>

[<span data-ttu-id="52fbe-147">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="52fbe-147">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="52fbe-148">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="52fbe-148">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="52fbe-149">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="52fbe-149">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="52fbe-150">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="52fbe-150">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="52fbe-151">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="52fbe-151">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

