---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758424"
---
# <span data-ttu-id="4f832-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="4f832-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="4f832-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f832-102">SYNOPSIS</span></span>
<span data-ttu-id="4f832-103">Hämtar Metric-data för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="4f832-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f832-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f832-104">SYNTAX</span></span>

### <span data-ttu-id="4f832-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="4f832-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="4f832-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f832-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="4f832-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4f832-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="4f832-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f832-108">DESCRIPTION</span></span>
<span data-ttu-id="4f832-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-cmdleten får Metric-data om integrations körningen i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="4f832-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="4f832-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f832-110">EXAMPLES</span></span>

### <span data-ttu-id="4f832-111">Exempel 1: skaffa statistik för kör tids mått</span><span class="sxs-lookup"><span data-stu-id="4f832-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="4f832-112">Det här kommandot visar Metric-data om integrations körningen med namnet ' test-selfhost-IR ' i prenumerationen på resurs gruppen med namnet "RG-test-dfv2" och data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="4f832-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="4f832-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f832-113">PARAMETERS</span></span>

### <span data-ttu-id="4f832-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f832-114">-DataFactoryName</span></span>
<span data-ttu-id="4f832-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="4f832-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f832-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f832-116">-InputObject</span></span>
<span data-ttu-id="4f832-117">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="4f832-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f832-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f832-118">-Name</span></span>
<span data-ttu-id="4f832-119">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="4f832-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f832-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f832-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f832-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4f832-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f832-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f832-122">-ResourceId</span></span>
<span data-ttu-id="4f832-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="4f832-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="4f832-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f832-124">INPUTS</span></span>

### <span data-ttu-id="4f832-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4f832-125">System.String</span></span>
<span data-ttu-id="4f832-126">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4f832-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="4f832-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f832-127">OUTPUTS</span></span>

### <span data-ttu-id="4f832-128">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="4f832-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="4f832-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f832-129">NOTES</span></span>

## <span data-ttu-id="4f832-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f832-130">RELATED LINKS</span></span>
[<span data-ttu-id="4f832-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4f832-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

