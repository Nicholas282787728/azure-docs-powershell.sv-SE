---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320900"
---
# <span data-ttu-id="39f51-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="39f51-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="39f51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39f51-102">SYNOPSIS</span></span>
<span data-ttu-id="39f51-103">Tar bort ett data flöde från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="39f51-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="39f51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39f51-104">SYNTAX</span></span>

### <span data-ttu-id="39f51-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="39f51-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39f51-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="39f51-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f51-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39f51-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39f51-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39f51-108">DESCRIPTION</span></span>
<span data-ttu-id="39f51-109">Remove-AzDataFactoryV2DataFlow-cmdleten tar bort ett data flöde från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="39f51-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="39f51-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39f51-110">EXAMPLES</span></span>

### <span data-ttu-id="39f51-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39f51-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="39f51-112">Det här kommandot tar bort data flödet med namnet dataflow5 från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="39f51-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="39f51-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39f51-113">PARAMETERS</span></span>

### <span data-ttu-id="39f51-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="39f51-114">-DataFactoryName</span></span>
<span data-ttu-id="39f51-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="39f51-115">The data factory name.</span></span>

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

### <span data-ttu-id="39f51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f51-116">-DefaultProfile</span></span>
<span data-ttu-id="39f51-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39f51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f51-118">-Force</span><span class="sxs-lookup"><span data-stu-id="39f51-118">-Force</span></span>
<span data-ttu-id="39f51-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="39f51-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="39f51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39f51-120">-InputObject</span></span>
<span data-ttu-id="39f51-121">Data flödes objekt.</span><span class="sxs-lookup"><span data-stu-id="39f51-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f51-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="39f51-122">-Name</span></span>
<span data-ttu-id="39f51-123">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="39f51-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f51-124">-ResourceGroupName</span></span>
<span data-ttu-id="39f51-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="39f51-125">The resource group name.</span></span>

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

### <span data-ttu-id="39f51-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f51-126">-ResourceId</span></span>
<span data-ttu-id="39f51-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="39f51-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f51-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39f51-128">-PassThru</span></span>
<span data-ttu-id="39f51-129">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="39f51-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="39f51-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="39f51-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="39f51-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39f51-131">-Confirm</span></span>
<span data-ttu-id="39f51-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39f51-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f51-133">-WhatIf</span></span>
<span data-ttu-id="39f51-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39f51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f51-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39f51-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f51-136">CommonParameters</span></span>
<span data-ttu-id="39f51-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f51-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39f51-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f51-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39f51-139">INPUTS</span></span>

### <span data-ttu-id="39f51-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="39f51-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="39f51-141">System. String</span><span class="sxs-lookup"><span data-stu-id="39f51-141">System.String</span></span>

## <span data-ttu-id="39f51-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39f51-142">OUTPUTS</span></span>

### <span data-ttu-id="39f51-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="39f51-143">System.Void</span></span>

### <span data-ttu-id="39f51-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39f51-144">System.Boolean</span></span>

## <span data-ttu-id="39f51-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39f51-145">NOTES</span></span>
<span data-ttu-id="39f51-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="39f51-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="39f51-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39f51-147">RELATED LINKS</span></span>

[<span data-ttu-id="39f51-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="39f51-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="39f51-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="39f51-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

