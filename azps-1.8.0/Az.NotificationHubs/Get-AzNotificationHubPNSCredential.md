---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 440eb112ea49465863b53f705c6b90a8b2e4be74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747633"
---
# <span data-ttu-id="d2ddf-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="d2ddf-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="d2ddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ddf-103">Hämtar PNS-autentiseringsuppgifter för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="d2ddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2ddf-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ddf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ddf-106">Cmdleten **Get-AzNotificationHubPNSCredential** hämtar PNS-autentiseringsuppgifterna (Platform Notification Service) för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="d2ddf-107">Varje meddelande nav har en uppsättning PNS-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="d2ddf-108">Dessa autentiseringsuppgifter tillämpas på enskilda Push Notification-tjänster, till exempel, men inte begränsat till; tjänsten iOS Push Notification, tjänsten Android Push Notification och Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="d2ddf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2ddf-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ddf-110">Exempel 1: Hämta PNS-autentiseringsuppgifter för ett specifikt meddelande nav</span><span class="sxs-lookup"><span data-stu-id="d2ddf-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="d2ddf-111">Det här kommandot får PNS-autentiseringsuppgifter för aviserings navet med namnet ContosoInternalHub som tillhör resurs gruppen med namnet ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="d2ddf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2ddf-112">PARAMETERS</span></span>

### <span data-ttu-id="d2ddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ddf-113">-DefaultProfile</span></span>
<span data-ttu-id="d2ddf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d2ddf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ddf-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d2ddf-115">-Namespace</span></span>
<span data-ttu-id="d2ddf-116">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d2ddf-117">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d2ddf-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d2ddf-118">-NotificationHub</span></span>
<span data-ttu-id="d2ddf-119">Anger meddelandets Hub som PNS-autentiseringsuppgifterna är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="d2ddf-120">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="d2ddf-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d2ddf-121">-ResourceGroup</span></span>
<span data-ttu-id="d2ddf-122">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="d2ddf-123">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d2ddf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ddf-124">CommonParameters</span></span>
<span data-ttu-id="d2ddf-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ddf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ddf-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ddf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ddf-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2ddf-127">INPUTS</span></span>

### <span data-ttu-id="d2ddf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ddf-128">System.String</span></span>

## <span data-ttu-id="d2ddf-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2ddf-129">OUTPUTS</span></span>

### <span data-ttu-id="d2ddf-130">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d2ddf-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="d2ddf-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2ddf-131">NOTES</span></span>

## <span data-ttu-id="d2ddf-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2ddf-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2ddf-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d2ddf-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

