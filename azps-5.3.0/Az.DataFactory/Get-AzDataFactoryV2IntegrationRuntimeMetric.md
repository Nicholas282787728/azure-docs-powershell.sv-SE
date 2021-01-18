---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524201"
---
# <span data-ttu-id="5d638-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="5d638-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="5d638-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d638-102">SYNOPSIS</span></span>
<span data-ttu-id="5d638-103">Hämtar Metric-data för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="5d638-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="5d638-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d638-104">SYNTAX</span></span>

### <span data-ttu-id="5d638-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="5d638-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d638-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d638-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d638-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5d638-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d638-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d638-108">DESCRIPTION</span></span>
<span data-ttu-id="5d638-109">Get-AzDataFactoryV2IntegrationRuntimeMetric-cmdleten får Metric-data om integrations körningen i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5d638-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="5d638-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d638-110">EXAMPLES</span></span>

### <span data-ttu-id="5d638-111">Exempel 1: skaffa statistik för kör tids mått</span><span class="sxs-lookup"><span data-stu-id="5d638-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="5d638-112">Det här kommandot visar Metric-data om integrations körningen med namnet ' test-selfhost-IR ' i prenumerationen på resurs gruppen med namnet "RG-test-dfv2" och data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="5d638-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="5d638-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d638-113">PARAMETERS</span></span>

### <span data-ttu-id="5d638-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5d638-114">-DataFactoryName</span></span>
<span data-ttu-id="5d638-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5d638-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d638-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d638-116">-DefaultProfile</span></span>
<span data-ttu-id="5d638-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d638-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d638-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d638-118">-InputObject</span></span>
<span data-ttu-id="5d638-119">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="5d638-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d638-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d638-120">-Name</span></span>
<span data-ttu-id="5d638-121">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="5d638-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d638-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d638-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d638-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5d638-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d638-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d638-124">-ResourceId</span></span>
<span data-ttu-id="5d638-125">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="5d638-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d638-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d638-126">CommonParameters</span></span>
<span data-ttu-id="5d638-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d638-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d638-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d638-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d638-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d638-129">INPUTS</span></span>

### <span data-ttu-id="5d638-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d638-130">System.String</span></span>

### <span data-ttu-id="5d638-131">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5d638-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5d638-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d638-132">OUTPUTS</span></span>

### <span data-ttu-id="5d638-133">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="5d638-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="5d638-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d638-134">NOTES</span></span>

## <span data-ttu-id="5d638-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d638-135">RELATED LINKS</span></span>

[<span data-ttu-id="5d638-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5d638-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

