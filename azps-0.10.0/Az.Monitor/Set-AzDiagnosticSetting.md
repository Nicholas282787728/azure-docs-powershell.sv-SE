---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 175d3cc49f042cb10200c43cb07bbed5d58cf9e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922481"
---
# <span data-ttu-id="66d35-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="66d35-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="66d35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66d35-102">SYNOPSIS</span></span>
<span data-ttu-id="66d35-103">Ange inställningar för loggar och mått för resursen.</span><span class="sxs-lookup"><span data-stu-id="66d35-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="66d35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66d35-104">SYNTAX</span></span>

### <span data-ttu-id="66d35-105">OldSetDiagnosticSetting (standard)</span><span class="sxs-lookup"><span data-stu-id="66d35-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66d35-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="66d35-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d35-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66d35-107">DESCRIPTION</span></span>
<span data-ttu-id="66d35-108">Cmdleten **set-AzDiagnosticSetting** aktiverar eller inaktiverar varje tidpunkt och log-kategori för den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="66d35-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="66d35-109">Loggar och mått lagras i angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="66d35-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="66d35-110">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="66d35-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="66d35-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66d35-111">EXAMPLES</span></span>

### <span data-ttu-id="66d35-112">Exempel 1: Aktivera alla mått och loggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="66d35-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="66d35-113">Det här kommandot aktiverar alla tillgängliga mått och loggar för Resource01.</span><span class="sxs-lookup"><span data-stu-id="66d35-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="66d35-114">Exempel 2: inaktivera alla mått och loggar</span><span class="sxs-lookup"><span data-stu-id="66d35-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="66d35-115">Det här kommandot inaktiverar alla tillgängliga mått och loggar för resursens Resource01.</span><span class="sxs-lookup"><span data-stu-id="66d35-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="66d35-116">Exempel 3: Aktivera/inaktivera flera mått kategorier</span><span class="sxs-lookup"><span data-stu-id="66d35-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="66d35-117">Det här kommandot inaktiverar mått kategorierna Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="66d35-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="66d35-118">Alla andra kategorier förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="66d35-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="66d35-119">Exempel 4: Aktivera/inaktivera flera kategorier av typer</span><span class="sxs-lookup"><span data-stu-id="66d35-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="66d35-120">Det här kommandot aktiverar Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="66d35-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="66d35-121">Alla de andra måtten och loggarna är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="66d35-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="66d35-122">Exempel 4: Aktivera tids kornig het och flera kategorier</span><span class="sxs-lookup"><span data-stu-id="66d35-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="66d35-123">Det här kommandot aktiverar endast Category1, Category2 och Time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="66d35-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="66d35-124">Alla andra tidsenheter och kategorier är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="66d35-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="66d35-125">Exempel 5: använda pipeline</span><span class="sxs-lookup"><span data-stu-id="66d35-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="66d35-126">Det här kommandot använder PowerShell-pipeline för att ange (ingen ändring har gjorts).</span><span class="sxs-lookup"><span data-stu-id="66d35-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="66d35-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66d35-127">PARAMETERS</span></span>

