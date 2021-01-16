---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523494"
---
# <span data-ttu-id="13b6f-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b6f-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="13b6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="13b6f-103">Tar bort en batch-konfiguration för integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="13b6f-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="13b6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13b6f-104">SYNTAX</span></span>

### <span data-ttu-id="13b6f-105">ByIntegrationAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="13b6f-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b6f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13b6f-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b6f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13b6f-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13b6f-108">DESCRIPTION</span></span>
<span data-ttu-id="13b6f-109">Cmdleten **Remove-AzIntegrationAccountBatchConfiguration** tar bort en grupp konfiguration från ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="13b6f-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="13b6f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13b6f-110">EXAMPLES</span></span>

### <span data-ttu-id="13b6f-111">Exempel 1: ta bort en kommando konfiguration efter parametrar</span><span class="sxs-lookup"><span data-stu-id="13b6f-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="13b6f-112">Tar bort gruppkonfigurationen med namnet "sampleBatchConfig" som finns i integrations kontot "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="13b6f-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="13b6f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13b6f-113">PARAMETERS</span></span>

### <span data-ttu-id="13b6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b6f-114">-DefaultProfile</span></span>
<span data-ttu-id="13b6f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13b6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b6f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13b6f-116">-InputObject</span></span>
<span data-ttu-id="13b6f-117">En batch-konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="13b6f-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b6f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="13b6f-118">-Name</span></span>
<span data-ttu-id="13b6f-119">Namnet på batch-konfigurationsfilen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="13b6f-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b6f-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="13b6f-120">-ParentName</span></span>
<span data-ttu-id="13b6f-121">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="13b6f-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b6f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13b6f-122">-PassThru</span></span>
<span data-ttu-id="13b6f-123">Returnera om kommandot lyckades eller inte.</span><span class="sxs-lookup"><span data-stu-id="13b6f-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="13b6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="13b6f-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="13b6f-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b6f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13b6f-126">-ResourceId</span></span>
<span data-ttu-id="13b6f-127">ID för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="13b6f-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b6f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13b6f-128">-Confirm</span></span>
<span data-ttu-id="13b6f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13b6f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b6f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b6f-130">-WhatIf</span></span>
<span data-ttu-id="13b6f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13b6f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13b6f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13b6f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b6f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b6f-133">CommonParameters</span></span>
<span data-ttu-id="13b6f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b6f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b6f-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b6f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b6f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13b6f-136">INPUTS</span></span>

### <span data-ttu-id="13b6f-137">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="13b6f-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="13b6f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="13b6f-138">System.String</span></span>

## <span data-ttu-id="13b6f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13b6f-139">OUTPUTS</span></span>

### <span data-ttu-id="13b6f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13b6f-140">System.Boolean</span></span>

## <span data-ttu-id="13b6f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13b6f-141">NOTES</span></span>

## <span data-ttu-id="13b6f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13b6f-142">RELATED LINKS</span></span>
