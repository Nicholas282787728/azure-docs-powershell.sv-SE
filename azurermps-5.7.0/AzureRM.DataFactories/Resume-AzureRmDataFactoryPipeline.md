---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 5cf769a02b6a02f0fba9b26df48554d80a406140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574324"
---
# <span data-ttu-id="b8c18-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b8c18-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="b8c18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8c18-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c18-103">Återupptar en pausad rörledning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b8c18-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8c18-104">SYNTAX</span></span>

### <span data-ttu-id="b8c18-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8c18-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c18-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8c18-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c18-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8c18-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c18-108">Cmdleten **Resume-AzureRmDataFactoryPipeline** återupptar en pausad pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b8c18-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="b8c18-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8c18-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c18-110">Exempel 1: återuppta en rörledning</span><span class="sxs-lookup"><span data-stu-id="b8c18-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b8c18-111">Det här kommandot återupptar pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b8c18-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="b8c18-112">Använd cmdleten **suspend-AzureRmDataFactoryPipeline** för att skjuta upp en rörledning.</span><span class="sxs-lookup"><span data-stu-id="b8c18-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="b8c18-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="b8c18-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b8c18-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8c18-114">PARAMETERS</span></span>

### <span data-ttu-id="b8c18-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8c18-115">-DataFactory</span></span>
<span data-ttu-id="b8c18-116">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c18-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b8c18-117">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8c18-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c18-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8c18-118">-DataFactoryName</span></span>
<span data-ttu-id="b8c18-119">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b8c18-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b8c18-120">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8c18-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8c18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c18-121">-DefaultProfile</span></span>
<span data-ttu-id="b8c18-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b8c18-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c18-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8c18-123">-Name</span></span>
<span data-ttu-id="b8c18-124">Anger namnet på pipeline till Fortsätt.</span><span class="sxs-lookup"><span data-stu-id="b8c18-124">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c18-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8c18-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="b8c18-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b8c18-127">Denna cmdlet återupptar en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8c18-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8c18-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8c18-128">-Confirm</span></span>
<span data-ttu-id="b8c18-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8c18-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c18-130">-WhatIf</span></span>
<span data-ttu-id="b8c18-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8c18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c18-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8c18-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c18-133">CommonParameters</span></span>
<span data-ttu-id="b8c18-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c18-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c18-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c18-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8c18-136">INPUTS</span></span>

### <span data-ttu-id="b8c18-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="b8c18-137">None</span></span>
<span data-ttu-id="b8c18-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b8c18-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8c18-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8c18-139">OUTPUTS</span></span>

### <span data-ttu-id="b8c18-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8c18-140">System.Boolean</span></span>

## <span data-ttu-id="b8c18-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8c18-141">NOTES</span></span>
* <span data-ttu-id="b8c18-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b8c18-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8c18-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8c18-143">RELATED LINKS</span></span>

[<span data-ttu-id="b8c18-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b8c18-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b8c18-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b8c18-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b8c18-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b8c18-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="b8c18-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b8c18-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="b8c18-148">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b8c18-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