### <span data-ttu-id="66d35-128">-Kategori</span><span class="sxs-lookup"><span data-stu-id="66d35-128">-Category</span></span>
<span data-ttu-id="66d35-129">Anger listan över loggnings kategorier som ska aktive ras eller inaktive ras enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="66d35-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="66d35-130">Om ingen kategori anges fungerar det här kommandot i alla kategorier som stöds.</span><span class="sxs-lookup"><span data-stu-id="66d35-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d35-131">-DefaultProfile</span></span>
<span data-ttu-id="66d35-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66d35-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66d35-133">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="66d35-133">-Enabled</span></span>
<span data-ttu-id="66d35-134">Anger om diagnostik ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="66d35-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="66d35-135">Ange $True för att aktivera diagnostik eller $False för att inaktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="66d35-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="66d35-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="66d35-137">ID för auktoriseringsregeln för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="66d35-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="66d35-138">-EventHubName</span></span>
<span data-ttu-id="66d35-139">Namn på händelsehubben</span><span class="sxs-lookup"><span data-stu-id="66d35-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="66d35-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="66d35-141">Flagga som anger att exportera till LA måste göras till en specifik tabell, a.k.a.</span><span class="sxs-lookup"><span data-stu-id="66d35-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="66d35-142">dedikerad eller fast schema tabell, i stället för den dynamiska **standard** schema tabellen som heter **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="66d35-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="66d35-143">Det här argumentet är bara effektivt när argumentet **-workspaceId** också ges.</span><span class="sxs-lookup"><span data-stu-id="66d35-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66d35-144">-InputObject</span></span>
<span data-ttu-id="66d35-145">Indatavärdet (möjligt från pipelinen.) Namnet och resourceId extraheras från det här objektet.</span><span class="sxs-lookup"><span data-stu-id="66d35-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="66d35-146">-MetricCategory</span></span>
<span data-ttu-id="66d35-147">Listan med mått kategorier.</span><span class="sxs-lookup"><span data-stu-id="66d35-147">The list of metric categories.</span></span> <span data-ttu-id="66d35-148">Om ingen kategori anges fungerar det här kommandot i alla kategorier som stöds.</span><span class="sxs-lookup"><span data-stu-id="66d35-148">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="66d35-149">-Name</span></span>
<span data-ttu-id="66d35-150">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="66d35-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="66d35-151">Standardvärdet är **service**.</span><span class="sxs-lookup"><span data-stu-id="66d35-151">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66d35-152">-ResourceId</span></span>
<span data-ttu-id="66d35-153">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="66d35-153">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="66d35-154">-RetentionEnabled</span></span>
<span data-ttu-id="66d35-155">Anger om att diagnostikinformation är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="66d35-155">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="66d35-156">-RetentionInDays</span></span>
<span data-ttu-id="66d35-157">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="66d35-157">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-158">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="66d35-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="66d35-159">ID för Service Bus-regel.</span><span class="sxs-lookup"><span data-stu-id="66d35-159">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-160">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="66d35-160">-StorageAccountId</span></span>
<span data-ttu-id="66d35-161">Anger ID för det lagrings konto där du vill spara data.</span><span class="sxs-lookup"><span data-stu-id="66d35-161">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-162">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="66d35-162">-Timegrain</span></span>
<span data-ttu-id="66d35-163">Anger hur lång tid som ska aktive ras eller inaktive ras för mått enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="66d35-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="66d35-164">Om du inte anger en tids kornig het kan det här kommandot användas för alla tillgängliga tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="66d35-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-165">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="66d35-165">-WorkspaceId</span></span>
<span data-ttu-id="66d35-166">ID för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="66d35-166">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66d35-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66d35-167">-Confirm</span></span>
<span data-ttu-id="66d35-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66d35-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d35-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d35-169">-WhatIf</span></span>
<span data-ttu-id="66d35-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66d35-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66d35-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66d35-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d35-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d35-172">CommonParameters</span></span>
<span data-ttu-id="66d35-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d35-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d35-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66d35-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d35-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66d35-175">INPUTS</span></span>

### <span data-ttu-id="66d35-176">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="66d35-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="66d35-177">System. String</span><span class="sxs-lookup"><span data-stu-id="66d35-177">System.String</span></span>

### <span data-ttu-id="66d35-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66d35-178">System.Boolean</span></span>

### <span data-ttu-id="66d35-179">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66d35-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="66d35-180">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66d35-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="66d35-181">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66d35-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66d35-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66d35-182">OUTPUTS</span></span>

### <span data-ttu-id="66d35-183">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="66d35-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="66d35-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66d35-184">NOTES</span></span>

## <span data-ttu-id="66d35-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66d35-185">RELATED LINKS</span></span>

<span data-ttu-id="66d35-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="66d35-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
