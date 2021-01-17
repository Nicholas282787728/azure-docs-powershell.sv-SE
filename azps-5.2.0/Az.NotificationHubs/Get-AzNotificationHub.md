---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395328"
---
# <span data-ttu-id="0d976-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0d976-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="0d976-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d976-102">SYNOPSIS</span></span>
<span data-ttu-id="0d976-103">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="0d976-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="0d976-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d976-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d976-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d976-105">DESCRIPTION</span></span>
<span data-ttu-id="0d976-106">Cmdleten **Get-AzNotificationHub** hämtar information om meddelande nav i ett angivet namn område och tilldelats till en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0d976-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="0d976-107">Du kan till exempel få information om alla meddelande nav i namn området ContosoNamespace och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0d976-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="0d976-108">Alternativt kan du använda parametern *NotificationHub* för att begränsa vilka data som returneras till information om ett specifikt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="0d976-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="0d976-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform, till exempel iOS, Android, Windows Phone 8 och Windows Store, som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="0d976-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="0d976-110">Dessa NAV är ungefär likvärdiga med enskilda appar och alla dina program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="0d976-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="0d976-111">Denna cmdlet får bara information om själva navet.</span><span class="sxs-lookup"><span data-stu-id="0d976-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="0d976-112">Andra cmdlets, till exempel get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys och get-AzNotificationHubPNSCredentials behövs för att få information om ett NAVs auktoriseringsregler, anslutnings strängar och autentiseringsuppgifter för Platform Notification-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0d976-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="0d976-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d976-113">EXAMPLES</span></span>

### <span data-ttu-id="0d976-114">Exempel 1: Hämta information för alla aviserings nav i ett angivet namn område</span><span class="sxs-lookup"><span data-stu-id="0d976-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="0d976-115">Med det här kommandot får du information för alla aviserings nav i namn området med namnet ContosoNamespace som har tilldelats till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0d976-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="0d976-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0d976-116">Example 2</span></span>

<span data-ttu-id="0d976-117">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="0d976-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="0d976-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="0d976-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="0d976-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d976-119">PARAMETERS</span></span>

### <span data-ttu-id="0d976-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d976-120">-DefaultProfile</span></span>
<span data-ttu-id="0d976-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0d976-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d976-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="0d976-122">-Namespace</span></span>
<span data-ttu-id="0d976-123">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0d976-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="0d976-124">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="0d976-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0d976-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0d976-125">-NotificationHub</span></span>
<span data-ttu-id="0d976-126">Anger namnet på meddelande navet som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="0d976-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="0d976-127">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="0d976-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="0d976-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0d976-128">-ResourceGroup</span></span>
<span data-ttu-id="0d976-129">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0d976-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="0d976-130">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="0d976-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0d976-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d976-131">CommonParameters</span></span>
<span data-ttu-id="0d976-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d976-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d976-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d976-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d976-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d976-134">INPUTS</span></span>

### <span data-ttu-id="0d976-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0d976-135">System.String</span></span>

## <span data-ttu-id="0d976-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d976-136">OUTPUTS</span></span>

### <span data-ttu-id="0d976-137">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="0d976-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="0d976-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d976-138">NOTES</span></span>

## <span data-ttu-id="0d976-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d976-139">RELATED LINKS</span></span>

[<span data-ttu-id="0d976-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0d976-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="0d976-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="0d976-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="0d976-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="0d976-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="0d976-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0d976-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="0d976-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0d976-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="0d976-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0d976-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


