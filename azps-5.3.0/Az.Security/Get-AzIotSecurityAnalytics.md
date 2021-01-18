---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525683"
---
# <span data-ttu-id="59a4d-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="59a4d-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="59a4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="59a4d-103">Skaffa IoT Security Analytics</span><span class="sxs-lookup"><span data-stu-id="59a4d-103">Get IoT security analytics</span></span>

## <span data-ttu-id="59a4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59a4d-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59a4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="59a4d-106">Get-AzIotSecurityAnalytics cmdlet returnerar en uppsättning säkerhets analyser för en specifik IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="59a4d-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="59a4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="59a4d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59a4d-108">Example 1</span></span>
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

<span data-ttu-id="59a4d-109">Skaffa deafult IoT Security Analytics för säkerhets lösning "testlösning" i reasource-gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="59a4d-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="59a4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="59a4d-111">-Standard</span><span class="sxs-lookup"><span data-stu-id="59a4d-111">-Default</span></span>
<span data-ttu-id="59a4d-112">Om det finns en standard analys kan du hämta en lista över alla analys uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="59a4d-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="59a4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a4d-113">-DefaultProfile</span></span>
<span data-ttu-id="59a4d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59a4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59a4d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a4d-115">-ResourceGroupName</span></span>
<span data-ttu-id="59a4d-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="59a4d-116">Resource group name.</span></span>

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

### <span data-ttu-id="59a4d-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="59a4d-117">-SolutionName</span></span>
<span data-ttu-id="59a4d-118">Lösningens namn</span><span class="sxs-lookup"><span data-stu-id="59a4d-118">Solution name</span></span>

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

### <span data-ttu-id="59a4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a4d-119">CommonParameters</span></span>
<span data-ttu-id="59a4d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a4d-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59a4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a4d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59a4d-122">INPUTS</span></span>

### <span data-ttu-id="59a4d-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="59a4d-123">None</span></span>

## <span data-ttu-id="59a4d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59a4d-124">OUTPUTS</span></span>

### <span data-ttu-id="59a4d-125">Microsoft. Azure. commands. Security. Models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="59a4d-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="59a4d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59a4d-126">NOTES</span></span>

## <span data-ttu-id="59a4d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59a4d-127">RELATED LINKS</span></span>
