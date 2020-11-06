---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: db2b3357b7db90b5d5b310c43afb3f29ca596878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578824"
---
# <span data-ttu-id="a16e8-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a16e8-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="a16e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a16e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a16e8-103">Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="a16e8-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a16e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a16e8-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a16e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a16e8-105">DESCRIPTION</span></span>
<span data-ttu-id="a16e8-106">Cmdleten **Get-AzureRmNotificationHubAuthorizationRules** hämtar information om de auktoriseringsregler som är associerade med en meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="a16e8-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="a16e8-107">Cmdleten returnerar information om alla regler som associeras med ett nav eller, genom att inkludera parametern *AuthorizationRule* , får du information om en viss regel.</span><span class="sxs-lookup"><span data-stu-id="a16e8-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="a16e8-108">Auktoriseringsregler hantera åtkomst till dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="a16e8-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="a16e8-109">En auktoriseringsregel skapar länkar, som en URI, baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="a16e8-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="a16e8-110">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="a16e8-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="a16e8-111">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="a16e8-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="a16e8-112">Cmdleten **Get-AzureRmNotificationHubAuthorizationRules** får bara information om de auktoriseringsregler som är associerade med en meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="a16e8-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="a16e8-113">Använd Get-AzureRmNotificationHub för att få information om navet själv.</span><span class="sxs-lookup"><span data-stu-id="a16e8-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="a16e8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a16e8-114">EXAMPLES</span></span>

### <span data-ttu-id="a16e8-115">Exempel 1: Hämta information om alla auktoriseringsregler som tilldelats ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="a16e8-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="a16e8-116">Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a16e8-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="a16e8-117">Du måste ange namn området där navet finns samt resurs gruppen som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a16e8-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="a16e8-118">Exempel 2: Hämta information om en auktoriseringsregel som tilldelats ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="a16e8-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="a16e8-119">Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a16e8-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="a16e8-120">Kommandot använder parametern *AuthorizationRule* för att begränsa vilka data som returneras till en enda auktoriseringsregel med namnet ListenRule.</span><span class="sxs-lookup"><span data-stu-id="a16e8-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="a16e8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a16e8-121">PARAMETERS</span></span>

### <span data-ttu-id="a16e8-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a16e8-122">-AuthorizationRule</span></span>
<span data-ttu-id="a16e8-123">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="a16e8-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="a16e8-124">Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="a16e8-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="a16e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16e8-125">-DefaultProfile</span></span>
<span data-ttu-id="a16e8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a16e8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e8-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a16e8-127">-Namespace</span></span>
<span data-ttu-id="a16e8-128">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a16e8-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a16e8-129">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="a16e8-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a16e8-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a16e8-130">-NotificationHub</span></span>
<span data-ttu-id="a16e8-131">Anger meddelandets hubb som den här cmdleten tilldelar auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="a16e8-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="a16e8-132">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="a16e8-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="a16e8-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a16e8-133">-ResourceGroup</span></span>
<span data-ttu-id="a16e8-134">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a16e8-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a16e8-135">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar hantering av lager och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="a16e8-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a16e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16e8-136">CommonParameters</span></span>
<span data-ttu-id="a16e8-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16e8-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a16e8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16e8-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a16e8-139">INPUTS</span></span>

### <span data-ttu-id="a16e8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a16e8-140">System.String</span></span>

## <span data-ttu-id="a16e8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a16e8-141">OUTPUTS</span></span>

### <span data-ttu-id="a16e8-142">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a16e8-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a16e8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a16e8-143">NOTES</span></span>

## <span data-ttu-id="a16e8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a16e8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a16e8-145">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a16e8-145">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="a16e8-146">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a16e8-146">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a16e8-147">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a16e8-147">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a16e8-148">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a16e8-148">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


