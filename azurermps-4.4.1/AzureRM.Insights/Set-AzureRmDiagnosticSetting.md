---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756597"
---
# <span data-ttu-id="d4d0c-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4d0c-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="d4d0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d0c-103">Ange inställningar för loggar och mått för resursen.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4d0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4d0c-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4d0c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d0c-106">Cmdleten **set-AzureRmDiagnosticSetting** aktiverar eller inaktiverar varje tidpunkt och log-kategori för den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="d4d0c-107">Loggar och mått lagras i angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="d4d0c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4d0c-108">EXAMPLES</span></span>

### <span data-ttu-id="d4d0c-109">Exempel 1: Aktivera alla mått och loggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="d4d0c-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="d4d0c-110">Det här kommandot aktiverar alla tillgängliga mått och loggar för Resource01.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="d4d0c-111">Exempel 2: inaktivera alla mått och loggar</span><span class="sxs-lookup"><span data-stu-id="d4d0c-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="d4d0c-112">Det här kommandot inaktiverar alla tillgängliga mått och loggar för resursens Resource01.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="d4d0c-113">Exempel 3: aktivera flera kategorier</span><span class="sxs-lookup"><span data-stu-id="d4d0c-113">Example 3: Enable multiple categories</span></span>
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

<span data-ttu-id="d4d0c-114">Det här kommandot aktiverar Category1 och Category2.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="d4d0c-115">Alla timegrains och andra kategorier förblir desamma.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="d4d0c-116">Exempel 4: Aktivera tids kornig het och flera kategorier</span><span class="sxs-lookup"><span data-stu-id="d4d0c-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="d4d0c-117">Det här kommandot aktiverar endast Category1, Category2 och Time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="d4d0c-118">Alla andra tidsenheter och kategorier är oförändrade.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="d4d0c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4d0c-119">PARAMETERS</span></span>

### <span data-ttu-id="d4d0c-120">-Kategorier</span><span class="sxs-lookup"><span data-stu-id="d4d0c-120">-Categories</span></span>
<span data-ttu-id="d4d0c-121">Anger listan över loggnings kategorier som ska aktive ras eller inaktive ras enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d4d0c-122">Om du inte anger en kategori används det här kommandot i alla kategorier.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-122">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="d4d0c-123">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="d4d0c-123">-Enabled</span></span>
<span data-ttu-id="d4d0c-124">Anger om diagnostik ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="d4d0c-125">Ange $True för att aktivera diagnostik eller $False för att inaktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d0c-126">-ResourceId</span></span>
<span data-ttu-id="d4d0c-127">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="d4d0c-128">-RetentionEnabled</span></span>
<span data-ttu-id="d4d0c-129">Anger om att diagnostikinformation är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d4d0c-130">-RetentionInDays</span></span>
<span data-ttu-id="d4d0c-131">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="d4d0c-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4d0c-133">-StorageAccountId</span></span>
<span data-ttu-id="d4d0c-134">Anger ID för det lagrings konto där du vill spara data.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="d4d0c-135">-Timegrains</span></span>
<span data-ttu-id="d4d0c-136">Anger hur lång tid som ska aktive ras eller inaktive ras för mått enligt värdet för *aktive rad*.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d4d0c-137">Om du inte anger en tids kornig het kan det här kommandot användas för alla tillgängliga tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="d4d0c-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d4d0c-138">-WorkspaceId</span></span>
<span data-ttu-id="d4d0c-139">ID för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="d4d0c-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d0c-140">-DefaultProfile</span></span>
<span data-ttu-id="d4d0c-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4d0c-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="d4d0c-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="d4d0c-143">Regel-ID för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="d4d0c-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d0c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d0c-144">CommonParameters</span></span>
<span data-ttu-id="d4d0c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d0c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d0c-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d0c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d0c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4d0c-147">INPUTS</span></span>

## <span data-ttu-id="d4d0c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4d0c-148">OUTPUTS</span></span>

### <span data-ttu-id="d4d0c-149">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="d4d0c-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d4d0c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4d0c-150">NOTES</span></span>

## <span data-ttu-id="d4d0c-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4d0c-151">RELATED LINKS</span></span>

[<span data-ttu-id="d4d0c-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4d0c-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


