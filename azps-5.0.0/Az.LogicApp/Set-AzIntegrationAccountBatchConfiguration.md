---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273358"
---
# <span data-ttu-id="efc50-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc50-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="efc50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efc50-102">SYNOPSIS</span></span>
<span data-ttu-id="efc50-103">Ändrar kommando konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="efc50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efc50-104">SYNTAX</span></span>

### <span data-ttu-id="efc50-105">ByIntegrationAccountAndParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="efc50-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="efc50-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="efc50-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="efc50-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="efc50-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="efc50-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="efc50-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="efc50-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc50-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="efc50-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc50-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efc50-114">DESCRIPTION</span></span>
<span data-ttu-id="efc50-115">Cmdleten **set-AzIntegrationAccountBatchConfiguration** ändrar en batch-konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="efc50-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efc50-116">EXAMPLES</span></span>

### <span data-ttu-id="efc50-117">Exempel 1: ändra en kommando konfiguration med lokal fil</span><span class="sxs-lookup"><span data-stu-id="efc50-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="efc50-118">Ändra en kommando konfiguration med namnet "sampleBatchConfig" med den lokala filen som finns på fil Sök vägen i $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="efc50-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="efc50-119">Exempel 2: ändra en kommando konfiguration med hjälp av en JSON-sträng</span><span class="sxs-lookup"><span data-stu-id="efc50-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="efc50-120">Ändra en kommando konfiguration med namnet "sampleBatchConfig" med hjälp av en JSON-sträng i "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="efc50-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="efc50-121">Exempel 3: ändra en kommando konfiguration med hjälp av parametrar</span><span class="sxs-lookup"><span data-stu-id="efc50-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="efc50-122">Ändra en kommando konfiguration med namnet "sampleBatchConfig" genom att manuellt tillhandahålla alla nödvändiga parametrar.</span><span class="sxs-lookup"><span data-stu-id="efc50-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="efc50-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efc50-123">PARAMETERS</span></span>

### <span data-ttu-id="efc50-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="efc50-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="efc50-125">Kommando konfigurations definitionen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="efc50-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="efc50-127">Sökvägen till batch-konfigurationsfilen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="efc50-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="efc50-128">-BatchGroupName</span></span>
<span data-ttu-id="efc50-129">Grupp namnet för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="efc50-130">-BatchSize</span></span>
<span data-ttu-id="efc50-131">Batchstorleken för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc50-132">-DefaultProfile</span></span>
<span data-ttu-id="efc50-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efc50-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc50-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc50-134">-InputObject</span></span>
<span data-ttu-id="efc50-135">En batch-konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="efc50-136">-MessageCount</span></span>
<span data-ttu-id="efc50-137">Antalet meddelanden i batchen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="efc50-138">-Metadata</span></span>
<span data-ttu-id="efc50-139">Metadata för batch-konfigurationsfilen i integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="efc50-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="efc50-140">-Name</span></span>
<span data-ttu-id="efc50-141">Namnet på batch-konfigurationsfilen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="efc50-142">-ParentName</span></span>
<span data-ttu-id="efc50-143">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc50-144">-ResourceGroupName</span></span>
<span data-ttu-id="efc50-145">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="efc50-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc50-146">-ResourceId</span></span>
<span data-ttu-id="efc50-147">ID för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="efc50-148">-ScheduleFrequency</span></span>
<span data-ttu-id="efc50-149">Schema frekvens för integrerings kontots batchjobb.</span><span class="sxs-lookup"><span data-stu-id="efc50-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="efc50-150">-ScheduleInterval</span></span>
<span data-ttu-id="efc50-151">Schema intervallet för batch-konfigurationsverktyget med integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="efc50-152">-ScheduleStartTime</span></span>
<span data-ttu-id="efc50-153">Start tiden för batchjobbet integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="efc50-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="efc50-155">Den här tids zonen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="efc50-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc50-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="efc50-156">-Confirm</span></span>
<span data-ttu-id="efc50-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="efc50-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc50-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc50-158">-WhatIf</span></span>
<span data-ttu-id="efc50-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efc50-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc50-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="efc50-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc50-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc50-161">CommonParameters</span></span>
<span data-ttu-id="efc50-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc50-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc50-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc50-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc50-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efc50-164">INPUTS</span></span>

### <span data-ttu-id="efc50-165">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc50-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="efc50-166">System. String</span><span class="sxs-lookup"><span data-stu-id="efc50-166">System.String</span></span>

## <span data-ttu-id="efc50-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efc50-167">OUTPUTS</span></span>

### <span data-ttu-id="efc50-168">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc50-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="efc50-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efc50-169">NOTES</span></span>

## <span data-ttu-id="efc50-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efc50-170">RELATED LINKS</span></span>
