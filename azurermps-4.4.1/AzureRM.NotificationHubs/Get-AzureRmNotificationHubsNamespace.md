---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575947"
---
# <span data-ttu-id="30ad1-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="30ad1-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="30ad1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="30ad1-103">Hämtar information om ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="30ad1-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30ad1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30ad1-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ad1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="30ad1-106">Cmdleten **Get-AzureRmNotificationHubsNamespace** hämtar information om namn rymder för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="30ad1-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="30ad1-107">Med den här cmdleten kan du hämta information för alla dina namn områden, information om de namn områden som har tilldelats till en viss resurs grupp; eller för att returnera information om ett specifikt namn område.</span><span class="sxs-lookup"><span data-stu-id="30ad1-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="30ad1-108">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="30ad1-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="30ad1-109">Du måste ha minst en namnrymd för aviserings navet: alla aviserings NAV måste kopplas till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="30ad1-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="30ad1-110">Ett enda namn område kan House flera nav, vilket innebär att du kanske bara behöver ett namn område i organisationen.</span><span class="sxs-lookup"><span data-stu-id="30ad1-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="30ad1-111">Men du kan också ha flera namn områden för att bättre organisera dina nav, eller ge specifika enskilda personer tillstånd att hantera en viss delmängd av NAV.</span><span class="sxs-lookup"><span data-stu-id="30ad1-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="30ad1-112">Cmdleten **Get-AzureRmNotificationHubsNamespace** returnerar grundläggande information om själva namn området.</span><span class="sxs-lookup"><span data-stu-id="30ad1-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="30ad1-113">Om du vill ha information om de auktoriseringsregler som är associerade med ett namn område använder du get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="30ad1-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="30ad1-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30ad1-114">EXAMPLES</span></span>

### <span data-ttu-id="30ad1-115">Exempel 1: Hämta information för alla namn områden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="30ad1-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="30ad1-116">Det här kommandot returnerar information för alla dina namn områden i meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="30ad1-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="30ad1-117">Exempel 2: Hämta information om ett namn område för en enskild avisering</span><span class="sxs-lookup"><span data-stu-id="30ad1-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="30ad1-118">Det här kommandot får information om ett namn område för en enskild aviserings hubb: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="30ad1-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="30ad1-119">Exempel 3: Hämta information om alla aviserings nav som har tilldelats till ett visst namn område</span><span class="sxs-lookup"><span data-stu-id="30ad1-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="30ad1-120">Med det här kommandot får du information för alla namn rymder för aviseringar som tilldelats resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="30ad1-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="30ad1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30ad1-121">PARAMETERS</span></span>

### <span data-ttu-id="30ad1-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="30ad1-122">-Namespace</span></span>
<span data-ttu-id="30ad1-123">Anger ett unikt namn för namn området.</span><span class="sxs-lookup"><span data-stu-id="30ad1-123">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="30ad1-124">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="30ad1-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ad1-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30ad1-125">-ResourceGroup</span></span>
<span data-ttu-id="30ad1-126">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="30ad1-126">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="30ad1-127">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="30ad1-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ad1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ad1-128">-DefaultProfile</span></span>
<span data-ttu-id="30ad1-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30ad1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30ad1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ad1-130">CommonParameters</span></span>
<span data-ttu-id="30ad1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ad1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ad1-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ad1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ad1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30ad1-133">INPUTS</span></span>

## <span data-ttu-id="30ad1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30ad1-134">OUTPUTS</span></span>

### <span data-ttu-id="30ad1-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="30ad1-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="30ad1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30ad1-136">NOTES</span></span>

## <span data-ttu-id="30ad1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30ad1-137">RELATED LINKS</span></span>

[<span data-ttu-id="30ad1-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="30ad1-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="30ad1-139">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="30ad1-139">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="30ad1-140">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="30ad1-140">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="30ad1-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="30ad1-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


