---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927733"
---
# <span data-ttu-id="2c9b8-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="2c9b8-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="2c9b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9b8-103">Konfigurerar den aktiva perioden för data sektorer.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="2c9b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c9b8-104">SYNTAX</span></span>

### <span data-ttu-id="2c9b8-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="2c9b8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c9b8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2c9b8-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c9b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2c9b8-108">Cmdleten **set-AzDataFactoryPipelineActivePeriod** konfigurerar den aktiva perioden för de data sektorer som bearbetas av en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="2c9b8-109">Om du använder Set-AzDataFactorySliceStatus cmdlet för att ändra statusen för sektorer för en data mängd kontrollerar du att start tiden och slut tiden för ett segment ligger i den aktiva perioden för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="2c9b8-110">När du har skapat en pipeline kan du ange den period då data bearbetning sker.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="2c9b8-111">Att ange den aktiva perioden för en pipeline anger hur länge data sektorerna bearbetas baserat på de **tillgänglighets** egenskaper som har definierats för varje data fabriks data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="2c9b8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-112">EXAMPLES</span></span>

### <span data-ttu-id="2c9b8-113">Exempel 1: Konfigurera den aktiva perioden</span><span class="sxs-lookup"><span data-stu-id="2c9b8-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2c9b8-114">Det här kommandot konfigurerar den aktiva perioden för de data sektorer som pipelinen heter DPWikisample Processes.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="2c9b8-115">Kommandot tillhandahåller start-och slut punkter för data sektorerna som värden.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="2c9b8-116">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="2c9b8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c9b8-117">PARAMETERS</span></span>

### <span data-ttu-id="2c9b8-118">-Lös konflikt</span><span class="sxs-lookup"><span data-stu-id="2c9b8-118">-AutoResolve</span></span>
<span data-ttu-id="2c9b8-119">Anger att denna cmdlet använder automatisk matchning.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="2c9b8-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c9b8-120">-DataFactory</span></span>
<span data-ttu-id="2c9b8-121">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2c9b8-122">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c9b8-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c9b8-123">-DataFactoryName</span></span>
<span data-ttu-id="2c9b8-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2c9b8-125">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c9b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9b8-126">-DefaultProfile</span></span>
<span data-ttu-id="2c9b8-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c9b8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c9b8-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="2c9b8-128">-EndDateTime</span></span>
<span data-ttu-id="2c9b8-129">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="2c9b8-130">Data bearbetning inträffar eller data sektorer bearbetas inom den här perioden.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="2c9b8-131">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2c9b8-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="2c9b8-132">*EndDateTime* måste anges i formatet iso8601 som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time).</span><span class="sxs-lookup"><span data-stu-id="2c9b8-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="2c9b8-133">-ForceRecalculate</span></span>
<span data-ttu-id="2c9b8-134">Anger att denna cmdlet använder tvingande omberäkning.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="2c9b8-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2c9b8-135">-PipelineName</span></span>
<span data-ttu-id="2c9b8-136">Anger namnet på pipelinen.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="2c9b8-137">Denna cmdlet anger den aktiva perioden för den pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9b8-138">-ResourceGroupName</span></span>
<span data-ttu-id="2c9b8-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2c9b8-140">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c9b8-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="2c9b8-141">-StartDateTime</span></span>
<span data-ttu-id="2c9b8-142">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="2c9b8-143">Data bearbetning inträffar eller data sektorer bearbetas inom den här perioden.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="2c9b8-144">*StartDateTime* måste anges i iso8601-formatet.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9b8-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c9b8-145">-Confirm</span></span>
<span data-ttu-id="2c9b8-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9b8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9b8-147">-WhatIf</span></span>
<span data-ttu-id="2c9b8-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9b8-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9b8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9b8-150">CommonParameters</span></span>
<span data-ttu-id="2c9b8-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9b8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9b8-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9b8-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9b8-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c9b8-153">INPUTS</span></span>

### <span data-ttu-id="2c9b8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9b8-154">System.String</span></span>

### <span data-ttu-id="2c9b8-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2c9b8-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2c9b8-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c9b8-156">OUTPUTS</span></span>

### <span data-ttu-id="2c9b8-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c9b8-157">System.Boolean</span></span>

## <span data-ttu-id="2c9b8-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c9b8-158">NOTES</span></span>
* <span data-ttu-id="2c9b8-159">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="2c9b8-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2c9b8-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c9b8-160">RELATED LINKS</span></span>

[<span data-ttu-id="2c9b8-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2c9b8-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="2c9b8-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="2c9b8-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

