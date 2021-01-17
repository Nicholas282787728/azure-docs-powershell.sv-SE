---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408723"
---
# <span data-ttu-id="ddc51-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ddc51-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ddc51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddc51-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc51-103">Inaktive ras en rörledning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ddc51-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="ddc51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddc51-104">SYNTAX</span></span>

### <span data-ttu-id="ddc51-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ddc51-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc51-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ddc51-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc51-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddc51-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc51-108">Cmdleten **suspend-AzDataFactoryPipeline** inaktive ras en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ddc51-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="ddc51-109">Du kan återuppta pipeline genom att använda Resume-AzDataFactoryPipeline cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc51-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="ddc51-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddc51-110">EXAMPLES</span></span>

### <span data-ttu-id="ddc51-111">Exempel 1: pausa en rörledning</span><span class="sxs-lookup"><span data-stu-id="ddc51-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ddc51-112">Det här kommandot gör att pipelinen med namnet DPWikiSample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ddc51-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ddc51-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="ddc51-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ddc51-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddc51-114">PARAMETERS</span></span>

### <span data-ttu-id="ddc51-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ddc51-115">-DataFactory</span></span>
<span data-ttu-id="ddc51-116">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ddc51-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ddc51-117">Denna cmdlet avbryter en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ddc51-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddc51-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ddc51-118">-DataFactoryName</span></span>
<span data-ttu-id="ddc51-119">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ddc51-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ddc51-120">Denna cmdlet avbryter en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ddc51-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddc51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc51-121">-DefaultProfile</span></span>
<span data-ttu-id="ddc51-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ddc51-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddc51-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddc51-123">-Name</span></span>
<span data-ttu-id="ddc51-124">Anger namnet på den rörledning som ska avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="ddc51-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="ddc51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc51-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddc51-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ddc51-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ddc51-127">Denna cmdlet avbryter en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ddc51-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddc51-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddc51-128">-Confirm</span></span>
<span data-ttu-id="ddc51-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddc51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc51-130">-WhatIf</span></span>
<span data-ttu-id="ddc51-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddc51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc51-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddc51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc51-133">CommonParameters</span></span>
<span data-ttu-id="ddc51-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc51-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc51-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc51-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddc51-136">INPUTS</span></span>

### <span data-ttu-id="ddc51-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc51-137">System.String</span></span>

### <span data-ttu-id="ddc51-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ddc51-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ddc51-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddc51-139">OUTPUTS</span></span>

### <span data-ttu-id="ddc51-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddc51-140">System.Boolean</span></span>

## <span data-ttu-id="ddc51-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddc51-141">NOTES</span></span>
* <span data-ttu-id="ddc51-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="ddc51-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ddc51-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddc51-143">RELATED LINKS</span></span>

[<span data-ttu-id="ddc51-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ddc51-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="ddc51-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ddc51-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ddc51-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ddc51-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="ddc51-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ddc51-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="ddc51-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ddc51-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


