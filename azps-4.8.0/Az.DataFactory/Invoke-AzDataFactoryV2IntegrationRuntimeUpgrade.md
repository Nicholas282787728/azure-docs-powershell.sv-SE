---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260058"
---
# <span data-ttu-id="9cf1b-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="9cf1b-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="9cf1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cf1b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf1b-103">Uppgraderar integrerings körning med egen värd.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="9cf1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cf1b-104">SYNTAX</span></span>

### <span data-ttu-id="9cf1b-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="9cf1b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cf1b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cf1b-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf1b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9cf1b-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf1b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cf1b-108">DESCRIPTION</span></span>
<span data-ttu-id="9cf1b-109">Cmdleten **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** uppgraderar den självvärdbaserade integrerings miljön om den nya versionen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="9cf1b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cf1b-110">EXAMPLES</span></span>

### <span data-ttu-id="9cf1b-111">Exempel 1: uppgraderar en uppgraderings körning för självvärd</span><span class="sxs-lookup"><span data-stu-id="9cf1b-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="9cf1b-112">Cmdleten uppgraderar den självvärdbaserade integrations körningen med namnet ' test-selfhost-IR ' i Data Factory ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="9cf1b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cf1b-113">PARAMETERS</span></span>

### <span data-ttu-id="9cf1b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9cf1b-114">-DataFactoryName</span></span>
<span data-ttu-id="9cf1b-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-115">The data factory name.</span></span>

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

### <span data-ttu-id="9cf1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf1b-116">-DefaultProfile</span></span>
<span data-ttu-id="9cf1b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf1b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf1b-118">-InputObject</span></span>
<span data-ttu-id="9cf1b-119">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="9cf1b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cf1b-120">-Name</span></span>
<span data-ttu-id="9cf1b-121">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="9cf1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cf1b-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-123">The resource group name.</span></span>

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

### <span data-ttu-id="9cf1b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cf1b-124">-ResourceId</span></span>
<span data-ttu-id="9cf1b-125">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9cf1b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cf1b-126">-Confirm</span></span>
<span data-ttu-id="9cf1b-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf1b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf1b-128">-WhatIf</span></span>
<span data-ttu-id="9cf1b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf1b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf1b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf1b-131">CommonParameters</span></span>
<span data-ttu-id="9cf1b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf1b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf1b-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf1b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf1b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cf1b-134">INPUTS</span></span>

### <span data-ttu-id="9cf1b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf1b-135">System.String</span></span>

### <span data-ttu-id="9cf1b-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9cf1b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9cf1b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cf1b-137">OUTPUTS</span></span>

### <span data-ttu-id="9cf1b-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="9cf1b-138">System.Void</span></span>

## <span data-ttu-id="9cf1b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cf1b-139">NOTES</span></span>
<span data-ttu-id="9cf1b-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="9cf1b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="9cf1b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cf1b-141">RELATED LINKS</span></span>

<span data-ttu-id="9cf1b-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="9cf1b-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
