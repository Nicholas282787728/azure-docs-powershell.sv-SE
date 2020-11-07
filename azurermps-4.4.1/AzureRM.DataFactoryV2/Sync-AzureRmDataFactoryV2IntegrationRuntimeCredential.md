---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755455"
---
# <span data-ttu-id="4fabf-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="4fabf-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="4fabf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fabf-102">SYNOPSIS</span></span>
<span data-ttu-id="4fabf-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="4fabf-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fabf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fabf-104">SYNTAX</span></span>

### <span data-ttu-id="4fabf-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="4fabf-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4fabf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fabf-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4fabf-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4fabf-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4fabf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fabf-108">DESCRIPTION</span></span>
<span data-ttu-id="4fabf-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="4fabf-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="4fabf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fabf-110">EXAMPLES</span></span>

### <span data-ttu-id="4fabf-111">Exempel 1: synkronisera en referens till integration runtime</span><span class="sxs-lookup"><span data-stu-id="4fabf-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="4fabf-112">Cmdleten synkroniserar uppgifter mellan integrations körnings noder.</span><span class="sxs-lookup"><span data-stu-id="4fabf-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="4fabf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fabf-113">PARAMETERS</span></span>

### <span data-ttu-id="4fabf-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fabf-114">-Confirm</span></span>
<span data-ttu-id="4fabf-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fabf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fabf-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4fabf-116">-DataFactoryName</span></span>
<span data-ttu-id="4fabf-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="4fabf-117">The data factory name.</span></span>

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

### <span data-ttu-id="4fabf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4fabf-118">-Force</span></span>
<span data-ttu-id="4fabf-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4fabf-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4fabf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fabf-120">-InputObject</span></span>
<span data-ttu-id="4fabf-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="4fabf-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="4fabf-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4fabf-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4fabf-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="4fabf-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fabf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fabf-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fabf-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4fabf-125">The resource group name.</span></span>

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

### <span data-ttu-id="4fabf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fabf-126">-ResourceId</span></span>
<span data-ttu-id="4fabf-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="4fabf-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4fabf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fabf-128">-WhatIf</span></span>
<span data-ttu-id="4fabf-129">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fabf-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="4fabf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fabf-130">INPUTS</span></span>

### <span data-ttu-id="4fabf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4fabf-131">System.String</span></span>
<span data-ttu-id="4fabf-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4fabf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="4fabf-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fabf-133">OUTPUTS</span></span>

### <span data-ttu-id="4fabf-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="4fabf-134">System.Object</span></span>

## <span data-ttu-id="4fabf-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fabf-135">NOTES</span></span>

## <span data-ttu-id="4fabf-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fabf-136">RELATED LINKS</span></span>
