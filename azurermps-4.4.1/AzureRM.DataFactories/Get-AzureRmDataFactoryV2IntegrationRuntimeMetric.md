---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574718"
---
# <span data-ttu-id="8cea7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="8cea7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="8cea7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cea7-102">SYNOPSIS</span></span>
<span data-ttu-id="8cea7-103">Hämtar Metric-data för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="8cea7-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cea7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cea7-104">SYNTAX</span></span>

### <span data-ttu-id="8cea7-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="8cea7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cea7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cea7-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cea7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8cea7-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cea7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cea7-108">DESCRIPTION</span></span>
<span data-ttu-id="8cea7-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric-cmdleten får Metric-data om integrations körningen i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8cea7-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="8cea7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cea7-110">EXAMPLES</span></span>

### <span data-ttu-id="8cea7-111">Exempel 1: skaffa statistik för kör tids mått</span><span class="sxs-lookup"><span data-stu-id="8cea7-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="8cea7-112">Det här kommandot visar Metric-data om integrations körningen med namnet ' test-selfhost-IR ' i prenumerationen på resurs gruppen med namnet "RG-test-dfv2" och data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8cea7-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="8cea7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cea7-113">PARAMETERS</span></span>

### <span data-ttu-id="8cea7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8cea7-114">-DataFactoryName</span></span>
<span data-ttu-id="8cea7-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8cea7-115">The data factory name.</span></span>

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

### <span data-ttu-id="8cea7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cea7-116">-InputObject</span></span>
<span data-ttu-id="8cea7-117">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea7-117">The integration runtime object.</span></span>

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

### <span data-ttu-id="8cea7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cea7-118">-Name</span></span>
<span data-ttu-id="8cea7-119">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="8cea7-119">The integration runtime name.</span></span>

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

### <span data-ttu-id="8cea7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cea7-120">-ResourceGroupName</span></span>
<span data-ttu-id="8cea7-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8cea7-121">The resource group name.</span></span>

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

### <span data-ttu-id="8cea7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cea7-122">-ResourceId</span></span>
<span data-ttu-id="8cea7-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="8cea7-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8cea7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cea7-124">-DefaultProfile</span></span>
<span data-ttu-id="8cea7-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cea7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cea7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cea7-126">CommonParameters</span></span>
<span data-ttu-id="8cea7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cea7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cea7-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cea7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cea7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cea7-129">INPUTS</span></span>

### <span data-ttu-id="8cea7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8cea7-130">System.String</span></span>
<span data-ttu-id="8cea7-131">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8cea7-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8cea7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cea7-132">OUTPUTS</span></span>

### <span data-ttu-id="8cea7-133">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="8cea7-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="8cea7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cea7-134">NOTES</span></span>

## <span data-ttu-id="8cea7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cea7-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cea7-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8cea7-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

