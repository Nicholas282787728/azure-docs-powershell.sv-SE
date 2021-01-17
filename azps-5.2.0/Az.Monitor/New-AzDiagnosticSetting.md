---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405032"
---
# <span data-ttu-id="041be-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="041be-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="041be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="041be-102">SYNOPSIS</span></span>
<span data-ttu-id="041be-103">Skapa PSServiceDiagnosticSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="041be-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="041be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="041be-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="041be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="041be-105">DESCRIPTION</span></span>
<span data-ttu-id="041be-106">Skapa PSServiceDiagnosticSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="041be-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="041be-107">Den kan användas som parameter `-InputObject` för `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="041be-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="041be-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="041be-108">EXAMPLES</span></span>

### <span data-ttu-id="041be-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="041be-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="041be-110">Skapa PSServiceDiagnosticSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="041be-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="041be-111">Och skapa en diagnostisk inställning för mål resursen.</span><span class="sxs-lookup"><span data-stu-id="041be-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="041be-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="041be-112">PARAMETERS</span></span>

### <span data-ttu-id="041be-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="041be-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="041be-114">Det värde som anger om du vill exportera (to ODS) till resursfiler (om den finns) eller till AzureDiagnostics (standard, inte tillgänglig)</span><span class="sxs-lookup"><span data-stu-id="041be-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041be-115">-DefaultProfile</span></span>
<span data-ttu-id="041be-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="041be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="041be-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="041be-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="041be-118">Regel-ID för händelsehubben</span><span class="sxs-lookup"><span data-stu-id="041be-118">The event hub rule id</span></span>

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

### <span data-ttu-id="041be-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="041be-119">-EventHubName</span></span>
<span data-ttu-id="041be-120">ID för Service Bus-regel</span><span class="sxs-lookup"><span data-stu-id="041be-120">The service bus rule id</span></span>

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

### <span data-ttu-id="041be-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="041be-121">-Name</span></span>
<span data-ttu-id="041be-122">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="041be-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="041be-123">Standard är "tjänst"</span><span class="sxs-lookup"><span data-stu-id="041be-123">Defaults to 'service'</span></span>

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

### <span data-ttu-id="041be-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="041be-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="041be-125">ID för Service Bus-regel</span><span class="sxs-lookup"><span data-stu-id="041be-125">The service bus rule id</span></span>

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

### <span data-ttu-id="041be-126">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="041be-126">-Setting</span></span>
<span data-ttu-id="041be-127">Inställningar för mått eller logg inställningar</span><span class="sxs-lookup"><span data-stu-id="041be-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041be-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="041be-128">-StorageAccountId</span></span>
<span data-ttu-id="041be-129">ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="041be-129">The storage account id</span></span>

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

### <span data-ttu-id="041be-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="041be-130">-TargetResourceId</span></span>
<span data-ttu-id="041be-131">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="041be-131">The resource id</span></span>

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

### <span data-ttu-id="041be-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="041be-132">-WorkspaceId</span></span>
<span data-ttu-id="041be-133">Resurs-ID för logg analys arbets ytan för att skicka loggar/mått till</span><span class="sxs-lookup"><span data-stu-id="041be-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="041be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041be-134">CommonParameters</span></span>
<span data-ttu-id="041be-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="041be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041be-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="041be-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041be-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="041be-137">INPUTS</span></span>

### <span data-ttu-id="041be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="041be-138">System.String</span></span>

### <span data-ttu-id="041be-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="041be-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="041be-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings []</span><span class="sxs-lookup"><span data-stu-id="041be-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="041be-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="041be-141">OUTPUTS</span></span>

### <span data-ttu-id="041be-142">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="041be-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="041be-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="041be-143">NOTES</span></span>

## <span data-ttu-id="041be-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="041be-144">RELATED LINKS</span></span>
