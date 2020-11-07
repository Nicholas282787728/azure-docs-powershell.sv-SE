---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: cfdf4c9131cff3f7d45d0898e361ea54883a4503
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919244"
---
# <span data-ttu-id="e0f5f-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="e0f5f-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="e0f5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f5f-103">Hämtar säkerhets kontakter som har kon figurer ATS för detta abonnemang</span><span class="sxs-lookup"><span data-stu-id="e0f5f-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="e0f5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0f5f-104">SYNTAX</span></span>

### <span data-ttu-id="e0f5f-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="e0f5f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f5f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e0f5f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f5f-107">ID</span><span class="sxs-lookup"><span data-stu-id="e0f5f-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0f5f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0f5f-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f5f-109">Hämtar säkerhets kontakter som har kon figurer ATS för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="e0f5f-110">Säkerhets kontakten får aviseringar om säkerhets varningar som uppstår på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="e0f5f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="e0f5f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0f5f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="e0f5f-113">Hämtar alla konfigurerade säkerhets kontakter för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e0f5f-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="e0f5f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0f5f-114">PARAMETERS</span></span>

### <span data-ttu-id="e0f5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f5f-115">-DefaultProfile</span></span>
<span data-ttu-id="e0f5f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f5f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0f5f-117">-Name</span></span>
<span data-ttu-id="e0f5f-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f5f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f5f-119">-ResourceId</span></span>
<span data-ttu-id="e0f5f-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f5f-121">CommonParameters</span></span>
<span data-ttu-id="e0f5f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f5f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f5f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f5f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0f5f-124">INPUTS</span></span>

### <span data-ttu-id="e0f5f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f5f-125">System.String</span></span>

## <span data-ttu-id="e0f5f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0f5f-126">OUTPUTS</span></span>

### <span data-ttu-id="e0f5f-127">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="e0f5f-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="e0f5f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0f5f-128">NOTES</span></span>

## <span data-ttu-id="e0f5f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0f5f-129">RELATED LINKS</span></span>
