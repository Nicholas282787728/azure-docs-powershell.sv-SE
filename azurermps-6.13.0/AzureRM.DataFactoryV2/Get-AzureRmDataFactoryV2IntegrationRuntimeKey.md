---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 0f57e0ac27e47272c2b6e72a3c847d9f06a568a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580208"
---
# <span data-ttu-id="cf235-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf235-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cf235-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf235-102">SYNOPSIS</span></span>
<span data-ttu-id="cf235-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="cf235-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf235-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf235-104">SYNTAX</span></span>

### <span data-ttu-id="cf235-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="cf235-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf235-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf235-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf235-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf235-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf235-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf235-108">DESCRIPTION</span></span>
<span data-ttu-id="cf235-109">Skaffa nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="cf235-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="cf235-110">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cf235-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="cf235-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf235-111">EXAMPLES</span></span>

### <span data-ttu-id="cf235-112">Exempel 1: Hämta kör tids nycklar för integration</span><span class="sxs-lookup"><span data-stu-id="cf235-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="cf235-113">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="cf235-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cf235-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf235-114">PARAMETERS</span></span>

### <span data-ttu-id="cf235-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf235-115">-DataFactoryName</span></span>
<span data-ttu-id="cf235-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="cf235-116">The data factory name.</span></span>

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

### <span data-ttu-id="cf235-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf235-117">-DefaultProfile</span></span>
<span data-ttu-id="cf235-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf235-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf235-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf235-119">-InputObject</span></span>
<span data-ttu-id="cf235-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="cf235-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="cf235-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf235-121">-Name</span></span>
<span data-ttu-id="cf235-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="cf235-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="cf235-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf235-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf235-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cf235-124">The resource group name.</span></span>

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

### <span data-ttu-id="cf235-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf235-125">-ResourceId</span></span>
<span data-ttu-id="cf235-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="cf235-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf235-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf235-127">CommonParameters</span></span>
<span data-ttu-id="cf235-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf235-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf235-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf235-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf235-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf235-130">INPUTS</span></span>

### <span data-ttu-id="cf235-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cf235-131">System.String</span></span>

### <span data-ttu-id="cf235-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf235-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="cf235-133">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf235-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cf235-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf235-134">OUTPUTS</span></span>

### <span data-ttu-id="cf235-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="cf235-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="cf235-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf235-136">NOTES</span></span>

## <span data-ttu-id="cf235-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf235-137">RELATED LINKS</span></span>

[<span data-ttu-id="cf235-138">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf235-138">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
