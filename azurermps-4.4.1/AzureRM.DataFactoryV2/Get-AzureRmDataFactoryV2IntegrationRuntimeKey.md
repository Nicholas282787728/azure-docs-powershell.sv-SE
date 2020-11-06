---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585679"
---
# <span data-ttu-id="58eab-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="58eab-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="58eab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58eab-102">SYNOPSIS</span></span>
<span data-ttu-id="58eab-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="58eab-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58eab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58eab-104">SYNTAX</span></span>

### <span data-ttu-id="58eab-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="58eab-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="58eab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58eab-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="58eab-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="58eab-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="58eab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58eab-108">DESCRIPTION</span></span>
<span data-ttu-id="58eab-109">Skaffa nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="58eab-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="58eab-110">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="58eab-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="58eab-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58eab-111">EXAMPLES</span></span>

### <span data-ttu-id="58eab-112">Exempel 1: Hämta kör tids nycklar för integration</span><span class="sxs-lookup"><span data-stu-id="58eab-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="58eab-113">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="58eab-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="58eab-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58eab-114">PARAMETERS</span></span>

### <span data-ttu-id="58eab-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58eab-115">-DataFactoryName</span></span>
<span data-ttu-id="58eab-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="58eab-116">The data factory name.</span></span>

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

### <span data-ttu-id="58eab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58eab-117">-InputObject</span></span>
<span data-ttu-id="58eab-118">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="58eab-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="58eab-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="58eab-119">-Name</span></span>
<span data-ttu-id="58eab-120">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="58eab-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="58eab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58eab-121">-ResourceGroupName</span></span>
<span data-ttu-id="58eab-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="58eab-122">The resource group name.</span></span>

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

### <span data-ttu-id="58eab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58eab-123">-ResourceId</span></span>
<span data-ttu-id="58eab-124">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="58eab-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="58eab-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58eab-125">INPUTS</span></span>

### <span data-ttu-id="58eab-126">System. String</span><span class="sxs-lookup"><span data-stu-id="58eab-126">System.String</span></span>
<span data-ttu-id="58eab-127">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58eab-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="58eab-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58eab-128">OUTPUTS</span></span>

### <span data-ttu-id="58eab-129">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="58eab-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="58eab-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58eab-130">NOTES</span></span>

## <span data-ttu-id="58eab-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58eab-131">RELATED LINKS</span></span>
[<span data-ttu-id="58eab-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="58eab-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
