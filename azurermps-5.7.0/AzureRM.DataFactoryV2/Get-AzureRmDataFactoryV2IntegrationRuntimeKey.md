---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: eb248e1059da6dcab581e4fba8b3eac7f970bb30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578204"
---
# <span data-ttu-id="faaa8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="faaa8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="faaa8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="faaa8-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="faaa8-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faaa8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faaa8-104">SYNTAX</span></span>

### <span data-ttu-id="faaa8-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="faaa8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faaa8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="faaa8-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faaa8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="faaa8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faaa8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faaa8-108">DESCRIPTION</span></span>
<span data-ttu-id="faaa8-109">Skaffa nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="faaa8-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="faaa8-110">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="faaa8-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="faaa8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faaa8-111">EXAMPLES</span></span>

### <span data-ttu-id="faaa8-112">Exempel 1: Hämta kör tids nycklar för integration</span><span class="sxs-lookup"><span data-stu-id="faaa8-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="faaa8-113">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="faaa8-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="faaa8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faaa8-114">PARAMETERS</span></span>

### <span data-ttu-id="faaa8-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="faaa8-115">-DataFactoryName</span></span>
<span data-ttu-id="faaa8-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="faaa8-116">The data factory name.</span></span>

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

### <span data-ttu-id="faaa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faaa8-117">-DefaultProfile</span></span>
<span data-ttu-id="faaa8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="faaa8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faaa8-119">-InputObject</span></span>
<span data-ttu-id="faaa8-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="faaa8-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="faaa8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="faaa8-121">-Name</span></span>
<span data-ttu-id="faaa8-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="faaa8-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="faaa8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faaa8-123">-ResourceGroupName</span></span>
<span data-ttu-id="faaa8-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="faaa8-124">The resource group name.</span></span>

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

### <span data-ttu-id="faaa8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faaa8-125">-ResourceId</span></span>
<span data-ttu-id="faaa8-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="faaa8-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="faaa8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faaa8-127">CommonParameters</span></span>
<span data-ttu-id="faaa8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faaa8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faaa8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faaa8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faaa8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faaa8-130">INPUTS</span></span>

### <span data-ttu-id="faaa8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="faaa8-131">System.String</span></span>
<span data-ttu-id="faaa8-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="faaa8-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="faaa8-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faaa8-133">OUTPUTS</span></span>

### <span data-ttu-id="faaa8-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="faaa8-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="faaa8-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faaa8-135">NOTES</span></span>

## <span data-ttu-id="faaa8-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faaa8-136">RELATED LINKS</span></span>

[<span data-ttu-id="faaa8-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="faaa8-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
