---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574289"
---
# <span data-ttu-id="8a453-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8a453-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="8a453-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a453-102">SYNOPSIS</span></span>
<span data-ttu-id="8a453-103">Ange inställningar för loggar och mått för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a453-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a453-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a453-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a453-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a453-105">DESCRIPTION</span></span>
<span data-ttu-id="8a453-106">Cmdleten **set-AzureRmDiagnosticSetting** aktiverar eller inaktiverar varje tidpunkt och log-kategori för den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="8a453-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="8a453-107">Loggar och mått lagras i angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8a453-107">The logs and metrics are stored in the specified storage account.</span></span>

<span data-ttu-id="8a453-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="8a453-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8a453-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a453-109">EXAMPLES</span></span>

### <span data-ttu-id="8a453-110">Exempel 1: Aktivera alla mått och loggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="8a453-110">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="8a453-111">Det här kommandot aktiverar alla tillgängliga mått och loggar för Resource01.</span><span class="sxs-lookup"><span data-stu-id="8a453-111">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="8a453-112">Exempel 2: inaktivera alla mått och loggar</span><span class="sxs-lookup"><span data-stu-id="8a453-112">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="8a453-113">Det här kommandot inaktiverar alla tillgängliga mått och loggar för resursens Resource01.</span><span class="sxs-lookup"><span data-stu-id="8a453-113">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="8a453-114">Exempel 3: aktivera flera kategorier</span><span class="sxs-lookup"><span data-stu-id="8a453-114">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="8a453-115">Det här kommandot aktiverar Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="8a453-115">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="8a453-116">Alla timegrains och andra kategorier förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="8a453-116">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="8a453-117">Exempel 4: Aktivera tids kornig het och flera kategorier</span><span class="sxs-lookup"><span data-stu-id="8a453-117">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="8a453-118">Det här kommandot aktiverar endast Category1, Category2 och Time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="8a453-118">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="8a453-119">Alla andra tidsenheter och kategorier är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="8a453-119">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="8a453-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a453-120">PARAMETERS</span></span>

### <span data-ttu-id="8a453-121">-Kategorier</span><span class="sxs-lookup"><span data-stu-id="8a453-121">-Categories</span></span>
<span data-ttu-id="8a453-122">Anger listan över loggnings kategorier som ska aktive ras eller inaktive ras enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="8a453-122">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8a453-123">Om du inte anger en kategori används det här kommandot i alla kategorier.</span><span class="sxs-lookup"><span data-stu-id="8a453-123">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a453-124">-DefaultProfile</span></span>
<span data-ttu-id="8a453-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a453-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-126">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="8a453-126">-Enabled</span></span>
<span data-ttu-id="8a453-127">Anger om diagnostik ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="8a453-127">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="8a453-128">Ange $True för att aktivera diagnostik eller $False för att inaktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="8a453-128">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-129">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="8a453-129">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="8a453-130">Regel för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="8a453-130">The event hub rule i</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a453-131">-ResourceId</span></span>
<span data-ttu-id="8a453-132">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a453-132">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-133">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="8a453-133">-RetentionEnabled</span></span>
<span data-ttu-id="8a453-134">Anger om att diagnostikinformation är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="8a453-134">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8a453-135">-RetentionInDays</span></span>
<span data-ttu-id="8a453-136">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="8a453-136">Specifies the retention policy, in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-137">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="8a453-137">-ServiceBusRuleId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8a453-138">-StorageAccountId</span></span>
<span data-ttu-id="8a453-139">Anger ID för det lagrings konto där du vill spara data.</span><span class="sxs-lookup"><span data-stu-id="8a453-139">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-140">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="8a453-140">-Timegrains</span></span>
<span data-ttu-id="8a453-141">Anger hur lång tid som ska aktive ras eller inaktive ras för mått enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="8a453-141">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8a453-142">Om du inte anger en tids kornig het kan det här kommandot användas för alla tillgängliga tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="8a453-142">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-143">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="8a453-143">-WorkspaceId</span></span>
<span data-ttu-id="8a453-144">ID för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="8a453-144">The Id of the workspace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a453-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a453-145">CommonParameters</span></span>
<span data-ttu-id="8a453-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a453-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a453-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a453-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a453-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a453-148">INPUTS</span></span>

### <span data-ttu-id="8a453-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a453-149">None</span></span>
<span data-ttu-id="8a453-150">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8a453-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a453-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a453-151">OUTPUTS</span></span>

### <span data-ttu-id="8a453-152">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8a453-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="8a453-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a453-153">NOTES</span></span>

## <span data-ttu-id="8a453-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a453-154">RELATED LINKS</span></span>

[<span data-ttu-id="8a453-155">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8a453-155">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


