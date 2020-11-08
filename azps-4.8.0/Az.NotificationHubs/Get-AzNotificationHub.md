---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262033"
---
# <span data-ttu-id="62acc-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="62acc-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="62acc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62acc-102">SYNOPSIS</span></span>
<span data-ttu-id="62acc-103">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="62acc-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="62acc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62acc-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62acc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62acc-105">DESCRIPTION</span></span>
<span data-ttu-id="62acc-106">Cmdleten **Get-AzNotificationHub** hämtar information om meddelande nav i ett angivet namn område och tilldelats till en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62acc-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="62acc-107">Du kan till exempel få information om alla meddelande nav i namn området ContosoNamespace och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="62acc-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="62acc-108">Alternativt kan du använda parametern *NotificationHub* för att begränsa vilka data som returneras till information om ett specifikt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="62acc-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="62acc-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform, till exempel iOS, Android, Windows Phone 8 och Windows Store, som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="62acc-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="62acc-110">Dessa NAV är ungefär likvärdiga med enskilda appar och alla dina program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="62acc-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="62acc-111">Denna cmdlet får bara information om själva navet.</span><span class="sxs-lookup"><span data-stu-id="62acc-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="62acc-112">Andra cmdlets, till exempel get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys och get-AzNotificationHubPNSCredentials behövs för att få information om ett NAVs auktoriseringsregler, anslutnings strängar och autentiseringsuppgifter för Platform Notification-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="62acc-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="62acc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62acc-113">EXAMPLES</span></span>

### <span data-ttu-id="62acc-114">Exempel 1: Hämta information för alla aviserings nav i ett angivet namn område</span><span class="sxs-lookup"><span data-stu-id="62acc-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="62acc-115">Med det här kommandot får du information för alla aviserings nav i namn området med namnet ContosoNamespace som har tilldelats till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="62acc-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="62acc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62acc-116">PARAMETERS</span></span>

### <span data-ttu-id="62acc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62acc-117">-DefaultProfile</span></span>
<span data-ttu-id="62acc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62acc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62acc-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="62acc-119">-Namespace</span></span>
<span data-ttu-id="62acc-120">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="62acc-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="62acc-121">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="62acc-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="62acc-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="62acc-122">-NotificationHub</span></span>
<span data-ttu-id="62acc-123">Anger namnet på meddelande navet som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="62acc-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="62acc-124">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="62acc-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="62acc-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62acc-125">-ResourceGroup</span></span>
<span data-ttu-id="62acc-126">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="62acc-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="62acc-127">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="62acc-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="62acc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62acc-128">CommonParameters</span></span>
<span data-ttu-id="62acc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62acc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62acc-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62acc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62acc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62acc-131">INPUTS</span></span>

### <span data-ttu-id="62acc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62acc-132">System.String</span></span>

## <span data-ttu-id="62acc-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62acc-133">OUTPUTS</span></span>

### <span data-ttu-id="62acc-134">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="62acc-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="62acc-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62acc-135">NOTES</span></span>

## <span data-ttu-id="62acc-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62acc-136">RELATED LINKS</span></span>

[<span data-ttu-id="62acc-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="62acc-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="62acc-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="62acc-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="62acc-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="62acc-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="62acc-140">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="62acc-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="62acc-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="62acc-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="62acc-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="62acc-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


