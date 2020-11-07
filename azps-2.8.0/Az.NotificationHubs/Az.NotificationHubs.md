---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93743306"
---
# <span data-ttu-id="072ee-101">Modulen AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="072ee-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="072ee-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="072ee-102">Description</span></span>
<span data-ttu-id="072ee-103">I det här avsnittet visas hjälp avsnitt för Azure Notification Hub-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="072ee-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="072ee-104">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform (iOS, Android, Windows Phone 8, Windows Store, etc.) som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="072ee-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="072ee-105">Dessa NAV är ungefär likvärdiga med enskilda appar: varje program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="072ee-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="072ee-106">Meddelande NAV är organiserade i logiska containrar som kallas namn områden och auktoriseringsregler (säkerhets associationer för delad åtkomst) används för att hantera åtkomst till nav och namn områden.</span><span class="sxs-lookup"><span data-stu-id="072ee-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="072ee-107">Alla de här elementen kan administreras med cmdlets på Notification-navet.</span><span class="sxs-lookup"><span data-stu-id="072ee-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="072ee-108">AZ. NotificationHubs-cmdletar</span><span class="sxs-lookup"><span data-stu-id="072ee-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="072ee-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="072ee-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="072ee-110">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="072ee-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="072ee-112">Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="072ee-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="072ee-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="072ee-114">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="072ee-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="072ee-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="072ee-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="072ee-116">Hämtar PNS-autentiseringsuppgifter för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="072ee-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="072ee-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="072ee-118">Hämtar information om ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="072ee-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="072ee-120">Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="072ee-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="072ee-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="072ee-122">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="072ee-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="072ee-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="072ee-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="072ee-124">Skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="072ee-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="072ee-126">Skapar en auktoriseringsregel och tilldelar regeln ett huvud meddelande.</span><span class="sxs-lookup"><span data-stu-id="072ee-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="072ee-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="072ee-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="072ee-128">Återskapa nyckeln för en NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="072ee-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="072ee-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="072ee-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="072ee-130">Skapar ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="072ee-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="072ee-132">Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="072ee-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="072ee-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="072ee-134">Återskapa nyckeln för en auktoriseringsregel för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="072ee-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="072ee-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="072ee-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="072ee-136">Tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="072ee-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="072ee-138">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="072ee-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="072ee-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="072ee-140">Tar bort ett namn område för en avisering.</span><span class="sxs-lookup"><span data-stu-id="072ee-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="072ee-142">Tar bort en auktoriseringsregel från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="072ee-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="072ee-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="072ee-144">Ställer in egenskaps värden för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="072ee-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="072ee-146">Anger auktoriseringsregler för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="072ee-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="072ee-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="072ee-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="072ee-148">Anger egenskaps värden för ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="072ee-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="072ee-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="072ee-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="072ee-150">Anger auktoriseringsregler för ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="072ee-150">Sets authorization rules for a notification hub namespace.</span></span>

