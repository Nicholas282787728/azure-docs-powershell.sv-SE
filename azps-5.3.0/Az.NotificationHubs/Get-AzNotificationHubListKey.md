---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525717"
---
# <span data-ttu-id="04afc-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="04afc-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="04afc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04afc-102">SYNOPSIS</span></span>
<span data-ttu-id="04afc-103">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="04afc-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="04afc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04afc-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04afc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04afc-105">DESCRIPTION</span></span>
<span data-ttu-id="04afc-106">Cmdleten **Get-AzNotificationHubListKey** returnerar de primära och sekundära anslutnings strängarna för en auktoriseringsregel för en aviserings nav med delad åtkomst-signatur.</span><span class="sxs-lookup"><span data-stu-id="04afc-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="04afc-107">Auktoriseringsregler hantera användar rättigheter för navet.</span><span class="sxs-lookup"><span data-stu-id="04afc-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="04afc-108">Varje regel innehåller en primär och en sekundär anslutnings sträng.</span><span class="sxs-lookup"><span data-stu-id="04afc-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="04afc-109">Följande anslutnings strängar:</span><span class="sxs-lookup"><span data-stu-id="04afc-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="04afc-110">Peka användare i en resurs.</span><span class="sxs-lookup"><span data-stu-id="04afc-110">Point users to a resource.</span></span>
- <span data-ttu-id="04afc-111">Inkludera ett token som innehåller frågeparametrar.</span><span class="sxs-lookup"><span data-stu-id="04afc-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="04afc-112">En av dessa parametrar, signaturen används för att autentisera användaren och ange den angivna åtkomst nivån.</span><span class="sxs-lookup"><span data-stu-id="04afc-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="04afc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04afc-113">EXAMPLES</span></span>

### <span data-ttu-id="04afc-114">Exempel 1: Hämta primära och sekundära anslutnings strängar för en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="04afc-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="04afc-115">Det här kommandot hämtar de primära och sekundära anslutnings strängarna för auktoriseringsregeln ListenRule, en regel som tilldelats meddelande navet för ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="04afc-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="04afc-116">Kommandot måste innehålla hubb namn området och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="04afc-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="04afc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04afc-117">PARAMETERS</span></span>

### <span data-ttu-id="04afc-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="04afc-118">-AuthorizationRule</span></span>
<span data-ttu-id="04afc-119">Anger namnet på en autentiseringsprincip för en delad Access-signatur.</span><span class="sxs-lookup"><span data-stu-id="04afc-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="04afc-120">Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="04afc-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04afc-121">-DefaultProfile</span></span>
<span data-ttu-id="04afc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="04afc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04afc-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="04afc-123">-Namespace</span></span>
<span data-ttu-id="04afc-124">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="04afc-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="04afc-125">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="04afc-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afc-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="04afc-126">-NotificationHub</span></span>
<span data-ttu-id="04afc-127">Anger meddelandets hubb som denna cmdlet tilldelar en auktoriseringsregel till.</span><span class="sxs-lookup"><span data-stu-id="04afc-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="04afc-128">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="04afc-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afc-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04afc-129">-ResourceGroup</span></span>
<span data-ttu-id="04afc-130">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="04afc-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="04afc-131">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="04afc-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04afc-132">CommonParameters</span></span>
<span data-ttu-id="04afc-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04afc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04afc-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04afc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04afc-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04afc-135">INPUTS</span></span>

### <span data-ttu-id="04afc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="04afc-136">System.String</span></span>

## <span data-ttu-id="04afc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04afc-137">OUTPUTS</span></span>

### <span data-ttu-id="04afc-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="04afc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="04afc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04afc-139">NOTES</span></span>

## <span data-ttu-id="04afc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04afc-140">RELATED LINKS</span></span>

[<span data-ttu-id="04afc-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="04afc-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


