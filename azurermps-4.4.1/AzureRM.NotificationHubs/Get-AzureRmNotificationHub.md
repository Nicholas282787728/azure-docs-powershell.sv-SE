---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: 2bb7d6f6addbbbf91f7f9f93e7e30de9cb3ece81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585484"
---
# <span data-ttu-id="3edbd-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edbd-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="3edbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3edbd-102">SYNOPSIS</span></span>
<span data-ttu-id="3edbd-103">Hämtar information om dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="3edbd-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3edbd-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3edbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3edbd-105">DESCRIPTION</span></span>
<span data-ttu-id="3edbd-106">Cmdleten **Get-AzureRmNotificationHub** hämtar information om meddelande nav i ett angivet namn område och tilldelats till en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3edbd-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="3edbd-107">Du kan till exempel få information om alla meddelande nav i namn området ContosoNamespace och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3edbd-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="3edbd-108">Alternativt kan du använda parametern *NotificationHub* för att begränsa vilka data som returneras till information om ett specifikt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="3edbd-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="3edbd-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform, till exempel iOS, Android, Windows Phone 8 och Windows Store, som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="3edbd-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="3edbd-110">Dessa NAV är ungefär likvärdiga med enskilda appar och alla dina program har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="3edbd-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="3edbd-111">Denna cmdlet får bara information om själva navet.</span><span class="sxs-lookup"><span data-stu-id="3edbd-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="3edbd-112">Andra cmdlets, till exempel get-AzureRmNotificationHubAuthorizationRules, get-AzureRmNotificationHubListKeys och get-AzureRmNotificationHubPNSCredentials behövs för att få information om ett NAVs auktoriseringsregler, anslutnings strängar och autentiseringsuppgifter för Platform Notification-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3edbd-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="3edbd-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3edbd-113">EXAMPLES</span></span>

### <span data-ttu-id="3edbd-114">Exempel 1: Hämta information för alla aviserings nav i ett angivet namn område</span><span class="sxs-lookup"><span data-stu-id="3edbd-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="3edbd-115">Med det här kommandot får du information för alla aviserings nav i namn området med namnet ContosoNamespace som har tilldelats till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3edbd-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="3edbd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3edbd-116">PARAMETERS</span></span>

### <span data-ttu-id="3edbd-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3edbd-117">-Namespace</span></span>
<span data-ttu-id="3edbd-118">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="3edbd-118">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="3edbd-119">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="3edbd-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3edbd-120">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edbd-120">-NotificationHub</span></span>
<span data-ttu-id="3edbd-121">Anger namnet på meddelande navet som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3edbd-121">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="3edbd-122">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="3edbd-122">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3edbd-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3edbd-123">-ResourceGroup</span></span>
<span data-ttu-id="3edbd-124">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="3edbd-124">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="3edbd-125">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="3edbd-125">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3edbd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edbd-126">-DefaultProfile</span></span>
<span data-ttu-id="3edbd-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3edbd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3edbd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edbd-128">CommonParameters</span></span>
<span data-ttu-id="3edbd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edbd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edbd-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3edbd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edbd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3edbd-131">INPUTS</span></span>

## <span data-ttu-id="3edbd-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3edbd-132">OUTPUTS</span></span>

### <span data-ttu-id="3edbd-133">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="3edbd-133">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="3edbd-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3edbd-134">NOTES</span></span>

## <span data-ttu-id="3edbd-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3edbd-135">RELATED LINKS</span></span>

[<span data-ttu-id="3edbd-136">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3edbd-136">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="3edbd-137">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="3edbd-137">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="3edbd-138">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="3edbd-138">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="3edbd-139">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edbd-139">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="3edbd-140">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edbd-140">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="3edbd-141">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3edbd-141">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


