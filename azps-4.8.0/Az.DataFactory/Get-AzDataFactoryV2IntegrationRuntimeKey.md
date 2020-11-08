---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262776"
---
# <span data-ttu-id="13af2-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="13af2-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="13af2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13af2-102">SYNOPSIS</span></span>
<span data-ttu-id="13af2-103">Hämtar nycklar för en självvärds integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="13af2-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="13af2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13af2-104">SYNTAX</span></span>

### <span data-ttu-id="13af2-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="13af2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13af2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13af2-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13af2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="13af2-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13af2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13af2-108">DESCRIPTION</span></span>
<span data-ttu-id="13af2-109">Skaffa nycklar för en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="13af2-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="13af2-110">Nycklarna används för att registrera en nod för integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="13af2-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="13af2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13af2-111">EXAMPLES</span></span>

### <span data-ttu-id="13af2-112">Exempel 1: Hämta kör tids nycklar för integration</span><span class="sxs-lookup"><span data-stu-id="13af2-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="13af2-113">Cmdleten hämtar nycklar för en integrations körning med namnet ' test-selfhost-IR '.</span><span class="sxs-lookup"><span data-stu-id="13af2-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="13af2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13af2-114">PARAMETERS</span></span>

### <span data-ttu-id="13af2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13af2-115">-DataFactoryName</span></span>
<span data-ttu-id="13af2-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="13af2-116">The data factory name.</span></span>

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

### <span data-ttu-id="13af2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13af2-117">-DefaultProfile</span></span>
<span data-ttu-id="13af2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13af2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13af2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13af2-119">-InputObject</span></span>
<span data-ttu-id="13af2-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="13af2-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="13af2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="13af2-121">-Name</span></span>
<span data-ttu-id="13af2-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="13af2-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="13af2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13af2-123">-ResourceGroupName</span></span>
<span data-ttu-id="13af2-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="13af2-124">The resource group name.</span></span>

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

### <span data-ttu-id="13af2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13af2-125">-ResourceId</span></span>
<span data-ttu-id="13af2-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="13af2-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="13af2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13af2-127">CommonParameters</span></span>
<span data-ttu-id="13af2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13af2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13af2-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13af2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13af2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13af2-130">INPUTS</span></span>

### <span data-ttu-id="13af2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="13af2-131">System.String</span></span>

### <span data-ttu-id="13af2-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="13af2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="13af2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13af2-133">OUTPUTS</span></span>

### <span data-ttu-id="13af2-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="13af2-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="13af2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13af2-135">NOTES</span></span>

## <span data-ttu-id="13af2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13af2-136">RELATED LINKS</span></span>

[<span data-ttu-id="13af2-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="13af2-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
