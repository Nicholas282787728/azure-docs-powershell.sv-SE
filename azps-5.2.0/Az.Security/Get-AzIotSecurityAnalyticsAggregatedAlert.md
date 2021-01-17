---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416336"
---
# <span data-ttu-id="dffff-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="dffff-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="dffff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dffff-102">SYNOPSIS</span></span>
<span data-ttu-id="dffff-103">Få IoT Security Aggregate-avisering</span><span class="sxs-lookup"><span data-stu-id="dffff-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="dffff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dffff-104">SYNTAX</span></span>

### <span data-ttu-id="dffff-105">SolutionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="dffff-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffff-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="dffff-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dffff-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dffff-107">DESCRIPTION</span></span>
<span data-ttu-id="dffff-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returnerar en eller flera aggregerade aviseringar på enheter i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="dffff-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="dffff-109">Namnet på de aggregerade varningarna är en kombination av varnings typen och aviseringens aggragted-datum, avgränsade med "/".</span><span class="sxs-lookup"><span data-stu-id="dffff-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="dffff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dffff-110">EXAMPLES</span></span>

### <span data-ttu-id="dffff-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dffff-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="dffff-112">Hämta den sammanställda varningen "IoT_Bruteforce_Fail/2019-02-02" (namnet som kombineras med aviserings typen och dess aggregerade datum) i lösning "problemlösning" och resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="dffff-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="dffff-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dffff-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="dffff-114">Få en lista över alla aggregerade aviseringar i lösningen "lösning" och resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="dffff-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="dffff-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dffff-115">PARAMETERS</span></span>

### <span data-ttu-id="dffff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffff-116">-DefaultProfile</span></span>
<span data-ttu-id="dffff-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dffff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dffff-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dffff-118">-Name</span></span>
<span data-ttu-id="dffff-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="dffff-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffff-120">-ResourceGroupName</span></span>
<span data-ttu-id="dffff-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dffff-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffff-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="dffff-122">-SolutionName</span></span>
<span data-ttu-id="dffff-123">Lösningens namn</span><span class="sxs-lookup"><span data-stu-id="dffff-123">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffff-124">CommonParameters</span></span>
<span data-ttu-id="dffff-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffff-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dffff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffff-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dffff-127">INPUTS</span></span>

### <span data-ttu-id="dffff-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="dffff-128">None</span></span>

## <span data-ttu-id="dffff-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dffff-129">OUTPUTS</span></span>

### <span data-ttu-id="dffff-130">Microsoft. Azure. commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="dffff-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="dffff-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dffff-131">NOTES</span></span>

## <span data-ttu-id="dffff-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dffff-132">RELATED LINKS</span></span>
