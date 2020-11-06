---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 07c5b03b3d5717115238e3cd66b9f80925b51537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580211"
---
# <span data-ttu-id="ac0b1-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="ac0b1-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="ac0b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0b1-103">Hämtar Metric-data för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac0b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac0b1-104">SYNTAX</span></span>

### <span data-ttu-id="ac0b1-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="ac0b1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac0b1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0b1-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac0b1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ac0b1-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac0b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac0b1-108">DESCRIPTION</span></span>
<span data-ttu-id="ac0b1-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-cmdleten får Metric-data om integrations körningen i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="ac0b1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac0b1-110">EXAMPLES</span></span>

### <span data-ttu-id="ac0b1-111">Exempel 1: skaffa statistik för kör tids mått</span><span class="sxs-lookup"><span data-stu-id="ac0b1-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="ac0b1-112">Det här kommandot visar Metric-data om integrations körningen med namnet ' test-selfhost-IR ' i prenumerationen på resurs gruppen med namnet "RG-test-dfv2" och data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="ac0b1-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ac0b1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac0b1-113">PARAMETERS</span></span>

### <span data-ttu-id="ac0b1-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac0b1-114">-DataFactoryName</span></span>
<span data-ttu-id="ac0b1-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-115">The data factory name.</span></span>

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

### <span data-ttu-id="ac0b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0b1-116">-DefaultProfile</span></span>
<span data-ttu-id="ac0b1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac0b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac0b1-118">-InputObject</span></span>
<span data-ttu-id="ac0b1-119">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="ac0b1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac0b1-120">-Name</span></span>
<span data-ttu-id="ac0b1-121">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="ac0b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac0b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ac0b1-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-123">The resource group name.</span></span>

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

### <span data-ttu-id="ac0b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0b1-124">-ResourceId</span></span>
<span data-ttu-id="ac0b1-125">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ac0b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0b1-126">CommonParameters</span></span>
<span data-ttu-id="ac0b1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac0b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0b1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac0b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0b1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac0b1-129">INPUTS</span></span>

### <span data-ttu-id="ac0b1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ac0b1-130">System.String</span></span>

### <span data-ttu-id="ac0b1-131">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac0b1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="ac0b1-132">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac0b1-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ac0b1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac0b1-133">OUTPUTS</span></span>

### <span data-ttu-id="ac0b1-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="ac0b1-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="ac0b1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac0b1-135">NOTES</span></span>

## <span data-ttu-id="ac0b1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac0b1-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac0b1-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac0b1-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

