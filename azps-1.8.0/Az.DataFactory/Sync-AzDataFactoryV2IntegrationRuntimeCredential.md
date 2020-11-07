---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917006"
---
# <span data-ttu-id="02874-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="02874-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="02874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02874-102">SYNOPSIS</span></span>
<span data-ttu-id="02874-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="02874-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="02874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02874-104">SYNTAX</span></span>

### <span data-ttu-id="02874-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="02874-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02874-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02874-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02874-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="02874-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02874-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02874-108">DESCRIPTION</span></span>
<span data-ttu-id="02874-109">**Sync-AzDataFactoryV2IntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="02874-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="02874-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02874-110">EXAMPLES</span></span>

### <span data-ttu-id="02874-111">Exempel 1: synkronisera en referens till integration runtime</span><span class="sxs-lookup"><span data-stu-id="02874-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="02874-112">Cmdleten synkroniserar uppgifter mellan integrations körnings noder.</span><span class="sxs-lookup"><span data-stu-id="02874-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="02874-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02874-113">PARAMETERS</span></span>

### <span data-ttu-id="02874-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="02874-114">-DataFactoryName</span></span>
<span data-ttu-id="02874-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="02874-115">The data factory name.</span></span>

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

### <span data-ttu-id="02874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02874-116">-DefaultProfile</span></span>
<span data-ttu-id="02874-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02874-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02874-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02874-118">-Force</span></span>
<span data-ttu-id="02874-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="02874-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="02874-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02874-120">-InputObject</span></span>
<span data-ttu-id="02874-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="02874-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="02874-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="02874-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="02874-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="02874-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="02874-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02874-124">-ResourceGroupName</span></span>
<span data-ttu-id="02874-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="02874-125">The resource group name.</span></span>

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

### <span data-ttu-id="02874-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02874-126">-ResourceId</span></span>
<span data-ttu-id="02874-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="02874-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="02874-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02874-128">-Confirm</span></span>
<span data-ttu-id="02874-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02874-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02874-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02874-130">-WhatIf</span></span>
<span data-ttu-id="02874-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02874-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="02874-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02874-132">CommonParameters</span></span>
<span data-ttu-id="02874-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02874-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02874-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02874-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02874-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02874-135">INPUTS</span></span>

### <span data-ttu-id="02874-136">System. String</span><span class="sxs-lookup"><span data-stu-id="02874-136">System.String</span></span>

### <span data-ttu-id="02874-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="02874-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="02874-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02874-138">OUTPUTS</span></span>

### <span data-ttu-id="02874-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="02874-139">System.Void</span></span>

## <span data-ttu-id="02874-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02874-140">NOTES</span></span>

## <span data-ttu-id="02874-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02874-141">RELATED LINKS</span></span>
