---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 996904a68e8cb55aa4964a6c776064722c63dbab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577118"
---
# <span data-ttu-id="54dbb-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="54dbb-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="54dbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="54dbb-103">Hämtar information om ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="54dbb-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54dbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54dbb-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54dbb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="54dbb-106">Cmdleten **Get-AzureRmNotificationHubsNamespace** hämtar information om namn rymder för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="54dbb-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="54dbb-107">Med den här cmdleten kan du hämta information för alla dina namn områden, information om de namn områden som har tilldelats till en viss resurs grupp; eller för att returnera information om ett specifikt namn område.</span><span class="sxs-lookup"><span data-stu-id="54dbb-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="54dbb-108">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="54dbb-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="54dbb-109">Du måste ha minst en namnrymd för aviserings navet: alla aviserings NAV måste kopplas till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="54dbb-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="54dbb-110">Ett enda namn område kan House flera nav, vilket innebär att du kanske bara behöver ett namn område i organisationen.</span><span class="sxs-lookup"><span data-stu-id="54dbb-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="54dbb-111">Men du kan också ha flera namn områden för att bättre organisera dina nav, eller ge specifika enskilda personer tillstånd att hantera en viss delmängd av NAV.</span><span class="sxs-lookup"><span data-stu-id="54dbb-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="54dbb-112">Cmdleten **Get-AzureRmNotificationHubsNamespace** returnerar grundläggande information om själva namn området.</span><span class="sxs-lookup"><span data-stu-id="54dbb-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="54dbb-113">Om du vill ha information om de auktoriseringsregler som är associerade med ett namn område använder du get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="54dbb-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="54dbb-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54dbb-114">EXAMPLES</span></span>

### <span data-ttu-id="54dbb-115">Exempel 1: Hämta information för alla namn områden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="54dbb-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="54dbb-116">Det här kommandot returnerar information för alla dina namn områden i meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="54dbb-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="54dbb-117">Exempel 2: Hämta information om ett namn område för en enskild avisering</span><span class="sxs-lookup"><span data-stu-id="54dbb-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="54dbb-118">Det här kommandot får information om ett namn område för en enskild aviserings hubb: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="54dbb-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="54dbb-119">Exempel 3: Hämta information om alla aviserings nav som har tilldelats till ett visst namn område</span><span class="sxs-lookup"><span data-stu-id="54dbb-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="54dbb-120">Med det här kommandot får du information för alla namn rymder för aviseringar som tilldelats resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="54dbb-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="54dbb-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54dbb-121">PARAMETERS</span></span>

### <span data-ttu-id="54dbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54dbb-122">-DefaultProfile</span></span>
<span data-ttu-id="54dbb-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54dbb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54dbb-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="54dbb-124">-Namespace</span></span>
<span data-ttu-id="54dbb-125">Anger ett unikt namn för namn området.</span><span class="sxs-lookup"><span data-stu-id="54dbb-125">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="54dbb-126">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="54dbb-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54dbb-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54dbb-127">-ResourceGroup</span></span>
<span data-ttu-id="54dbb-128">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="54dbb-128">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="54dbb-129">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="54dbb-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54dbb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54dbb-130">CommonParameters</span></span>
<span data-ttu-id="54dbb-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54dbb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54dbb-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54dbb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54dbb-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54dbb-133">INPUTS</span></span>

### <span data-ttu-id="54dbb-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="54dbb-134">None</span></span>
<span data-ttu-id="54dbb-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="54dbb-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54dbb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54dbb-136">OUTPUTS</span></span>

### <span data-ttu-id="54dbb-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="54dbb-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="54dbb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54dbb-138">NOTES</span></span>

## <span data-ttu-id="54dbb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54dbb-139">RELATED LINKS</span></span>

[<span data-ttu-id="54dbb-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="54dbb-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="54dbb-141">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="54dbb-141">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="54dbb-142">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="54dbb-142">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="54dbb-143">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="54dbb-143">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


