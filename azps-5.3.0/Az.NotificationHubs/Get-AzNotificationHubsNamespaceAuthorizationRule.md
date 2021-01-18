---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527416"
---
# <span data-ttu-id="d4d86-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4d86-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d4d86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4d86-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d86-103">Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="d4d86-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="d4d86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4d86-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d86-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4d86-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d86-106">Cmdleten **Get-AzNotificationHubsNamespaceAuthorizationRule** returnerar information om behörighets reglerna för de delade Access-signaturerna (säkerhets associationer) som är associerade med ett namn område.</span><span class="sxs-lookup"><span data-stu-id="d4d86-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="d4d86-107">Du kan returnera information om alla regler som är kopplade till namn området.</span><span class="sxs-lookup"><span data-stu-id="d4d86-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="d4d86-108">Du kan också returnera information för en viss regel genom att ta med parametern *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="d4d86-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="d4d86-109">Auktoriseringsregler hanterar åtkomst till namn utrymmen.</span><span class="sxs-lookup"><span data-stu-id="d4d86-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="d4d86-110">Detta görs genom att länkar skapas som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="d4d86-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d4d86-111">Plattforms nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="d4d86-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="d4d86-112">Lyssna</span><span class="sxs-lookup"><span data-stu-id="d4d86-112">Listen</span></span>
- <span data-ttu-id="d4d86-113">Bifoga</span><span class="sxs-lookup"><span data-stu-id="d4d86-113">Send</span></span>
- <span data-ttu-id="d4d86-114">Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="d4d86-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d4d86-115">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="d4d86-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="d4d86-116">Denna cmdlet får bara auktoriseringsregler som är associerade med ett namn område.</span><span class="sxs-lookup"><span data-stu-id="d4d86-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="d4d86-117">Använd Get-AzNotificationHubsNamespace för att få information om själva namn området.</span><span class="sxs-lookup"><span data-stu-id="d4d86-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="d4d86-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4d86-118">EXAMPLES</span></span>

### <span data-ttu-id="d4d86-119">Exempel 1: få information om alla auktoriseringsregler som tilldelats till namn områden</span><span class="sxs-lookup"><span data-stu-id="d4d86-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="d4d86-120">Med det här kommandot får du information om alla auktoriseringsregler som tilldelats både namn områdets ContosoNamespace och ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d4d86-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d4d86-121">Exempel 2: Hämta information om en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="d4d86-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="d4d86-122">Det här kommandot får information om en enda auktoriseringsregel med namnet ListenRule.</span><span class="sxs-lookup"><span data-stu-id="d4d86-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="d4d86-123">Du måste inkludera namn området och resurs gruppen när du får information för en specifik auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="d4d86-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="d4d86-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4d86-124">PARAMETERS</span></span>

### <span data-ttu-id="d4d86-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4d86-125">-AuthorizationRule</span></span>
<span data-ttu-id="d4d86-126">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="d4d86-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="d4d86-127">Dessa regler bestämmer vilken typ av åtkomst användare har till namn området.</span><span class="sxs-lookup"><span data-stu-id="d4d86-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d86-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d86-128">-DefaultProfile</span></span>
<span data-ttu-id="d4d86-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d4d86-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4d86-130">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d4d86-130">-Namespace</span></span>
<span data-ttu-id="d4d86-131">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="d4d86-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d4d86-132">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d4d86-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d4d86-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d4d86-133">-ResourceGroup</span></span>
<span data-ttu-id="d4d86-134">Anger resurs gruppen som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="d4d86-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d4d86-135">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="d4d86-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d4d86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d86-136">CommonParameters</span></span>
<span data-ttu-id="d4d86-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d86-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d86-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d86-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4d86-139">INPUTS</span></span>

### <span data-ttu-id="d4d86-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d86-140">System.String</span></span>

## <span data-ttu-id="d4d86-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4d86-141">OUTPUTS</span></span>

### <span data-ttu-id="d4d86-142">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d4d86-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d4d86-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4d86-143">NOTES</span></span>

## <span data-ttu-id="d4d86-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4d86-144">RELATED LINKS</span></span>

[<span data-ttu-id="d4d86-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d4d86-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d4d86-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d4d86-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d4d86-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d4d86-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d4d86-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d4d86-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


