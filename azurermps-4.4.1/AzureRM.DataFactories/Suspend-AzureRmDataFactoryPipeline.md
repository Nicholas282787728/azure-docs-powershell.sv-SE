---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 52163f9f99a82934ab354f42a49ca77d1c82d7a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756108"
---
# <span data-ttu-id="53276-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="53276-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="53276-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53276-102">SYNOPSIS</span></span>
<span data-ttu-id="53276-103">Inaktive ras en rörledning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="53276-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53276-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53276-104">SYNTAX</span></span>

### <span data-ttu-id="53276-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="53276-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53276-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="53276-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53276-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53276-107">DESCRIPTION</span></span>
<span data-ttu-id="53276-108">Cmdleten **suspend-AzureRmDataFactoryPipeline** inaktive ras en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="53276-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="53276-109">Du kan återuppta pipeline genom att använda Resume-AzureRmDataFactoryPipeline cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53276-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="53276-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53276-110">EXAMPLES</span></span>

### <span data-ttu-id="53276-111">Exempel 1: pausa en rörledning</span><span class="sxs-lookup"><span data-stu-id="53276-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="53276-112">Det här kommandot gör att pipelinen med namnet DPWikiSample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="53276-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="53276-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="53276-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="53276-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53276-114">PARAMETERS</span></span>

### <span data-ttu-id="53276-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="53276-115">-DataFactory</span></span>
<span data-ttu-id="53276-116">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="53276-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="53276-117">Denna cmdlet avbryter en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53276-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="53276-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="53276-118">-DataFactoryName</span></span>
<span data-ttu-id="53276-119">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="53276-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="53276-120">Denna cmdlet avbryter en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53276-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="53276-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="53276-121">-Name</span></span>
<span data-ttu-id="53276-122">Anger namnet på den rörledning som ska avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="53276-122">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="53276-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53276-123">-ResourceGroupName</span></span>
<span data-ttu-id="53276-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="53276-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="53276-125">Denna cmdlet avbryter en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53276-125">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53276-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53276-126">-Confirm</span></span>
<span data-ttu-id="53276-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53276-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53276-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53276-128">-WhatIf</span></span>
<span data-ttu-id="53276-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53276-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53276-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53276-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53276-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53276-131">-DefaultProfile</span></span>
<span data-ttu-id="53276-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53276-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53276-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53276-133">CommonParameters</span></span>
<span data-ttu-id="53276-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53276-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53276-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53276-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53276-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53276-136">INPUTS</span></span>

## <span data-ttu-id="53276-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53276-137">OUTPUTS</span></span>

### <span data-ttu-id="53276-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53276-138">System.Boolean</span></span>

## <span data-ttu-id="53276-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53276-139">NOTES</span></span>
* <span data-ttu-id="53276-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="53276-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="53276-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53276-141">RELATED LINKS</span></span>

[<span data-ttu-id="53276-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="53276-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="53276-143">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="53276-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="53276-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="53276-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="53276-145">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="53276-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="53276-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="53276-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

