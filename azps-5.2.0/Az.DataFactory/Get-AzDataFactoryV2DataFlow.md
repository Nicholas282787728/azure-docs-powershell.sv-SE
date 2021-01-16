---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407427"
---
# <span data-ttu-id="14b13-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="14b13-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="14b13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14b13-102">SYNOPSIS</span></span>
<span data-ttu-id="14b13-103">Hämtar information om data flöden i data fabrik.</span><span class="sxs-lookup"><span data-stu-id="14b13-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="14b13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14b13-104">SYNTAX</span></span>

### <span data-ttu-id="14b13-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="14b13-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b13-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="14b13-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b13-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14b13-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14b13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14b13-108">DESCRIPTION</span></span>
<span data-ttu-id="14b13-109">Get-AzDataFactoryV2DataFlow cmdlet får information om data flöden i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="14b13-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="14b13-110">Om du anger namnet på ett data flöde får denna cmdlet information om det data flödet.</span><span class="sxs-lookup"><span data-stu-id="14b13-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="14b13-111">Om du inte anger ett namn hämtas den här cmdleten information om alla data flöden i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="14b13-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="14b13-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14b13-112">EXAMPLES</span></span>
### <span data-ttu-id="14b13-113">Exempel 1: få information om alla data flöden</span><span class="sxs-lookup"><span data-stu-id="14b13-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="14b13-114">Det här kommandot får information om alla data flöden i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14b13-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="14b13-115">Exempel 2: Hämta information om ett specifikt data flöde</span><span class="sxs-lookup"><span data-stu-id="14b13-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="14b13-116">Med det här kommandot får du information om data flödet med namnet dataflow1 i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14b13-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="14b13-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14b13-117">PARAMETERS</span></span>

### <span data-ttu-id="14b13-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="14b13-118">-DataFactory</span></span>
<span data-ttu-id="14b13-119">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="14b13-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b13-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="14b13-120">-DataFactoryName</span></span>
<span data-ttu-id="14b13-121">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="14b13-121">The data factory name.</span></span>

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

### <span data-ttu-id="14b13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b13-122">-DefaultProfile</span></span>
<span data-ttu-id="14b13-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14b13-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b13-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="14b13-124">-Name</span></span>
<span data-ttu-id="14b13-125">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="14b13-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b13-126">-ResourceGroupName</span></span>
<span data-ttu-id="14b13-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="14b13-127">The resource group name.</span></span>

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

### <span data-ttu-id="14b13-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b13-128">-ResourceId</span></span>
<span data-ttu-id="14b13-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="14b13-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="14b13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b13-130">CommonParameters</span></span>
<span data-ttu-id="14b13-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b13-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14b13-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b13-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14b13-133">INPUTS</span></span>

### <span data-ttu-id="14b13-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14b13-134">System.String</span></span>

### <span data-ttu-id="14b13-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14b13-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="14b13-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14b13-136">OUTPUTS</span></span>

### <span data-ttu-id="14b13-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b13-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="14b13-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14b13-138">NOTES</span></span>
<span data-ttu-id="14b13-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="14b13-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14b13-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14b13-140">RELATED LINKS</span></span>

[<span data-ttu-id="14b13-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b13-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="14b13-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="14b13-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)