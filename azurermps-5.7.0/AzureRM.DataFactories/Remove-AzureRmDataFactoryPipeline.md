---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574323"
---
# <span data-ttu-id="f8faa-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f8faa-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="f8faa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8faa-102">SYNOPSIS</span></span>
<span data-ttu-id="f8faa-103">Tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8faa-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8faa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8faa-104">SYNTAX</span></span>

### <span data-ttu-id="f8faa-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="f8faa-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8faa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f8faa-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8faa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8faa-107">DESCRIPTION</span></span>
<span data-ttu-id="f8faa-108">Cmdleten **Remove-AzureRmDataFactoryPipeline** tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8faa-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f8faa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8faa-109">EXAMPLES</span></span>

### <span data-ttu-id="f8faa-110">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="f8faa-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="f8faa-111">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f8faa-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="f8faa-112">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="f8faa-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f8faa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8faa-113">PARAMETERS</span></span>

### <span data-ttu-id="f8faa-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8faa-114">-DataFactory</span></span>
<span data-ttu-id="f8faa-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f8faa-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f8faa-116">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f8faa-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8faa-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f8faa-117">-DataFactoryName</span></span>
<span data-ttu-id="f8faa-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f8faa-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f8faa-119">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f8faa-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8faa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8faa-120">-DefaultProfile</span></span>
<span data-ttu-id="f8faa-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f8faa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8faa-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f8faa-122">-Force</span></span>
<span data-ttu-id="f8faa-123">Anger att denna cmdlet tar bort en rörledning utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f8faa-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f8faa-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8faa-124">-Name</span></span>
<span data-ttu-id="f8faa-125">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f8faa-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="f8faa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8faa-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8faa-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f8faa-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f8faa-128">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f8faa-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8faa-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8faa-129">-Confirm</span></span>
<span data-ttu-id="f8faa-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8faa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8faa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8faa-131">-WhatIf</span></span>
<span data-ttu-id="f8faa-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8faa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8faa-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8faa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8faa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8faa-134">CommonParameters</span></span>
<span data-ttu-id="f8faa-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8faa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8faa-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8faa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8faa-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8faa-137">INPUTS</span></span>

### <span data-ttu-id="f8faa-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8faa-138">None</span></span>
<span data-ttu-id="f8faa-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f8faa-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8faa-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8faa-140">OUTPUTS</span></span>

### <span data-ttu-id="f8faa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8faa-141">System.Boolean</span></span>

## <span data-ttu-id="f8faa-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8faa-142">NOTES</span></span>
* <span data-ttu-id="f8faa-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f8faa-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8faa-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8faa-144">RELATED LINKS</span></span>

[<span data-ttu-id="f8faa-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f8faa-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f8faa-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f8faa-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f8faa-147">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f8faa-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f8faa-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f8faa-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f8faa-149">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f8faa-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


