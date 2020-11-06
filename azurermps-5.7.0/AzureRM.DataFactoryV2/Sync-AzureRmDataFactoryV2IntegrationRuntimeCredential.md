---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 11619cf9d5699b626032f82efbc9674713076ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576567"
---
# <span data-ttu-id="5a0b9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="5a0b9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="5a0b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0b9-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a0b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a0b9-104">SYNTAX</span></span>

### <span data-ttu-id="5a0b9-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="5a0b9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0b9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a0b9-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0b9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5a0b9-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a0b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a0b9-108">DESCRIPTION</span></span>
<span data-ttu-id="5a0b9-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="5a0b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a0b9-110">EXAMPLES</span></span>

### <span data-ttu-id="5a0b9-111">Exempel 1: synkronisera en referens till integration runtime</span><span class="sxs-lookup"><span data-stu-id="5a0b9-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="5a0b9-112">Cmdleten synkroniserar uppgifter mellan integrations körnings noder.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="5a0b9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a0b9-113">PARAMETERS</span></span>

### <span data-ttu-id="5a0b9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a0b9-114">-DataFactoryName</span></span>
<span data-ttu-id="5a0b9-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-115">The data factory name.</span></span>

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

### <span data-ttu-id="5a0b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0b9-116">-DefaultProfile</span></span>
<span data-ttu-id="5a0b9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a0b9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5a0b9-118">-Force</span></span>
<span data-ttu-id="5a0b9-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5a0b9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a0b9-120">-InputObject</span></span>
<span data-ttu-id="5a0b9-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="5a0b9-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5a0b9-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5a0b9-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="5a0b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a0b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a0b9-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-125">The resource group name.</span></span>

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

### <span data-ttu-id="5a0b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a0b9-126">-ResourceId</span></span>
<span data-ttu-id="5a0b9-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5a0b9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a0b9-128">-Confirm</span></span>
<span data-ttu-id="5a0b9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a0b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0b9-130">-WhatIf</span></span>
<span data-ttu-id="5a0b9-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5a0b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0b9-132">CommonParameters</span></span>
<span data-ttu-id="5a0b9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a0b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0b9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0b9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a0b9-135">INPUTS</span></span>

### <span data-ttu-id="5a0b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5a0b9-136">System.String</span></span>
<span data-ttu-id="5a0b9-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5a0b9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5a0b9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a0b9-138">OUTPUTS</span></span>

### <span data-ttu-id="5a0b9-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="5a0b9-139">System.Object</span></span>

## <span data-ttu-id="5a0b9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a0b9-140">NOTES</span></span>

## <span data-ttu-id="5a0b9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a0b9-141">RELATED LINKS</span></span>

