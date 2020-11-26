---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262205"
---
# <span data-ttu-id="60283-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60283-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="60283-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60283-102">SYNOPSIS</span></span>
<span data-ttu-id="60283-103">Skapar en batch-konfiguration för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="60283-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60283-104">SYNTAX</span></span>

### <span data-ttu-id="60283-105">ByIntegrationAccountAndParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="60283-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="60283-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="60283-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="60283-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="60283-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="60283-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="60283-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="60283-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60283-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="60283-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60283-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60283-114">DESCRIPTION</span></span>
<span data-ttu-id="60283-115">Cmdleten **Get-AzIntegrationAccountBatchConfiguration** skapar en ny grupp konfiguration i ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="60283-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="60283-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60283-116">EXAMPLES</span></span>

### <span data-ttu-id="60283-117">Exempel 1: skapa ny grupp konfiguration med lokal fil</span><span class="sxs-lookup"><span data-stu-id="60283-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="60283-118">Skapar en ny grupp konfiguration med den lokala filen som finns på fil Sök vägen i $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="60283-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="60283-119">Exempel 2: skapa ny kommando konfiguration med en JSON-sträng</span><span class="sxs-lookup"><span data-stu-id="60283-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="60283-120">Skapar en ny grupp konfiguration med hjälp av en JSON-sträng i "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="60283-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="60283-121">Exempel 3: skapa ny kommando konfiguration med hjälp av parametrar</span><span class="sxs-lookup"><span data-stu-id="60283-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="60283-122">Skapar en ny grupp konfiguration genom att manuellt tillhandahålla alla nödvändiga parametrar.</span><span class="sxs-lookup"><span data-stu-id="60283-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="60283-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60283-123">PARAMETERS</span></span>

### <span data-ttu-id="60283-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="60283-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="60283-125">Kommando konfigurations definitionen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="60283-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="60283-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="60283-127">Sökvägen till batch-konfigurationsfilen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="60283-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="60283-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="60283-128">-BatchGroupName</span></span>
<span data-ttu-id="60283-129">Grupp namnet för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="60283-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="60283-130">-BatchSize</span></span>
<span data-ttu-id="60283-131">Batchstorleken för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="60283-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60283-132">-DefaultProfile</span></span>
<span data-ttu-id="60283-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60283-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60283-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="60283-134">-MessageCount</span></span>
<span data-ttu-id="60283-135">Antalet meddelanden i batchen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="60283-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="60283-136">-Metadata</span></span>
<span data-ttu-id="60283-137">Metadata för batch-konfigurationsfilen i integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="60283-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="60283-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="60283-138">-Name</span></span>
<span data-ttu-id="60283-139">Namnet på batch-konfigurationsfilen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="60283-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="60283-140">-ParentName</span></span>
<span data-ttu-id="60283-141">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="60283-141">The integration account name.</span></span>

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

### <span data-ttu-id="60283-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60283-142">-ParentObject</span></span>
<span data-ttu-id="60283-143">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="60283-143">An integration account object.</span></span>

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

### <span data-ttu-id="60283-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="60283-144">-ParentResourceId</span></span>
<span data-ttu-id="60283-145">ID för batch-sidan integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="60283-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60283-146">-ResourceGroupName</span></span>
<span data-ttu-id="60283-147">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="60283-147">The resource group name.</span></span>

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

### <span data-ttu-id="60283-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="60283-148">-ScheduleFrequency</span></span>
<span data-ttu-id="60283-149">Schema frekvens för integrerings kontots batchjobb.</span><span class="sxs-lookup"><span data-stu-id="60283-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="60283-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="60283-150">-ScheduleInterval</span></span>
<span data-ttu-id="60283-151">Schema intervallet för batch-konfigurationsverktyget med integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="60283-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="60283-152">-ScheduleStartTime</span></span>
<span data-ttu-id="60283-153">Start tiden för batchjobbet integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="60283-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="60283-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="60283-155">Den här tids zonen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="60283-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="60283-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60283-156">-Confirm</span></span>
<span data-ttu-id="60283-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60283-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60283-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60283-158">-WhatIf</span></span>
<span data-ttu-id="60283-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60283-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60283-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60283-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60283-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60283-161">CommonParameters</span></span>
<span data-ttu-id="60283-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60283-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60283-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60283-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60283-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60283-164">INPUTS</span></span>

### <span data-ttu-id="60283-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="60283-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="60283-166">System. String</span><span class="sxs-lookup"><span data-stu-id="60283-166">System.String</span></span>

## <span data-ttu-id="60283-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60283-167">OUTPUTS</span></span>

### <span data-ttu-id="60283-168">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60283-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="60283-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60283-169">NOTES</span></span>

## <span data-ttu-id="60283-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60283-170">RELATED LINKS</span></span>