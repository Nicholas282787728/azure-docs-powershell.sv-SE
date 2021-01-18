---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524063"
---
# <span data-ttu-id="4e289-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e289-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4e289-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e289-102">SYNOPSIS</span></span>
<span data-ttu-id="4e289-103">Skapar en batch-konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="4e289-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e289-104">SYNTAX</span></span>

### <span data-ttu-id="4e289-105">ByIntegrationAccountAndParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="4e289-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="4e289-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4e289-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="4e289-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4e289-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="4e289-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="4e289-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4e289-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e289-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="4e289-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e289-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e289-114">DESCRIPTION</span></span>
<span data-ttu-id="4e289-115">Cmdleten **Get-AzIntegrationAccountBatchConfiguration** skapar en ny grupp konfiguration i ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="4e289-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e289-116">EXAMPLES</span></span>

### <span data-ttu-id="4e289-117">Exempel 1: skapa ny grupp konfiguration med lokal fil</span><span class="sxs-lookup"><span data-stu-id="4e289-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4e289-118">Skapar en ny grupp konfiguration med den lokala filen som finns på fil Sök vägen i $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="4e289-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="4e289-119">Exempel 2: skapa ny kommando konfiguration med en JSON-sträng</span><span class="sxs-lookup"><span data-stu-id="4e289-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4e289-120">Skapar en ny grupp konfiguration med hjälp av en JSON-sträng i "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="4e289-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="4e289-121">Exempel 3: skapa ny kommando konfiguration med hjälp av parametrar</span><span class="sxs-lookup"><span data-stu-id="4e289-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4e289-122">Skapar en ny grupp konfiguration genom att manuellt tillhandahålla alla nödvändiga parametrar.</span><span class="sxs-lookup"><span data-stu-id="4e289-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="4e289-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e289-123">PARAMETERS</span></span>

### <span data-ttu-id="4e289-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="4e289-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="4e289-125">Kommando konfigurations definitionen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="4e289-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="4e289-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="4e289-127">Sökvägen till batch-konfigurationsfilen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="4e289-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="4e289-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="4e289-128">-BatchGroupName</span></span>
<span data-ttu-id="4e289-129">Grupp namnet för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="4e289-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="4e289-130">-BatchSize</span></span>
<span data-ttu-id="4e289-131">Batchstorleken för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="4e289-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e289-132">-DefaultProfile</span></span>
<span data-ttu-id="4e289-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e289-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e289-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="4e289-134">-MessageCount</span></span>
<span data-ttu-id="4e289-135">Antalet meddelanden i batchen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="4e289-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4e289-136">-Metadata</span></span>
<span data-ttu-id="4e289-137">Metadata för batch-konfigurationsfilen i integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="4e289-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="4e289-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e289-138">-Name</span></span>
<span data-ttu-id="4e289-139">Namnet på batch-konfigurationsfilen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e289-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4e289-140">-ParentName</span></span>
<span data-ttu-id="4e289-141">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-141">The integration account name.</span></span>

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

### <span data-ttu-id="4e289-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4e289-142">-ParentObject</span></span>
<span data-ttu-id="4e289-143">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="4e289-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e289-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e289-144">-ParentResourceId</span></span>
<span data-ttu-id="4e289-145">ID för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="4e289-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e289-146">-ResourceGroupName</span></span>
<span data-ttu-id="4e289-147">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4e289-147">The resource group name.</span></span>

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

### <span data-ttu-id="4e289-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="4e289-148">-ScheduleFrequency</span></span>
<span data-ttu-id="4e289-149">Schema frekvens för integrerings kontots batchjobb.</span><span class="sxs-lookup"><span data-stu-id="4e289-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="4e289-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="4e289-150">-ScheduleInterval</span></span>
<span data-ttu-id="4e289-151">Schema intervallet för batch-konfigurationsverktyget med integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="4e289-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="4e289-152">-ScheduleStartTime</span></span>
<span data-ttu-id="4e289-153">Start tiden för batchjobbet integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="4e289-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="4e289-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="4e289-155">Den här tids zonen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4e289-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="4e289-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e289-156">-Confirm</span></span>
<span data-ttu-id="4e289-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e289-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e289-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e289-158">-WhatIf</span></span>
<span data-ttu-id="4e289-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e289-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e289-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e289-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e289-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e289-161">CommonParameters</span></span>
<span data-ttu-id="4e289-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e289-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e289-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e289-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e289-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e289-164">INPUTS</span></span>

### <span data-ttu-id="4e289-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4e289-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4e289-166">System. String</span><span class="sxs-lookup"><span data-stu-id="4e289-166">System.String</span></span>

## <span data-ttu-id="4e289-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e289-167">OUTPUTS</span></span>

### <span data-ttu-id="4e289-168">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e289-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4e289-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e289-169">NOTES</span></span>

## <span data-ttu-id="4e289-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e289-170">RELATED LINKS</span></span>
