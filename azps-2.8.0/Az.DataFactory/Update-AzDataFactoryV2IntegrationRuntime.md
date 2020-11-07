---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: d2177e2ca7705f579921b9e2eb9fc64ab0e0c33a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744667"
---
# <span data-ttu-id="1dc59-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1dc59-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1dc59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dc59-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc59-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="1dc59-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="1dc59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dc59-104">SYNTAX</span></span>

### <span data-ttu-id="1dc59-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="1dc59-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc59-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc59-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc59-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1dc59-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dc59-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dc59-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc59-109">**Update-AzDataFactoryV2IntegrationRuntime** cmdlet uppdaterar egenskaperna för integrations körning.</span><span class="sxs-lookup"><span data-stu-id="1dc59-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="1dc59-110">För närvarande stöds endast cmdleten för uppdatering av "AutoUpdate" och "AutoUpdateDelayOffset" för integrations körning med egen värd.</span><span class="sxs-lookup"><span data-stu-id="1dc59-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="1dc59-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dc59-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc59-112">Exempel 1: uppdaterar en integrations körning</span><span class="sxs-lookup"><span data-stu-id="1dc59-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="1dc59-113">Cmdleten uppdaterar den självvärdbaserade integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="1dc59-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="1dc59-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dc59-114">PARAMETERS</span></span>

### <span data-ttu-id="1dc59-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="1dc59-115">-AutoUpdate</span></span>
<span data-ttu-id="1dc59-116">Aktivera eller inaktivera automatisk uppdatering för integrering med automatisk värd.</span><span class="sxs-lookup"><span data-stu-id="1dc59-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc59-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="1dc59-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="1dc59-118">Tid i timme för dagen för automatisk uppdatering av integrations körningen med självvärd.</span><span class="sxs-lookup"><span data-stu-id="1dc59-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc59-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1dc59-119">-DataFactoryName</span></span>
<span data-ttu-id="1dc59-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1dc59-120">The data factory name.</span></span>

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

### <span data-ttu-id="1dc59-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc59-121">-DefaultProfile</span></span>
<span data-ttu-id="1dc59-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc59-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc59-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc59-123">-InputObject</span></span>
<span data-ttu-id="1dc59-124">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="1dc59-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="1dc59-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dc59-125">-Name</span></span>
<span data-ttu-id="1dc59-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="1dc59-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="1dc59-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc59-127">-ResourceGroupName</span></span>
<span data-ttu-id="1dc59-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1dc59-128">The resource group name.</span></span>

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

### <span data-ttu-id="1dc59-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc59-129">-ResourceId</span></span>
<span data-ttu-id="1dc59-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="1dc59-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1dc59-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dc59-131">-Confirm</span></span>
<span data-ttu-id="1dc59-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dc59-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc59-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc59-133">-WhatIf</span></span>
<span data-ttu-id="1dc59-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dc59-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc59-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dc59-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc59-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc59-136">CommonParameters</span></span>
<span data-ttu-id="1dc59-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc59-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc59-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc59-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc59-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dc59-139">INPUTS</span></span>

### <span data-ttu-id="1dc59-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc59-140">System.String</span></span>

### <span data-ttu-id="1dc59-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1dc59-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1dc59-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dc59-142">OUTPUTS</span></span>

### <span data-ttu-id="1dc59-143">Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="1dc59-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="1dc59-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dc59-144">NOTES</span></span>
<span data-ttu-id="1dc59-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="1dc59-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1dc59-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dc59-146">RELATED LINKS</span></span>

<span data-ttu-id="1dc59-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="1dc59-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
