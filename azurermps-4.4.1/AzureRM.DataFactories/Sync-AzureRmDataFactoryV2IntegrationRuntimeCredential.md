---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: e89f4c69996f5527c49db72f3185e5a126b348c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574978"
---
# <span data-ttu-id="2c3a9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="2c3a9-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="2c3a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3a9-103">Synkroniserar uppgifter med kör tids noder för integration.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c3a9-104">SYNTAX</span></span>

### <span data-ttu-id="2c3a9-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="2c3a9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3a9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c3a9-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3a9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2c3a9-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3a9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c3a9-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3a9-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** -cmdleten synkroniserar lokala autentiseringsuppgifter bland integrations körnings noder, vilket innebär att autentiseringsuppgifterna är identiska på alla noder.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="2c3a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c3a9-110">EXAMPLES</span></span>

### <span data-ttu-id="2c3a9-111">Exempel 1: synkronisera en referens till integration runtime</span><span class="sxs-lookup"><span data-stu-id="2c3a9-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="2c3a9-112">Cmdleten synkroniserar uppgifter mellan integrations körnings noder.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="2c3a9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c3a9-113">PARAMETERS</span></span>

### <span data-ttu-id="2c3a9-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c3a9-114">-Confirm</span></span>
<span data-ttu-id="2c3a9-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3a9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c3a9-116">-DataFactoryName</span></span>
<span data-ttu-id="2c3a9-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-117">The data factory name.</span></span>

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

### <span data-ttu-id="2c3a9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2c3a9-118">-Force</span></span>
<span data-ttu-id="2c3a9-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2c3a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c3a9-120">-InputObject</span></span>
<span data-ttu-id="2c3a9-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c3a9-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2c3a9-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2c3a9-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c3a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c3a9-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-125">The resource group name.</span></span>

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

### <span data-ttu-id="2c3a9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c3a9-126">-ResourceId</span></span>
<span data-ttu-id="2c3a9-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2c3a9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3a9-128">-WhatIf</span></span>
<span data-ttu-id="2c3a9-129">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2c3a9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3a9-130">-DefaultProfile</span></span>
<span data-ttu-id="2c3a9-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3a9-132">CommonParameters</span></span>
<span data-ttu-id="2c3a9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3a9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3a9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c3a9-135">INPUTS</span></span>

### <span data-ttu-id="2c3a9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2c3a9-136">System.String</span></span>
<span data-ttu-id="2c3a9-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c3a9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2c3a9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c3a9-138">OUTPUTS</span></span>

### <span data-ttu-id="2c3a9-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="2c3a9-139">System.Object</span></span>

## <span data-ttu-id="2c3a9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c3a9-140">NOTES</span></span>

## <span data-ttu-id="2c3a9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c3a9-141">RELATED LINKS</span></span>

