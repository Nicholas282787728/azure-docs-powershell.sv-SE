---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524176"
---
# <span data-ttu-id="78477-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="78477-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="78477-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78477-102">SYNOPSIS</span></span>
<span data-ttu-id="78477-103">Tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="78477-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="78477-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78477-104">SYNTAX</span></span>

### <span data-ttu-id="78477-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="78477-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78477-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="78477-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78477-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78477-107">DESCRIPTION</span></span>
<span data-ttu-id="78477-108">Cmdleten **Remove-AzDataFactoryDataset** tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="78477-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="78477-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78477-109">EXAMPLES</span></span>

### <span data-ttu-id="78477-110">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="78477-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="78477-111">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="78477-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="78477-112">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="78477-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="78477-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78477-113">PARAMETERS</span></span>

### <span data-ttu-id="78477-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78477-114">-DataFactory</span></span>
<span data-ttu-id="78477-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="78477-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="78477-116">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="78477-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78477-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78477-117">-DataFactoryName</span></span>
<span data-ttu-id="78477-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="78477-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="78477-119">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="78477-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78477-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78477-120">-DefaultProfile</span></span>
<span data-ttu-id="78477-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="78477-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78477-122">-Force</span><span class="sxs-lookup"><span data-stu-id="78477-122">-Force</span></span>
<span data-ttu-id="78477-123">Anger att denna cmdlet tar bort en data uppsättning utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="78477-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="78477-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="78477-124">-Name</span></span>
<span data-ttu-id="78477-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="78477-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78477-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78477-126">-ResourceGroupName</span></span>
<span data-ttu-id="78477-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="78477-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="78477-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="78477-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78477-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78477-129">-Confirm</span></span>
<span data-ttu-id="78477-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78477-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78477-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78477-131">-WhatIf</span></span>
<span data-ttu-id="78477-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78477-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78477-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78477-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78477-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78477-134">CommonParameters</span></span>
<span data-ttu-id="78477-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78477-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78477-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78477-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78477-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78477-137">INPUTS</span></span>

### <span data-ttu-id="78477-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78477-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="78477-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78477-139">System.String</span></span>

## <span data-ttu-id="78477-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78477-140">OUTPUTS</span></span>

### <span data-ttu-id="78477-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="78477-141">System.Void</span></span>

## <span data-ttu-id="78477-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78477-142">NOTES</span></span>
* <span data-ttu-id="78477-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="78477-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="78477-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78477-144">RELATED LINKS</span></span>

[<span data-ttu-id="78477-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="78477-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="78477-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="78477-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


