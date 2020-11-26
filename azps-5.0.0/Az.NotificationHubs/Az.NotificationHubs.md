---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325109"
---
# <span data-ttu-id="e6e0a-101">Modulen AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e6e0a-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="e6e0a-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="e6e0a-102">Description</span></span>
<span data-ttu-id="e6e0a-103">I det här avsnittet visas hjälp avsnitt för Azure Notification Hub-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="e6e0a-104">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform (iOS, Android, Windows Phone 8, Windows Store, etc.) som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="e6e0a-105">Dessa NAV är ungefär likvärdiga med enskilda appar: varje program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="e6e0a-106">Meddelande NAV är organiserade i logiska containrar som kallas namn områden och auktoriseringsregler (säkerhets associationer för delad åtkomst) används för att hantera åtkomst till nav och namn områden.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="e6e0a-107">Alla de här elementen kan administreras med cmdlets på Notification-navet.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="e6e0a-108">AZ. NotificationHubs-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e6e0a-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="e6e0a-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e6e0a-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="e6e0a-110">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="e6e0a-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="e6e0a-112">Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="e6e0a-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="e6e0a-114">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="e6e0a-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="e6e0a-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="e6e0a-116">Hämtar PNS-autentiseringsuppgifter för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e6e0a-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="e6e0a-118">Hämtar information om ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="e6e0a-120">Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="e6e0a-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="e6e0a-122">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="e6e0a-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e6e0a-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="e6e0a-124">Skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="e6e0a-126">Skapar en auktoriseringsregel och tilldelar regeln ett huvud meddelande.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="e6e0a-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="e6e0a-128">Återskapa nyckeln för en NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="e6e0a-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e6e0a-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="e6e0a-130">Skapar ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="e6e0a-132">Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e6e0a-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="e6e0a-134">Återskapa nyckeln för en auktoriseringsregel för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="e6e0a-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e6e0a-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="e6e0a-136">Tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="e6e0a-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="e6e0a-138">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e6e0a-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="e6e0a-140">Tar bort ett namn område för en avisering.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="e6e0a-142">Tar bort en auktoriseringsregel från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e6e0a-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="e6e0a-144">Ställer in egenskaps värden för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="e6e0a-146">Anger auktoriseringsregler för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="e6e0a-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e6e0a-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="e6e0a-148">Anger egenskaps värden för ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="e6e0a-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e6e0a-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="e6e0a-150">Anger auktoriseringsregler för ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="e6e0a-150">Sets authorization rules for a notification hub namespace.</span></span>
