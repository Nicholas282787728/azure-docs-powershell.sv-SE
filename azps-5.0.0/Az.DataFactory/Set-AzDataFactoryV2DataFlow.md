---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320839"
---
# <span data-ttu-id="c3180-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="c3180-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="c3180-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3180-102">SYNOPSIS</span></span>
<span data-ttu-id="c3180-103">Skapar ett data flöde i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="c3180-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="c3180-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3180-104">SYNTAX</span></span>

### <span data-ttu-id="c3180-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="c3180-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3180-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3180-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3180-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3180-107">DESCRIPTION</span></span>
<span data-ttu-id="c3180-108">Set-AzDataFactoryV2DataFlow-cmdleten skapar ett data flöde eller uppdaterar ett befintligt data flöde i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c3180-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="c3180-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3180-109">EXAMPLES</span></span>

### <span data-ttu-id="c3180-110">Exempel 1: skapa ett data flöde</span><span class="sxs-lookup"><span data-stu-id="c3180-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="c3180-111">Det här kommandot skapar ett data flöde med namnet TaxiDemo1 i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c3180-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="c3180-112">Kommandot baserar data flödet på informationen i TaxiDemo1.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="c3180-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="c3180-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3180-113">PARAMETERS</span></span>

### <span data-ttu-id="c3180-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c3180-114">-DataFactoryName</span></span>
<span data-ttu-id="c3180-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="c3180-115">The data factory name.</span></span>

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

### <span data-ttu-id="c3180-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3180-116">-DefaultProfile</span></span>
<span data-ttu-id="c3180-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3180-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3180-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c3180-118">-DefinitionFile</span></span>
<span data-ttu-id="c3180-119">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="c3180-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3180-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c3180-120">-Force</span></span>
<span data-ttu-id="c3180-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3180-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c3180-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3180-122">-Name</span></span>
<span data-ttu-id="c3180-123">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="c3180-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3180-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3180-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3180-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c3180-125">The resource group name.</span></span>

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

### <span data-ttu-id="c3180-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3180-126">-ResourceId</span></span>
<span data-ttu-id="c3180-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="c3180-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c3180-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3180-128">-Confirm</span></span>
<span data-ttu-id="c3180-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3180-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3180-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3180-130">-WhatIf</span></span>
<span data-ttu-id="c3180-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3180-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3180-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3180-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3180-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3180-133">CommonParameters</span></span>
<span data-ttu-id="c3180-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3180-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3180-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3180-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3180-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3180-136">INPUTS</span></span>

### <span data-ttu-id="c3180-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c3180-137">System.String</span></span>

## <span data-ttu-id="c3180-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3180-138">OUTPUTS</span></span>

### <span data-ttu-id="c3180-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="c3180-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="c3180-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3180-140">NOTES</span></span>
<span data-ttu-id="c3180-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="c3180-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c3180-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3180-142">RELATED LINKS</span></span>

[<span data-ttu-id="c3180-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c3180-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="c3180-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c3180-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
