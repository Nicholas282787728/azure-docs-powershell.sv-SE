---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583823"
---
# <span data-ttu-id="0c5c2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0c5c2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0c5c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5c2-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c5c2-104">SYNTAX</span></span>

### <span data-ttu-id="0c5c2-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="0c5c2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c5c2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c5c2-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c5c2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0c5c2-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5c2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c5c2-108">DESCRIPTION</span></span>
<span data-ttu-id="0c5c2-109">Skaffa nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="0c5c2-110">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="0c5c2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c5c2-111">EXAMPLES</span></span>

### <span data-ttu-id="0c5c2-112">Exempel 1: Hämta kör tids nycklar för integration</span><span class="sxs-lookup"><span data-stu-id="0c5c2-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="0c5c2-113">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0c5c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c5c2-114">PARAMETERS</span></span>

### <span data-ttu-id="0c5c2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0c5c2-115">-DataFactoryName</span></span>
<span data-ttu-id="0c5c2-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-116">The data factory name.</span></span>

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

### <span data-ttu-id="0c5c2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c5c2-117">-InputObject</span></span>
<span data-ttu-id="0c5c2-118">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="0c5c2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c5c2-119">-Name</span></span>
<span data-ttu-id="0c5c2-120">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="0c5c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c5c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c5c2-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-122">The resource group name.</span></span>

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

### <span data-ttu-id="0c5c2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c5c2-123">-ResourceId</span></span>
<span data-ttu-id="0c5c2-124">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0c5c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5c2-125">-DefaultProfile</span></span>
<span data-ttu-id="0c5c2-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5c2-127">CommonParameters</span></span>
<span data-ttu-id="0c5c2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5c2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5c2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c5c2-130">INPUTS</span></span>

### <span data-ttu-id="0c5c2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0c5c2-131">System.String</span></span>
<span data-ttu-id="0c5c2-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0c5c2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="0c5c2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c5c2-133">OUTPUTS</span></span>

### <span data-ttu-id="0c5c2-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0c5c2-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0c5c2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c5c2-135">NOTES</span></span>

## <span data-ttu-id="0c5c2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c5c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c5c2-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0c5c2-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
