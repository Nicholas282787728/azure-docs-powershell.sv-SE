---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271243"
---
# <span data-ttu-id="d6742-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d6742-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="d6742-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6742-102">SYNOPSIS</span></span>
<span data-ttu-id="d6742-103">Skapa en ny tröskel anpassad varnings regel för säkerhets grupp för enheter (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="d6742-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d6742-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6742-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6742-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6742-105">DESCRIPTION</span></span>
<span data-ttu-id="d6742-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet skapar en ny lista över anpassade varnings regler för säkerhets grupp i IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="d6742-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d6742-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6742-107">EXAMPLES</span></span>

### <span data-ttu-id="d6742-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6742-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="d6742-109">Skapa en ny tröskel anpassad varnings regel från typen "SomeRuleType" med status aktiverat ANT-värden för minimum-och Max tröskel</span><span class="sxs-lookup"><span data-stu-id="d6742-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="d6742-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6742-110">PARAMETERS</span></span>

### <span data-ttu-id="d6742-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6742-111">-DefaultProfile</span></span>
<span data-ttu-id="d6742-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6742-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6742-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="d6742-113">-Enabled</span></span>
<span data-ttu-id="d6742-114">Är regeln aktive rad.</span><span class="sxs-lookup"><span data-stu-id="d6742-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="d6742-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="d6742-115">-MaxThreshold</span></span>
<span data-ttu-id="d6742-116">Maximalt tröskelvärde.</span><span class="sxs-lookup"><span data-stu-id="d6742-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="d6742-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="d6742-117">-MinThreshold</span></span>
<span data-ttu-id="d6742-118">Minsta tröskel.</span><span class="sxs-lookup"><span data-stu-id="d6742-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="d6742-119">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d6742-119">-Type</span></span>
<span data-ttu-id="d6742-120">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="d6742-120">Rule type.</span></span>

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

### <span data-ttu-id="d6742-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6742-121">CommonParameters</span></span>
<span data-ttu-id="d6742-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6742-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6742-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6742-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6742-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6742-124">INPUTS</span></span>

### <span data-ttu-id="d6742-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6742-125">None</span></span>

## <span data-ttu-id="d6742-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6742-126">OUTPUTS</span></span>

### <span data-ttu-id="d6742-127">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d6742-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="d6742-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6742-128">NOTES</span></span>

## <span data-ttu-id="d6742-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6742-129">RELATED LINKS</span></span>
