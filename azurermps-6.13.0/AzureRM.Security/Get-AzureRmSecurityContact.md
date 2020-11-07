---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757028"
---
# <span data-ttu-id="09673-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="09673-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="09673-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09673-102">SYNOPSIS</span></span>
<span data-ttu-id="09673-103">Hämtar säkerhets kontakter som har kon figurer ATS för detta abonnemang</span><span class="sxs-lookup"><span data-stu-id="09673-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09673-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09673-104">SYNTAX</span></span>

### <span data-ttu-id="09673-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="09673-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09673-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="09673-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09673-107">ID</span><span class="sxs-lookup"><span data-stu-id="09673-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09673-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09673-108">DESCRIPTION</span></span>
<span data-ttu-id="09673-109">Hämtar säkerhets kontakter som har kon figurer ATS för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09673-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="09673-110">Säkerhets kontakten får aviseringar om säkerhets varningar som uppstår på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09673-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="09673-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09673-111">EXAMPLES</span></span>

### <span data-ttu-id="09673-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09673-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="09673-113">Hämtar alla konfigurerade säkerhets kontakter för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="09673-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="09673-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09673-114">PARAMETERS</span></span>

### <span data-ttu-id="09673-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09673-115">-DefaultProfile</span></span>
<span data-ttu-id="09673-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09673-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09673-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="09673-117">-Name</span></span>
<span data-ttu-id="09673-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="09673-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09673-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09673-119">-ResourceId</span></span>
<span data-ttu-id="09673-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="09673-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09673-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09673-121">CommonParameters</span></span>
<span data-ttu-id="09673-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09673-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09673-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09673-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09673-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09673-124">INPUTS</span></span>

### <span data-ttu-id="09673-125">System. String</span><span class="sxs-lookup"><span data-stu-id="09673-125">System.String</span></span>

## <span data-ttu-id="09673-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09673-126">OUTPUTS</span></span>

### <span data-ttu-id="09673-127">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="09673-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="09673-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09673-128">NOTES</span></span>

## <span data-ttu-id="09673-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09673-129">RELATED LINKS</span></span>
