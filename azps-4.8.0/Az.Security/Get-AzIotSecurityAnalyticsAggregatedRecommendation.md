---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261712"
---
# <span data-ttu-id="5020f-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="5020f-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="5020f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5020f-102">SYNOPSIS</span></span>
<span data-ttu-id="5020f-103">Få IoT-samlad rekommendation</span><span class="sxs-lookup"><span data-stu-id="5020f-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="5020f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5020f-104">SYNTAX</span></span>

### <span data-ttu-id="5020f-105">SolutionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="5020f-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5020f-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5020f-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5020f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5020f-107">DESCRIPTION</span></span>
<span data-ttu-id="5020f-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returnerar en eller flera sammansatta rekommendationer på enheter med IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5020f-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="5020f-109">Namnet på en aggregerad rekommendation är typen</span><span class="sxs-lookup"><span data-stu-id="5020f-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="5020f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5020f-110">EXAMPLES</span></span>

### <span data-ttu-id="5020f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5020f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="5020f-112">Hämta den sammanställda rekommendationen "IoT_OpenPorts" i säkerhetslösningen "lösningen" och resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5020f-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="5020f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5020f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="5020f-114">Få en lista över sammanslagna rekommendationer i säkerhetslösningen "lösningen" och resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5020f-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="5020f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5020f-115">PARAMETERS</span></span>

### <span data-ttu-id="5020f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5020f-116">-DefaultProfile</span></span>
<span data-ttu-id="5020f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5020f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5020f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5020f-118">-Name</span></span>
<span data-ttu-id="5020f-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="5020f-119">Resource name.</span></span>

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

### <span data-ttu-id="5020f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5020f-120">-ResourceGroupName</span></span>
<span data-ttu-id="5020f-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5020f-121">Resource group name.</span></span>

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

### <span data-ttu-id="5020f-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="5020f-122">-SolutionName</span></span>
<span data-ttu-id="5020f-123">Lösningens namn</span><span class="sxs-lookup"><span data-stu-id="5020f-123">Solution name</span></span>

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

### <span data-ttu-id="5020f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5020f-124">CommonParameters</span></span>
<span data-ttu-id="5020f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5020f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5020f-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5020f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5020f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5020f-127">INPUTS</span></span>

### <span data-ttu-id="5020f-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="5020f-128">None</span></span>

## <span data-ttu-id="5020f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5020f-129">OUTPUTS</span></span>

### <span data-ttu-id="5020f-130">Microsoft. Azure. commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="5020f-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="5020f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5020f-131">NOTES</span></span>

## <span data-ttu-id="5020f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5020f-132">RELATED LINKS</span></span>