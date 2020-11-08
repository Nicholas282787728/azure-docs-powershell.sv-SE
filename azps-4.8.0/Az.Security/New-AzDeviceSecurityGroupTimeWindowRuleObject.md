---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261715"
---
# <span data-ttu-id="9522b-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="9522b-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="9522b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9522b-102">SYNOPSIS</span></span>
<span data-ttu-id="9522b-103">Skapa en ny tidsfönster regel för gruppen enhets säkerhet (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="9522b-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9522b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9522b-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9522b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9522b-105">DESCRIPTION</span></span>
<span data-ttu-id="9522b-106">New-AzDeviceSecurityGroupTimeWindowRuleObject-cmdleten skapar en ny lista över notifieringsregler för säkerhets gruppen enhet i IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="9522b-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9522b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9522b-107">EXAMPLES</span></span>

### <span data-ttu-id="9522b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9522b-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="9522b-109">Skapa en ny tidsfönster regel från typen "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="9522b-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="9522b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9522b-110">PARAMETERS</span></span>

### <span data-ttu-id="9522b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9522b-111">-DefaultProfile</span></span>
<span data-ttu-id="9522b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9522b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9522b-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="9522b-113">-Enabled</span></span>
<span data-ttu-id="9522b-114">Är regeln aktive rad.</span><span class="sxs-lookup"><span data-stu-id="9522b-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9522b-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="9522b-115">-MaxThreshold</span></span>
<span data-ttu-id="9522b-116">Maximalt tröskelvärde.</span><span class="sxs-lookup"><span data-stu-id="9522b-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9522b-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="9522b-117">-MinThreshold</span></span>
<span data-ttu-id="9522b-118">Minsta tröskel.</span><span class="sxs-lookup"><span data-stu-id="9522b-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9522b-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="9522b-119">-TimeWindowSize</span></span>
<span data-ttu-id="9522b-120">Tidsfönster storlek.</span><span class="sxs-lookup"><span data-stu-id="9522b-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9522b-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9522b-121">-Type</span></span>
<span data-ttu-id="9522b-122">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="9522b-122">Rule type.</span></span>

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

### <span data-ttu-id="9522b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9522b-123">CommonParameters</span></span>
<span data-ttu-id="9522b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9522b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9522b-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9522b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9522b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9522b-126">INPUTS</span></span>

### <span data-ttu-id="9522b-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="9522b-127">None</span></span>

## <span data-ttu-id="9522b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9522b-128">OUTPUTS</span></span>

### <span data-ttu-id="9522b-129">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9522b-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="9522b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9522b-130">NOTES</span></span>

## <span data-ttu-id="9522b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9522b-131">RELATED LINKS</span></span>
