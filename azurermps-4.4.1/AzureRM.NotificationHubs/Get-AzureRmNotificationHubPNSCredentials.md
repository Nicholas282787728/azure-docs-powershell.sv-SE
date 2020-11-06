---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575948"
---
# <span data-ttu-id="8ce5e-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="8ce5e-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="8ce5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ce5e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce5e-103">Hämtar PNS-autentiseringsuppgifter för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ce5e-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ce5e-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce5e-106">Cmdleten **Get-AzureRmNotificationHubPNSCredentials** hämtar PNS-autentiseringsuppgifterna (Platform Notification Service) för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="8ce5e-107">Varje meddelande nav har en uppsättning PNS-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="8ce5e-108">Dessa autentiseringsuppgifter tillämpas på enskilda Push Notification-tjänster, till exempel, men inte begränsat till; tjänsten iOS Push Notification, tjänsten Android Push Notification och Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="8ce5e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ce5e-109">EXAMPLES</span></span>

### <span data-ttu-id="8ce5e-110">Exempel 1: Hämta PNS-autentiseringsuppgifter för ett specifikt meddelande nav</span><span class="sxs-lookup"><span data-stu-id="8ce5e-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8ce5e-111">Det här kommandot får PNS-autentiseringsuppgifter för aviserings navet med namnet ContosoInternalHub som tillhör resurs gruppen med namnet ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="8ce5e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ce5e-112">PARAMETERS</span></span>

### <span data-ttu-id="8ce5e-113">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8ce5e-113">-Namespace</span></span>
<span data-ttu-id="8ce5e-114">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-114">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="8ce5e-115">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-115">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8ce5e-116">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8ce5e-116">-NotificationHub</span></span>
<span data-ttu-id="8ce5e-117">Anger meddelandets Hub som PNS-autentiseringsuppgifterna är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-117">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="8ce5e-118">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-118">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8ce5e-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ce5e-119">-ResourceGroup</span></span>
<span data-ttu-id="8ce5e-120">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-120">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="8ce5e-121">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8ce5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce5e-122">-DefaultProfile</span></span>
<span data-ttu-id="8ce5e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce5e-124">CommonParameters</span></span>
<span data-ttu-id="8ce5e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce5e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce5e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce5e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ce5e-127">INPUTS</span></span>

## <span data-ttu-id="8ce5e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ce5e-128">OUTPUTS</span></span>

### <span data-ttu-id="8ce5e-129">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8ce5e-129">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8ce5e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ce5e-130">NOTES</span></span>

## <span data-ttu-id="8ce5e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ce5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ce5e-132">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8ce5e-132">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


