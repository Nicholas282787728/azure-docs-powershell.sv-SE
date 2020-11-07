---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: cb9362a64b58770beb7d3b70f989fc740a2fc00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927661"
---
# <span data-ttu-id="17f8b-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="17f8b-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="17f8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="17f8b-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="17f8b-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="17f8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17f8b-104">SYNTAX</span></span>

### <span data-ttu-id="17f8b-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="17f8b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f8b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17f8b-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f8b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="17f8b-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f8b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17f8b-108">DESCRIPTION</span></span>
<span data-ttu-id="17f8b-109">**Sync-AzDataFactoryV2IntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="17f8b-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="17f8b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17f8b-110">EXAMPLES</span></span>

### <span data-ttu-id="17f8b-111">Exempel 1: synkronisera en referens till integration runtime</span><span class="sxs-lookup"><span data-stu-id="17f8b-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="17f8b-112">Cmdleten synkroniserar uppgifter mellan integrations körnings noder.</span><span class="sxs-lookup"><span data-stu-id="17f8b-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="17f8b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17f8b-113">PARAMETERS</span></span>

### <span data-ttu-id="17f8b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="17f8b-114">-DataFactoryName</span></span>
<span data-ttu-id="17f8b-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="17f8b-115">The data factory name.</span></span>

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

### <span data-ttu-id="17f8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f8b-116">-DefaultProfile</span></span>
<span data-ttu-id="17f8b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17f8b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f8b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="17f8b-118">-Force</span></span>
<span data-ttu-id="17f8b-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="17f8b-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17f8b-120">-InputObject</span></span>
<span data-ttu-id="17f8b-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="17f8b-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="17f8b-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="17f8b-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="17f8b-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="17f8b-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="17f8b-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="17f8b-125">The resource group name.</span></span>

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

### <span data-ttu-id="17f8b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17f8b-126">-ResourceId</span></span>
<span data-ttu-id="17f8b-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="17f8b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="17f8b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17f8b-128">-Confirm</span></span>
<span data-ttu-id="17f8b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17f8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f8b-130">-WhatIf</span></span>
<span data-ttu-id="17f8b-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17f8b-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f8b-132">CommonParameters</span></span>
<span data-ttu-id="17f8b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f8b-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f8b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f8b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17f8b-135">INPUTS</span></span>

### <span data-ttu-id="17f8b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="17f8b-136">System.String</span></span>

### <span data-ttu-id="17f8b-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="17f8b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="17f8b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17f8b-138">OUTPUTS</span></span>

### <span data-ttu-id="17f8b-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="17f8b-139">System.Void</span></span>

## <span data-ttu-id="17f8b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17f8b-140">NOTES</span></span>

## <span data-ttu-id="17f8b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17f8b-141">RELATED LINKS</span></span>
