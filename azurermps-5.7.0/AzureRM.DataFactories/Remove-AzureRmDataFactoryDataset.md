---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 35810cf1d190f9ee8ada758fbd2e52fe41ca2455
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573472"
---
# <span data-ttu-id="ff5eb-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff5eb-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="ff5eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5eb-103">Tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff5eb-104">SYNTAX</span></span>

### <span data-ttu-id="ff5eb-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ff5eb-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5eb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff5eb-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff5eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff5eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ff5eb-108">Cmdleten **Remove-AzureRmDataFactoryDataset** tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ff5eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff5eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ff5eb-110">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="ff5eb-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ff5eb-111">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ff5eb-112">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ff5eb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff5eb-113">PARAMETERS</span></span>

### <span data-ttu-id="ff5eb-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff5eb-114">-DataFactory</span></span>
<span data-ttu-id="ff5eb-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ff5eb-116">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5eb-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ff5eb-117">-DataFactoryName</span></span>
<span data-ttu-id="ff5eb-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ff5eb-119">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5eb-120">-DefaultProfile</span></span>
<span data-ttu-id="ff5eb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff5eb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff5eb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ff5eb-122">-Force</span></span>
<span data-ttu-id="ff5eb-123">Anger att denna cmdlet tar bort en data uppsättning utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ff5eb-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff5eb-124">-Name</span></span>
<span data-ttu-id="ff5eb-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff5eb-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff5eb-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff5eb-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff5eb-129">-Confirm</span></span>
<span data-ttu-id="ff5eb-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff5eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5eb-131">-WhatIf</span></span>
<span data-ttu-id="ff5eb-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff5eb-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff5eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5eb-134">CommonParameters</span></span>
<span data-ttu-id="ff5eb-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5eb-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5eb-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff5eb-137">INPUTS</span></span>

### <span data-ttu-id="ff5eb-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff5eb-138">None</span></span>
<span data-ttu-id="ff5eb-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff5eb-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff5eb-140">OUTPUTS</span></span>

### <span data-ttu-id="ff5eb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff5eb-141">System.Boolean</span></span>

## <span data-ttu-id="ff5eb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff5eb-142">NOTES</span></span>
* <span data-ttu-id="ff5eb-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="ff5eb-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff5eb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff5eb-144">RELATED LINKS</span></span>

[<span data-ttu-id="ff5eb-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff5eb-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="ff5eb-146">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff5eb-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


