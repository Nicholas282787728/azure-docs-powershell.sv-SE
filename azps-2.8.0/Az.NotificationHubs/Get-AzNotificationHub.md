---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: f58a34c5fb5a7ca108f2f4f55c9322f1f439fbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919417"
---
# <span data-ttu-id="fd28c-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd28c-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="fd28c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd28c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd28c-103">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="fd28c-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="fd28c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd28c-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd28c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd28c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd28c-106">Cmdleten **Get-AzNotificationHub** hämtar information om meddelande nav i ett angivet namn område och tilldelats till en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fd28c-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="fd28c-107">Du kan till exempel få information om alla meddelande nav i namn området ContosoNamespace och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="fd28c-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="fd28c-108">Alternativt kan du använda parametern *NotificationHub* för att begränsa vilka data som returneras till information om ett specifikt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="fd28c-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="fd28c-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform, till exempel iOS, Android, Windows Phone 8 och Windows Store, som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="fd28c-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="fd28c-110">Dessa NAV är ungefär likvärdiga med enskilda appar och alla dina program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="fd28c-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="fd28c-111">Denna cmdlet får bara information om själva navet.</span><span class="sxs-lookup"><span data-stu-id="fd28c-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="fd28c-112">Andra cmdlets, till exempel get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys och get-AzNotificationHubPNSCredentials behövs för att få information om ett NAVs auktoriseringsregler, anslutnings strängar och autentiseringsuppgifter för Platform Notification-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fd28c-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="fd28c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd28c-113">EXAMPLES</span></span>

### <span data-ttu-id="fd28c-114">Exempel 1: Hämta information för alla aviserings nav i ett angivet namn område</span><span class="sxs-lookup"><span data-stu-id="fd28c-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="fd28c-115">Med det här kommandot får du information för alla aviserings nav i namn området med namnet ContosoNamespace som har tilldelats till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="fd28c-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="fd28c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd28c-116">PARAMETERS</span></span>

### <span data-ttu-id="fd28c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd28c-117">-DefaultProfile</span></span>
<span data-ttu-id="fd28c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd28c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd28c-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fd28c-119">-Namespace</span></span>
<span data-ttu-id="fd28c-120">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="fd28c-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="fd28c-121">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="fd28c-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fd28c-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd28c-122">-NotificationHub</span></span>
<span data-ttu-id="fd28c-123">Anger namnet på meddelande navet som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="fd28c-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="fd28c-124">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="fd28c-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="fd28c-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fd28c-125">-ResourceGroup</span></span>
<span data-ttu-id="fd28c-126">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="fd28c-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="fd28c-127">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="fd28c-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fd28c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd28c-128">CommonParameters</span></span>
<span data-ttu-id="fd28c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd28c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd28c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd28c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd28c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd28c-131">INPUTS</span></span>

### <span data-ttu-id="fd28c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd28c-132">System.String</span></span>

## <span data-ttu-id="fd28c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd28c-133">OUTPUTS</span></span>

### <span data-ttu-id="fd28c-134">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fd28c-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="fd28c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd28c-135">NOTES</span></span>

## <span data-ttu-id="fd28c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd28c-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd28c-137">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd28c-137">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

[<span data-ttu-id="fd28c-138">Get-AzNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="fd28c-138">Get-AzNotificationHubListKeys</span></span>](./Get-AzNotificationHubListKeys.md)

[<span data-ttu-id="fd28c-139">Get-AzNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="fd28c-139">Get-AzNotificationHubPNSCredentials</span></span>](./Get-AzNotificationHubPNSCredentials.md)

[<span data-ttu-id="fd28c-140">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd28c-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="fd28c-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd28c-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="fd28c-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd28c-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

