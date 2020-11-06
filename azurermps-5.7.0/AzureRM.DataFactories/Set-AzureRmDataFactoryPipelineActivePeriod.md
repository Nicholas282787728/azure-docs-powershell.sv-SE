---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 1c6290f21693f599925f34f950256005df8be670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574316"
---
# <span data-ttu-id="bdff2-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="bdff2-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="bdff2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdff2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdff2-103">Konfigurerar den aktiva perioden för data sektorer.</span><span class="sxs-lookup"><span data-stu-id="bdff2-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdff2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdff2-104">SYNTAX</span></span>

### <span data-ttu-id="bdff2-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="bdff2-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdff2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bdff2-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdff2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdff2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdff2-108">Cmdleten **set-AzureRmDataFactoryPipelineActivePeriod** konfigurerar den aktiva perioden för de data sektorer som bearbetas av en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bdff2-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="bdff2-109">Om du använder Set-AzureRmDataFactorySliceStatus cmdlet för att ändra statusen för sektorer för en data mängd kontrollerar du att start tiden och slut tiden för ett segment ligger i den aktiva perioden för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="bdff2-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>

<span data-ttu-id="bdff2-110">När du har skapat en pipeline kan du ange den period då data bearbetning sker.</span><span class="sxs-lookup"><span data-stu-id="bdff2-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="bdff2-111">Att ange den aktiva perioden för en pipeline anger hur länge data sektorerna bearbetas baserat på de **tillgänglighets** egenskaper som har definierats för varje data fabriks data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="bdff2-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="bdff2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdff2-112">EXAMPLES</span></span>

### <span data-ttu-id="bdff2-113">Exempel 1: Konfigurera den aktiva perioden</span><span class="sxs-lookup"><span data-stu-id="bdff2-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="bdff2-114">Det här kommandot konfigurerar den aktiva perioden för de data sektorer som pipelinen heter DPWikisample Processes.</span><span class="sxs-lookup"><span data-stu-id="bdff2-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="bdff2-115">Kommandot tillhandahåller start-och slut punkter för data sektorerna som värden.</span><span class="sxs-lookup"><span data-stu-id="bdff2-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="bdff2-116">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="bdff2-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="bdff2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdff2-117">PARAMETERS</span></span>

### <span data-ttu-id="bdff2-118">-Lös konflikt</span><span class="sxs-lookup"><span data-stu-id="bdff2-118">-AutoResolve</span></span>
<span data-ttu-id="bdff2-119">Anger att denna cmdlet använder automatisk matchning.</span><span class="sxs-lookup"><span data-stu-id="bdff2-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="bdff2-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdff2-120">-DataFactory</span></span>
<span data-ttu-id="bdff2-121">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bdff2-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bdff2-122">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bdff2-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdff2-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bdff2-123">-DataFactoryName</span></span>
<span data-ttu-id="bdff2-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="bdff2-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bdff2-125">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bdff2-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdff2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdff2-126">-DefaultProfile</span></span>
<span data-ttu-id="bdff2-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bdff2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdff2-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="bdff2-128">-EndDateTime</span></span>
<span data-ttu-id="bdff2-129">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bdff2-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="bdff2-130">Data bearbetning inträffar eller data sektorer bearbetas inom den här perioden.</span><span class="sxs-lookup"><span data-stu-id="bdff2-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="bdff2-131">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bdff2-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="bdff2-132">*EndDateTime* måste anges i iso8601 format enligt följande exempel:</span><span class="sxs-lookup"><span data-stu-id="bdff2-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="bdff2-133">2015 – 01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific, normal tid)</span><span class="sxs-lookup"><span data-stu-id="bdff2-133">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="bdff2-134">Standard tids zonen är UTC.</span><span class="sxs-lookup"><span data-stu-id="bdff2-134">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdff2-135">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="bdff2-135">-ForceRecalculate</span></span>
<span data-ttu-id="bdff2-136">Anger att denna cmdlet använder tvingande omberäkning.</span><span class="sxs-lookup"><span data-stu-id="bdff2-136">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="bdff2-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="bdff2-137">-PipelineName</span></span>
<span data-ttu-id="bdff2-138">Anger namnet på pipelinen.</span><span class="sxs-lookup"><span data-stu-id="bdff2-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="bdff2-139">Denna cmdlet anger den aktiva perioden för den pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bdff2-139">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdff2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdff2-140">-ResourceGroupName</span></span>
<span data-ttu-id="bdff2-141">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="bdff2-141">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bdff2-142">Denna cmdlet ändrar den aktiva perioden för en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bdff2-142">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdff2-143">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="bdff2-143">-StartDateTime</span></span>
<span data-ttu-id="bdff2-144">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bdff2-144">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="bdff2-145">Data bearbetning inträffar eller data sektorer bearbetas inom den här perioden.</span><span class="sxs-lookup"><span data-stu-id="bdff2-145">Data processing occurs or data slices are processed within this period.</span></span>

<span data-ttu-id="bdff2-146">*StartDateTime* måste anges i iso8601-formatet.</span><span class="sxs-lookup"><span data-stu-id="bdff2-146">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdff2-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdff2-147">-Confirm</span></span>
<span data-ttu-id="bdff2-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdff2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdff2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdff2-149">-WhatIf</span></span>
<span data-ttu-id="bdff2-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdff2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdff2-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdff2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdff2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdff2-152">CommonParameters</span></span>
<span data-ttu-id="bdff2-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdff2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdff2-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdff2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdff2-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdff2-155">INPUTS</span></span>

### <span data-ttu-id="bdff2-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="bdff2-156">None</span></span>
<span data-ttu-id="bdff2-157">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bdff2-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdff2-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdff2-158">OUTPUTS</span></span>

### <span data-ttu-id="bdff2-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdff2-159">System.Boolean</span></span>

## <span data-ttu-id="bdff2-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdff2-160">NOTES</span></span>
* <span data-ttu-id="bdff2-161">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="bdff2-161">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bdff2-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdff2-162">RELATED LINKS</span></span>

[<span data-ttu-id="bdff2-163">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bdff2-163">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="bdff2-164">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="bdff2-164">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)


