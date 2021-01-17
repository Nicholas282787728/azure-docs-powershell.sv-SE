---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396083"
---
# <span data-ttu-id="20a62-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="20a62-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="20a62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20a62-102">SYNOPSIS</span></span>
<span data-ttu-id="20a62-103">Skaffa IoT Security Analytics</span><span class="sxs-lookup"><span data-stu-id="20a62-103">Get IoT security analytics</span></span>

## <span data-ttu-id="20a62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20a62-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20a62-105">DESCRIPTION</span></span>
<span data-ttu-id="20a62-106">Get-AzIotSecurityAnalytics cmdlet returnerar en uppsättning säkerhets analyser för en specifik IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="20a62-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="20a62-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20a62-107">EXAMPLES</span></span>

### <span data-ttu-id="20a62-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20a62-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="20a62-109">Skaffa deafult IoT Security Analytics för säkerhets lösning "testlösning" i reasource-gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="20a62-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="20a62-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20a62-110">PARAMETERS</span></span>

### <span data-ttu-id="20a62-111">-Standard</span><span class="sxs-lookup"><span data-stu-id="20a62-111">-Default</span></span>
<span data-ttu-id="20a62-112">Om det finns en standard analys kan du hämta en lista över alla analys uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="20a62-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a62-113">-DefaultProfile</span></span>
<span data-ttu-id="20a62-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20a62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a62-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a62-115">-ResourceGroupName</span></span>
<span data-ttu-id="20a62-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="20a62-116">Resource group name.</span></span>

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

### <span data-ttu-id="20a62-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="20a62-117">-SolutionName</span></span>
<span data-ttu-id="20a62-118">Lösningens namn</span><span class="sxs-lookup"><span data-stu-id="20a62-118">Solution name</span></span>

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

### <span data-ttu-id="20a62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a62-119">CommonParameters</span></span>
<span data-ttu-id="20a62-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a62-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a62-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a62-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20a62-122">INPUTS</span></span>

### <span data-ttu-id="20a62-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="20a62-123">None</span></span>

## <span data-ttu-id="20a62-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20a62-124">OUTPUTS</span></span>

### <span data-ttu-id="20a62-125">Microsoft. Azure. commands. Security. Models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="20a62-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="20a62-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20a62-126">NOTES</span></span>

## <span data-ttu-id="20a62-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20a62-127">RELATED LINKS</span></span>
