---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: caab088ab796401cc9718da82118e3004d49ce45
ms.sourcegitcommit: d656467e32643b7bc9523e89a1360d92a171ff13
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/25/2019
ms.locfileid: "93571224"
---
# <span data-ttu-id="478d4-101">Modulen AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="478d4-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="478d4-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="478d4-102">Description</span></span>
<span data-ttu-id="478d4-103">I det här avsnittet visas hjälp avsnitt för Azure Notification Hub-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="478d4-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="478d4-104">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform (iOS, Android, Windows Phone 8, Windows Store, etc.) som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="478d4-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="478d4-105">Dessa NAV är ungefär likvärdiga med enskilda appar: varje program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="478d4-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="478d4-106">Meddelande NAV är organiserade i logiska containrar som kallas namn områden och auktoriseringsregler (säkerhets associationer för delad åtkomst) används för att hantera åtkomst till nav och namn områden.</span><span class="sxs-lookup"><span data-stu-id="478d4-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="478d4-107">Alla de här elementen kan administreras med cmdlets på Notification-navet.</span><span class="sxs-lookup"><span data-stu-id="478d4-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="478d4-108">AzureRM. NotificationHubs-cmdletar</span><span class="sxs-lookup"><span data-stu-id="478d4-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="478d4-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="478d4-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="478d4-110">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="478d4-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="478d4-112">Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="478d4-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="478d4-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="478d4-114">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="478d4-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="478d4-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="478d4-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="478d4-116">Hämtar PNS-autentiseringsuppgifter för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="478d4-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="478d4-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="478d4-118">Hämtar information om ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="478d4-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="478d4-120">Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="478d4-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="478d4-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="478d4-122">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="478d4-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="478d4-123">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="478d4-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="478d4-124">Skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="478d4-125">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="478d4-126">Skapar en auktoriseringsregel och tilldelar regeln ett huvud meddelande.</span><span class="sxs-lookup"><span data-stu-id="478d4-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="478d4-127">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="478d4-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="478d4-128">Återskapa nyckeln för en NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="478d4-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="478d4-129">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="478d4-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="478d4-130">Skapar ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="478d4-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="478d4-132">Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="478d4-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-133">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="478d4-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="478d4-134">Återskapa nyckeln för en auktoriseringsregel för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="478d4-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="478d4-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="478d4-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="478d4-136">Tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="478d4-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="478d4-138">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="478d4-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="478d4-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="478d4-140">Tar bort ett namn område för en avisering.</span><span class="sxs-lookup"><span data-stu-id="478d4-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="478d4-142">Tar bort en auktoriseringsregel från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="478d4-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="478d4-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="478d4-144">Ställer in egenskaps värden för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="478d4-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="478d4-146">Anger auktoriseringsregler för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="478d4-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="478d4-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="478d4-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="478d4-148">Anger egenskaps värden för ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="478d4-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="478d4-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="478d4-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="478d4-150">Anger auktoriseringsregler för ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="478d4-150">Sets authorization rules for a notification hub namespace.</span></span>

