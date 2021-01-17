---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396051"
---
# <span data-ttu-id="e0040-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="e0040-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="e0040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0040-102">SYNOPSIS</span></span>
<span data-ttu-id="e0040-103">Skapa en anpassad varnings regel för listan Tillåt</span><span class="sxs-lookup"><span data-stu-id="e0040-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="e0040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0040-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0040-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0040-105">DESCRIPTION</span></span>
<span data-ttu-id="e0040-106">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet skapar en ny lista över tillåtna anpassade notifieringsregler för säkerhets gruppen enhet i IoT-säkerhetslösningen.</span><span class="sxs-lookup"><span data-stu-id="e0040-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="e0040-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0040-107">EXAMPLES</span></span>

### <span data-ttu-id="e0040-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0040-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="e0040-109">Skapa en ny lista för att tillåta anpassad avisering rull från typen "LocalUserNotAllowed" med status inställd på Disable</span><span class="sxs-lookup"><span data-stu-id="e0040-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="e0040-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0040-110">PARAMETERS</span></span>

### <span data-ttu-id="e0040-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="e0040-111">-AllowlistValue</span></span>
<span data-ttu-id="e0040-112">Tillåt List värden.</span><span class="sxs-lookup"><span data-stu-id="e0040-112">Allow list values.</span></span>

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

### <span data-ttu-id="e0040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0040-113">-DefaultProfile</span></span>
<span data-ttu-id="e0040-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0040-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0040-115">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="e0040-115">-Enabled</span></span>
<span data-ttu-id="e0040-116">Är regeln aktive rad.</span><span class="sxs-lookup"><span data-stu-id="e0040-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="e0040-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e0040-117">-Type</span></span>
<span data-ttu-id="e0040-118">Regeltyp.</span><span class="sxs-lookup"><span data-stu-id="e0040-118">Rule type.</span></span>

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

### <span data-ttu-id="e0040-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0040-119">CommonParameters</span></span>
<span data-ttu-id="e0040-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0040-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0040-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0040-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0040-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0040-122">INPUTS</span></span>

### <span data-ttu-id="e0040-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0040-123">None</span></span>

## <span data-ttu-id="e0040-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0040-124">OUTPUTS</span></span>

### <span data-ttu-id="e0040-125">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="e0040-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="e0040-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0040-126">NOTES</span></span>

## <span data-ttu-id="e0040-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0040-127">RELATED LINKS</span></span>
