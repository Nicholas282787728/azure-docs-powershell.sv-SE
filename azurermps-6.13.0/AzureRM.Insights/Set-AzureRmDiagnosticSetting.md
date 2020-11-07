---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: ee7d753ac81a55bf563742f87de7e195c89fb644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758188"
---
# <span data-ttu-id="77906-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="77906-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="77906-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77906-102">SYNOPSIS</span></span>
<span data-ttu-id="77906-103">Ange inställningar för loggar och mått för resursen.</span><span class="sxs-lookup"><span data-stu-id="77906-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77906-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77906-104">SYNTAX</span></span>

### <span data-ttu-id="77906-105">OldSetDiagnosticSetting (standard)</span><span class="sxs-lookup"><span data-stu-id="77906-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77906-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="77906-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77906-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77906-107">DESCRIPTION</span></span>
<span data-ttu-id="77906-108">Cmdleten **set-AzureRmDiagnosticSetting** aktiverar eller inaktiverar varje tidpunkt och log-kategori för den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="77906-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="77906-109">Loggar och mått lagras i angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="77906-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="77906-110">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="77906-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="77906-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77906-111">EXAMPLES</span></span>

### <span data-ttu-id="77906-112">Exempel 1: Aktivera alla mått och loggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="77906-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="77906-113">Det här kommandot aktiverar alla tillgängliga mått och loggar för Resource01.</span><span class="sxs-lookup"><span data-stu-id="77906-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="77906-114">Exempel 2: inaktivera alla mått och loggar</span><span class="sxs-lookup"><span data-stu-id="77906-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="77906-115">Det här kommandot inaktiverar alla tillgängliga mått och loggar för resursens Resource01.</span><span class="sxs-lookup"><span data-stu-id="77906-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="77906-116">Exempel 3: Aktivera/inaktivera flera mått kategorier</span><span class="sxs-lookup"><span data-stu-id="77906-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="77906-117">Med det här kommandot aktive ras måtten cateories Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="77906-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="77906-118">Alla andra kategorier förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="77906-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="77906-119">Exempel 4: Aktivera/inaktivera flera kategorier av typer</span><span class="sxs-lookup"><span data-stu-id="77906-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="77906-120">Det här kommandot aktiverar Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="77906-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="77906-121">Alla de andra måtten och loggarna är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="77906-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="77906-122">Exempel 4: Aktivera tids kornig het och flera kategorier</span><span class="sxs-lookup"><span data-stu-id="77906-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="77906-123">Det här kommandot aktiverar endast Category1, Category2 och Time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="77906-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="77906-124">Alla andra tidsenheter och kategorier är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="77906-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="77906-125">Exempel 5: använda pipeline</span><span class="sxs-lookup"><span data-stu-id="77906-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="77906-126">Det här kommandot använder PowerShell-pipeline för att ange (inte ändrat) en diagnostisk inställning.</span><span class="sxs-lookup"><span data-stu-id="77906-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="77906-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77906-127">PARAMETERS</span></span>

### <span data-ttu-id="77906-128">-Kategorier</span><span class="sxs-lookup"><span data-stu-id="77906-128">-Categories</span></span>
<span data-ttu-id="77906-129">Anger listan över loggnings kategorier som ska aktive ras eller inaktive ras enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="77906-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="77906-130">Om ingen kategori anges fungerar det här kommandot i alla kategorier som stöds.</span><span class="sxs-lookup"><span data-stu-id="77906-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77906-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77906-131">-DefaultProfile</span></span>
<span data-ttu-id="77906-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="77906-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77906-133">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="77906-133">-Enabled</span></span>
<span data-ttu-id="77906-134">Anger om diagnostik ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="77906-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="77906-135">Ange $True för att aktivera diagnostik eller $False för att inaktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="77906-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="77906-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="77906-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="77906-137">ID för auktoriseringsregeln för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="77906-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="77906-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="77906-138">-EventHubName</span></span>
<span data-ttu-id="77906-139">Namn på händelsehubben</span><span class="sxs-lookup"><span data-stu-id="77906-139">The event hub name</span></span>

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

### <span data-ttu-id="77906-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77906-140">-InputObject</span></span>
<span data-ttu-id="77906-141">Indatavärdet (möjligt från pipelinen.) Namnet och resourceId extraheras från det här objektet.</span><span class="sxs-lookup"><span data-stu-id="77906-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="77906-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="77906-142">-MetricCategory</span></span>
<span data-ttu-id="77906-143">Listan med mått kategorier.</span><span class="sxs-lookup"><span data-stu-id="77906-143">The list of metric categories.</span></span> <span data-ttu-id="77906-144">Om ingen kategori anges fungerar det här kommandot i alla kategorier som stöds.</span><span class="sxs-lookup"><span data-stu-id="77906-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="77906-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="77906-145">-Name</span></span>
<span data-ttu-id="77906-146">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="77906-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="77906-147">Standardvärdet är **service**.</span><span class="sxs-lookup"><span data-stu-id="77906-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="77906-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77906-148">-ResourceId</span></span>
<span data-ttu-id="77906-149">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="77906-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="77906-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="77906-150">-RetentionEnabled</span></span>
<span data-ttu-id="77906-151">Anger om att diagnostikinformation är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="77906-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="77906-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="77906-152">-RetentionInDays</span></span>
<span data-ttu-id="77906-153">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="77906-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="77906-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="77906-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="77906-155">ID för Service Bus-regel.</span><span class="sxs-lookup"><span data-stu-id="77906-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="77906-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="77906-156">-StorageAccountId</span></span>
<span data-ttu-id="77906-157">Anger ID för det lagrings konto där du vill spara data.</span><span class="sxs-lookup"><span data-stu-id="77906-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="77906-158">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="77906-158">-Timegrains</span></span>
<span data-ttu-id="77906-159">Anger hur lång tid som ska aktive ras eller inaktive ras för mått enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="77906-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="77906-160">Om du inte anger en tids kornig het kan det här kommandot användas för alla tillgängliga tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="77906-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77906-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="77906-161">-WorkspaceId</span></span>
<span data-ttu-id="77906-162">ID för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="77906-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="77906-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77906-163">-Confirm</span></span>
<span data-ttu-id="77906-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77906-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77906-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77906-165">-WhatIf</span></span>
<span data-ttu-id="77906-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77906-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77906-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77906-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77906-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77906-168">CommonParameters</span></span>
<span data-ttu-id="77906-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77906-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77906-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77906-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77906-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77906-171">INPUTS</span></span>

### <span data-ttu-id="77906-172">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="77906-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="77906-173">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77906-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="77906-174">System. String</span><span class="sxs-lookup"><span data-stu-id="77906-174">System.String</span></span>

### <span data-ttu-id="77906-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77906-175">System.Boolean</span></span>

### <span data-ttu-id="77906-176">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="77906-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="77906-177">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="77906-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="77906-178">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="77906-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="77906-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77906-179">OUTPUTS</span></span>

### <span data-ttu-id="77906-180">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="77906-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="77906-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77906-181">NOTES</span></span>

## <span data-ttu-id="77906-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77906-182">RELATED LINKS</span></span>

<span data-ttu-id="77906-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="77906-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
