---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586016"
---
# <span data-ttu-id="66fe5-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="66fe5-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="66fe5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="66fe5-103">Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="66fe5-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fe5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66fe5-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66fe5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="66fe5-106">Cmdleten **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** returnerar information om behörighets reglerna för de delade Access-signaturerna (säkerhets associationer) som är associerade med ett namn område.</span><span class="sxs-lookup"><span data-stu-id="66fe5-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="66fe5-107">Du kan returnera information om alla regler som är kopplade till namn området.</span><span class="sxs-lookup"><span data-stu-id="66fe5-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="66fe5-108">Du kan också returnera information för en viss regel genom att ta med parametern *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="66fe5-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="66fe5-109">Auktoriseringsregler hanterar åtkomst till namn utrymmen.</span><span class="sxs-lookup"><span data-stu-id="66fe5-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="66fe5-110">Detta görs genom att länkar skapas som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="66fe5-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="66fe5-111">Plattforms nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="66fe5-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="66fe5-112">Lyssna</span><span class="sxs-lookup"><span data-stu-id="66fe5-112">Listen</span></span>
- <span data-ttu-id="66fe5-113">Bifoga</span><span class="sxs-lookup"><span data-stu-id="66fe5-113">Send</span></span>
- <span data-ttu-id="66fe5-114">Inställningar</span><span class="sxs-lookup"><span data-stu-id="66fe5-114">Manage</span></span>

<span data-ttu-id="66fe5-115">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="66fe5-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="66fe5-116">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="66fe5-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="66fe5-117">Denna cmdlet får bara auktoriseringsregler som är associerade med ett namn område.</span><span class="sxs-lookup"><span data-stu-id="66fe5-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="66fe5-118">Använd Get-AzureRmNotificationHubsNamespace för att få information om själva namn området.</span><span class="sxs-lookup"><span data-stu-id="66fe5-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="66fe5-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66fe5-119">EXAMPLES</span></span>

### <span data-ttu-id="66fe5-120">Exempel 1: få information om alla auktoriseringsregler som tilldelats till namn områden</span><span class="sxs-lookup"><span data-stu-id="66fe5-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="66fe5-121">Med det här kommandot får du information om alla auktoriseringsregler som tilldelats både namn områdets ContosoNamespace och ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="66fe5-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="66fe5-122">Exempel 2: Hämta information om en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="66fe5-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="66fe5-123">Det här kommandot får information om en enda auktoriseringsregel med namnet ListenRule.</span><span class="sxs-lookup"><span data-stu-id="66fe5-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="66fe5-124">Du måste inkludera namn området och resurs gruppen när du får information för en specifik auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="66fe5-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="66fe5-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66fe5-125">PARAMETERS</span></span>

### <span data-ttu-id="66fe5-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="66fe5-126">-AuthorizationRule</span></span>
<span data-ttu-id="66fe5-127">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="66fe5-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="66fe5-128">Dessa regler bestämmer vilken typ av åtkomst användare har till namn området.</span><span class="sxs-lookup"><span data-stu-id="66fe5-128">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fe5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fe5-129">-DefaultProfile</span></span>
<span data-ttu-id="66fe5-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66fe5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66fe5-131">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="66fe5-131">-Namespace</span></span>
<span data-ttu-id="66fe5-132">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="66fe5-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="66fe5-133">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="66fe5-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fe5-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66fe5-134">-ResourceGroup</span></span>
<span data-ttu-id="66fe5-135">Anger resurs gruppen som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="66fe5-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="66fe5-136">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="66fe5-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fe5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fe5-137">CommonParameters</span></span>
<span data-ttu-id="66fe5-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fe5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fe5-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fe5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fe5-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66fe5-140">INPUTS</span></span>

### <span data-ttu-id="66fe5-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="66fe5-141">None</span></span>
<span data-ttu-id="66fe5-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="66fe5-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66fe5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66fe5-143">OUTPUTS</span></span>

### <span data-ttu-id="66fe5-144">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="66fe5-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="66fe5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66fe5-145">NOTES</span></span>

## <span data-ttu-id="66fe5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66fe5-146">RELATED LINKS</span></span>

[<span data-ttu-id="66fe5-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="66fe5-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="66fe5-148">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="66fe5-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="66fe5-149">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="66fe5-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="66fe5-150">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="66fe5-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


