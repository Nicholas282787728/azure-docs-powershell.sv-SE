---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269964"
---
# <span data-ttu-id="3c1e0-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="3c1e0-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="3c1e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1e0-103">Skapa en ny regel för att neka den anpassade varnings listan för säkerhets gruppen enhet (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="3c1e0-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="3c1e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c1e0-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c1e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="3c1e0-106">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet skapar en ny lista över nekade anpassade notifieringsregler för säkerhets gruppen enhet i IoT-säkerhetslösningen.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="3c1e0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="3c1e0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c1e0-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="3c1e0-109">Skapa en ny regel för att neka en anpassad avisering med rull typen "SomeRuleType" och status inställd på desable</span><span class="sxs-lookup"><span data-stu-id="3c1e0-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="3c1e0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c1e0-110">PARAMETERS</span></span>

### <span data-ttu-id="3c1e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1e0-111">-DefaultProfile</span></span>
<span data-ttu-id="3c1e0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1e0-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="3c1e0-113">-DenylistValue</span></span>
<span data-ttu-id="3c1e0-114">Neka List värden.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1e0-115">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="3c1e0-115">-Enabled</span></span>
<span data-ttu-id="3c1e0-116">Är regeln aktive rad.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="3c1e0-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="3c1e0-117">-Type</span></span>
<span data-ttu-id="3c1e0-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-118">Rule type.</span></span>

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

### <span data-ttu-id="3c1e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1e0-119">CommonParameters</span></span>
<span data-ttu-id="3c1e0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1e0-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c1e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1e0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c1e0-122">INPUTS</span></span>

### <span data-ttu-id="3c1e0-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c1e0-123">None</span></span>

## <span data-ttu-id="3c1e0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c1e0-124">OUTPUTS</span></span>

### <span data-ttu-id="3c1e0-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="3c1e0-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="3c1e0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c1e0-126">NOTES</span></span>

## <span data-ttu-id="3c1e0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c1e0-127">RELATED LINKS</span></span>
