---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574711"
---
# <span data-ttu-id="1c0d8-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1c0d8-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="1c0d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0d8-103">Återupptar en pausad rörledning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c0d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c0d8-104">SYNTAX</span></span>

### <span data-ttu-id="1c0d8-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="1c0d8-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c0d8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1c0d8-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c0d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c0d8-107">DESCRIPTION</span></span>
<span data-ttu-id="1c0d8-108">Cmdleten **Resume-AzureRmDataFactoryPipeline** återupptar en pausad pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="1c0d8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c0d8-109">EXAMPLES</span></span>

### <span data-ttu-id="1c0d8-110">Exempel 1: återuppta en rörledning</span><span class="sxs-lookup"><span data-stu-id="1c0d8-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1c0d8-111">Det här kommandot återupptar pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1c0d8-112">Använd cmdleten **suspend-AzureRmDataFactoryPipeline** för att skjuta upp en rörledning.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="1c0d8-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="1c0d8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c0d8-114">PARAMETERS</span></span>

### <span data-ttu-id="1c0d8-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c0d8-115">-DataFactory</span></span>
<span data-ttu-id="1c0d8-116">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1c0d8-117">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c0d8-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c0d8-118">-DataFactoryName</span></span>
<span data-ttu-id="1c0d8-119">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1c0d8-120">Denna cmdlet återupptar en pipeline som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c0d8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c0d8-121">-Name</span></span>
<span data-ttu-id="1c0d8-122">Anger namnet på pipeline till Fortsätt.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="1c0d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c0d8-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1c0d8-125">Denna cmdlet återupptar en pipeline som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c0d8-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c0d8-126">-Confirm</span></span>
<span data-ttu-id="1c0d8-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0d8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0d8-128">-WhatIf</span></span>
<span data-ttu-id="1c0d8-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0d8-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0d8-131">-DefaultProfile</span></span>
<span data-ttu-id="1c0d8-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c0d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0d8-133">CommonParameters</span></span>
<span data-ttu-id="1c0d8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0d8-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0d8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0d8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c0d8-136">INPUTS</span></span>

## <span data-ttu-id="1c0d8-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c0d8-137">OUTPUTS</span></span>

### <span data-ttu-id="1c0d8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c0d8-138">System.Boolean</span></span>

## <span data-ttu-id="1c0d8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c0d8-139">NOTES</span></span>
* <span data-ttu-id="1c0d8-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="1c0d8-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1c0d8-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c0d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c0d8-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1c0d8-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1c0d8-143">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1c0d8-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1c0d8-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1c0d8-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1c0d8-145">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1c0d8-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1c0d8-146">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1c0d8-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


