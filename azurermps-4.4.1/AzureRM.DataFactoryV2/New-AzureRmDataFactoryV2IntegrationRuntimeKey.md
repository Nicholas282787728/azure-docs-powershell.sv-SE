---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755456"
---
# <span data-ttu-id="2838e-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2838e-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="2838e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2838e-102">SYNOPSIS</span></span>
<span data-ttu-id="2838e-103">Återskapa den självvärdbaserade integrerings kör nyckeln.</span><span class="sxs-lookup"><span data-stu-id="2838e-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2838e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2838e-104">SYNTAX</span></span>

### <span data-ttu-id="2838e-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="2838e-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2838e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2838e-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="2838e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2838e-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2838e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2838e-108">DESCRIPTION</span></span>
<span data-ttu-id="2838e-109">Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** återskapar integrerings körnings nyckeln med det nycklar som anges med parametern "värde namn".</span><span class="sxs-lookup"><span data-stu-id="2838e-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="2838e-110">Den föregående knappen är ogiltig.</span><span class="sxs-lookup"><span data-stu-id="2838e-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="2838e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2838e-111">EXAMPLES</span></span>

### <span data-ttu-id="2838e-112">Exempel 1: skapa en ny-nyckeln för en integrations körning</span><span class="sxs-lookup"><span data-stu-id="2838e-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="2838e-113">Cmdleten återskapar nyckeln ' authKey2 ' för integration runtime "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="2838e-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2838e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2838e-114">PARAMETERS</span></span>

### <span data-ttu-id="2838e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2838e-115">-Confirm</span></span>
<span data-ttu-id="2838e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2838e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2838e-117">-DataFactoryName</span></span>
<span data-ttu-id="2838e-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2838e-118">The data factory name.</span></span>

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

### <span data-ttu-id="2838e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2838e-119">-Force</span></span>
<span data-ttu-id="2838e-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2838e-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2838e-121">-InputObject</span></span>
<span data-ttu-id="2838e-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="2838e-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="2838e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2838e-123">-KeyName</span></span>
<span data-ttu-id="2838e-124">Namn på en autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="2838e-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="2838e-125">-Name</span></span>
<span data-ttu-id="2838e-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="2838e-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="2838e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2838e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2838e-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2838e-128">The resource group name.</span></span>

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

### <span data-ttu-id="2838e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2838e-129">-ResourceId</span></span>
<span data-ttu-id="2838e-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="2838e-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2838e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2838e-131">-WhatIf</span></span>
<span data-ttu-id="2838e-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2838e-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2838e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2838e-133">INPUTS</span></span>

### <span data-ttu-id="2838e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2838e-134">System.String</span></span>
<span data-ttu-id="2838e-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2838e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="2838e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2838e-136">OUTPUTS</span></span>

### <span data-ttu-id="2838e-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="2838e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="2838e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2838e-138">NOTES</span></span>

## <span data-ttu-id="2838e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2838e-139">RELATED LINKS</span></span>
[<span data-ttu-id="2838e-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2838e-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
