---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420923"
---
# <span data-ttu-id="566c2-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="566c2-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="566c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="566c2-102">SYNOPSIS</span></span>
<span data-ttu-id="566c2-103">Skapa en ny tröskel anpassad varnings regel för säkerhets grupp för enheter (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="566c2-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="566c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="566c2-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="566c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="566c2-105">DESCRIPTION</span></span>
<span data-ttu-id="566c2-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet skapar en ny lista över anpassade varnings regler för säkerhets grupp i IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="566c2-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="566c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="566c2-107">EXAMPLES</span></span>

### <span data-ttu-id="566c2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="566c2-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="566c2-109">Skapa en ny tröskel anpassad varnings regel från typen "SomeRuleType" med status aktiverat ANT-värden för minimum-och Max tröskel</span><span class="sxs-lookup"><span data-stu-id="566c2-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="566c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="566c2-110">PARAMETERS</span></span>

### <span data-ttu-id="566c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566c2-111">-DefaultProfile</span></span>
<span data-ttu-id="566c2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="566c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="566c2-113">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="566c2-113">-Enabled</span></span>
<span data-ttu-id="566c2-114">Är regeln aktive rad.</span><span class="sxs-lookup"><span data-stu-id="566c2-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="566c2-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="566c2-115">-MaxThreshold</span></span>
<span data-ttu-id="566c2-116">Maximalt tröskelvärde.</span><span class="sxs-lookup"><span data-stu-id="566c2-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="566c2-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="566c2-117">-MinThreshold</span></span>
<span data-ttu-id="566c2-118">Minsta tröskel.</span><span class="sxs-lookup"><span data-stu-id="566c2-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="566c2-119">– Skriv</span><span class="sxs-lookup"><span data-stu-id="566c2-119">-Type</span></span>
<span data-ttu-id="566c2-120">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="566c2-120">Rule type.</span></span>

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

### <span data-ttu-id="566c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566c2-121">CommonParameters</span></span>
<span data-ttu-id="566c2-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566c2-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="566c2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566c2-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="566c2-124">INPUTS</span></span>

### <span data-ttu-id="566c2-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="566c2-125">None</span></span>

## <span data-ttu-id="566c2-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="566c2-126">OUTPUTS</span></span>

### <span data-ttu-id="566c2-127">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="566c2-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="566c2-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="566c2-128">NOTES</span></span>

## <span data-ttu-id="566c2-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="566c2-129">RELATED LINKS</span></span>
