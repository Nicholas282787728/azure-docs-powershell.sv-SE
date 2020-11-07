---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: a563d6b0e72c60632d99df2668552b649ffb1662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744696"
---
# <span data-ttu-id="cb0d9-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="cb0d9-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="cb0d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0d9-103">Skapar ett data flöde i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="cb0d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb0d9-104">SYNTAX</span></span>

### <span data-ttu-id="cb0d9-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="cb0d9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb0d9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb0d9-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb0d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb0d9-107">DESCRIPTION</span></span>
<span data-ttu-id="cb0d9-108">Set-AzDataFactoryV2DataFlow-cmdleten skapar ett data flöde eller uppdaterar ett befintligt data flöde i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="cb0d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb0d9-109">EXAMPLES</span></span>

### <span data-ttu-id="cb0d9-110">Exempel 1: skapa ett data flöde</span><span class="sxs-lookup"><span data-stu-id="cb0d9-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="cb0d9-111">Det här kommandot skapar ett data flöde med namnet TaxiDemo1 i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="cb0d9-112">Kommandot baserar data flödet på informationen i TaxiDemo1.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="cb0d9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb0d9-113">PARAMETERS</span></span>

### <span data-ttu-id="cb0d9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb0d9-114">-DataFactoryName</span></span>
<span data-ttu-id="cb0d9-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-115">The data factory name.</span></span>

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

### <span data-ttu-id="cb0d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0d9-116">-DefaultProfile</span></span>
<span data-ttu-id="cb0d9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0d9-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cb0d9-118">-DefinitionFile</span></span>
<span data-ttu-id="cb0d9-119">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-119">The JSON file path.</span></span>

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

### <span data-ttu-id="cb0d9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cb0d9-120">-Force</span></span>
<span data-ttu-id="cb0d9-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cb0d9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb0d9-122">-Name</span></span>
<span data-ttu-id="cb0d9-123">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-123">The data flow name.</span></span>

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

### <span data-ttu-id="cb0d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb0d9-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-125">The resource group name.</span></span>

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

### <span data-ttu-id="cb0d9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb0d9-126">-ResourceId</span></span>
<span data-ttu-id="cb0d9-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cb0d9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb0d9-128">-Confirm</span></span>
<span data-ttu-id="cb0d9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb0d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb0d9-130">-WhatIf</span></span>
<span data-ttu-id="cb0d9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb0d9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb0d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0d9-133">CommonParameters</span></span>
<span data-ttu-id="cb0d9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0d9-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb0d9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0d9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb0d9-136">INPUTS</span></span>

### <span data-ttu-id="cb0d9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cb0d9-137">System.String</span></span>

## <span data-ttu-id="cb0d9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb0d9-138">OUTPUTS</span></span>

### <span data-ttu-id="cb0d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="cb0d9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="cb0d9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb0d9-140">NOTES</span></span>
<span data-ttu-id="cb0d9-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="cb0d9-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb0d9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb0d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="cb0d9-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="cb0d9-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="cb0d9-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="cb0d9-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
