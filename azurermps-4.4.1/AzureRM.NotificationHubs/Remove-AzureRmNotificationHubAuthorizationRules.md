---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: bb92344616c79db26b37bd9b18bdff7973946c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575942"
---
# <span data-ttu-id="06eb7-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="06eb7-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="06eb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="06eb7-103">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="06eb7-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06eb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06eb7-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06eb7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="06eb7-106">Cmdleten **Remove-AzureRmNotificationHubAuthorizationRules** tar bort en auktoriseringsregel för delade Access-signaturer från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="06eb7-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="06eb7-107">Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="06eb7-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="06eb7-108">Behörighets nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="06eb7-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="06eb7-109">Lyssna</span><span class="sxs-lookup"><span data-stu-id="06eb7-109">Listen</span></span>
- <span data-ttu-id="06eb7-110">Bifoga</span><span class="sxs-lookup"><span data-stu-id="06eb7-110">Send</span></span>
- <span data-ttu-id="06eb7-111">Inställningar</span><span class="sxs-lookup"><span data-stu-id="06eb7-111">Manage</span></span>

<span data-ttu-id="06eb7-112">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="06eb7-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="06eb7-113">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="06eb7-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="06eb7-114">Om du tar bort en auktoriseringsregel raderas också motsvarande användar behörighet.</span><span class="sxs-lookup"><span data-stu-id="06eb7-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="06eb7-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06eb7-115">EXAMPLES</span></span>

### <span data-ttu-id="06eb7-116">Exempel 1: ta bort en auktoriseringsregel från ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="06eb7-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="06eb7-117">Det här kommandot tar bort auktoriseringsregeln med namnet ListenRule från meddelande navet ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="06eb7-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="06eb7-118">När du kör det här kommandot måste du ange både namn området och resurs gruppen som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="06eb7-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="06eb7-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06eb7-119">PARAMETERS</span></span>

### <span data-ttu-id="06eb7-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="06eb7-120">-AuthorizationRule</span></span>
<span data-ttu-id="06eb7-121">Anger namnet på den SAS-autentiseringsprocess som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="06eb7-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06eb7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="06eb7-122">-Force</span></span>
<span data-ttu-id="06eb7-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="06eb7-123">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06eb7-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="06eb7-124">-Namespace</span></span>
<span data-ttu-id="06eb7-125">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="06eb7-125">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="06eb7-126">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="06eb7-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="06eb7-127">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="06eb7-127">-NotificationHub</span></span>
<span data-ttu-id="06eb7-128">Anger meddelandets Hub som auktoriseringsregler är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="06eb7-128">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="06eb7-129">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform.</span><span class="sxs-lookup"><span data-stu-id="06eb7-129">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="06eb7-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06eb7-130">-ResourceGroup</span></span>
<span data-ttu-id="06eb7-131">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="06eb7-131">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="06eb7-132">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="06eb7-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="06eb7-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06eb7-133">-Confirm</span></span>
<span data-ttu-id="06eb7-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06eb7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06eb7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06eb7-135">-WhatIf</span></span>
<span data-ttu-id="06eb7-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06eb7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06eb7-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06eb7-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06eb7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06eb7-138">-DefaultProfile</span></span>
<span data-ttu-id="06eb7-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06eb7-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06eb7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06eb7-140">CommonParameters</span></span>
<span data-ttu-id="06eb7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06eb7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06eb7-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06eb7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06eb7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06eb7-143">INPUTS</span></span>

## <span data-ttu-id="06eb7-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06eb7-144">OUTPUTS</span></span>

## <span data-ttu-id="06eb7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06eb7-145">NOTES</span></span>

## <span data-ttu-id="06eb7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06eb7-146">RELATED LINKS</span></span>

[<span data-ttu-id="06eb7-147">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="06eb7-147">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="06eb7-148">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="06eb7-148">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="06eb7-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="06eb7-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


