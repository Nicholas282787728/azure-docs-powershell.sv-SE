---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092230"
---
# <span data-ttu-id="adc3c-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="adc3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="adc3c-103">Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="adc3c-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="adc3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adc3c-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adc3c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adc3c-105">DESCRIPTION</span></span>
<span data-ttu-id="adc3c-106">Cmdleten **Get-AzNotificationHubAuthorizationRule** hämtar information om de auktoriseringsregler som är associerade med en meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="adc3c-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="adc3c-107">Cmdleten returnerar information om alla regler som associeras med ett nav eller, genom att inkludera parametern *AuthorizationRule* , får du information om en viss regel.</span><span class="sxs-lookup"><span data-stu-id="adc3c-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="adc3c-108">Auktoriseringsregler hantera åtkomst till dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="adc3c-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="adc3c-109">En auktoriseringsregel skapar länkar, som en URI, baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="adc3c-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="adc3c-110">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="adc3c-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="adc3c-111">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="adc3c-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="adc3c-112">Cmdleten **Get-AzNotificationHubAuthorizationRule** får bara information om de auktoriseringsregler som är associerade med en meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="adc3c-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="adc3c-113">Använd Get-AzNotificationHub för att få information om navet själv.</span><span class="sxs-lookup"><span data-stu-id="adc3c-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="adc3c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adc3c-114">EXAMPLES</span></span>

### <span data-ttu-id="adc3c-115">Exempel 1: Hämta information om alla auktoriseringsregler som tilldelats ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="adc3c-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="adc3c-116">Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="adc3c-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="adc3c-117">Du måste ange namn området där navet finns samt resurs gruppen som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="adc3c-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="adc3c-118">Exempel 2: Hämta information om en auktoriseringsregel som tilldelats ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="adc3c-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="adc3c-119">Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="adc3c-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="adc3c-120">Kommandot använder parametern *AuthorizationRule* för att begränsa vilka data som returneras till en enda auktoriseringsregel med namnet ListenRule.</span><span class="sxs-lookup"><span data-stu-id="adc3c-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="adc3c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adc3c-121">PARAMETERS</span></span>

### <span data-ttu-id="adc3c-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-122">-AuthorizationRule</span></span>
<span data-ttu-id="adc3c-123">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="adc3c-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="adc3c-124">Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="adc3c-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc3c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc3c-125">-DefaultProfile</span></span>
<span data-ttu-id="adc3c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="adc3c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adc3c-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="adc3c-127">-Namespace</span></span>
<span data-ttu-id="adc3c-128">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="adc3c-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="adc3c-129">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="adc3c-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="adc3c-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="adc3c-130">-NotificationHub</span></span>
<span data-ttu-id="adc3c-131">Anger meddelandets hubb som den här cmdleten tilldelar auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="adc3c-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="adc3c-132">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="adc3c-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="adc3c-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="adc3c-133">-ResourceGroup</span></span>
<span data-ttu-id="adc3c-134">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="adc3c-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="adc3c-135">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar hantering av lager och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="adc3c-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="adc3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc3c-136">CommonParameters</span></span>
<span data-ttu-id="adc3c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc3c-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc3c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc3c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adc3c-139">INPUTS</span></span>

### <span data-ttu-id="adc3c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="adc3c-140">System.String</span></span>

## <span data-ttu-id="adc3c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adc3c-141">OUTPUTS</span></span>

### <span data-ttu-id="adc3c-142">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="adc3c-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="adc3c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adc3c-143">NOTES</span></span>

## <span data-ttu-id="adc3c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adc3c-144">RELATED LINKS</span></span>

[<span data-ttu-id="adc3c-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="adc3c-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="adc3c-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="adc3c-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="adc3c-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


