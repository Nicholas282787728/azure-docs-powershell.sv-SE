---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 9ae94e039d91f8f21015fb28b726ef5bacfb4ae4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575592"
---
# <span data-ttu-id="9fd57-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9fd57-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="9fd57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fd57-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd57-103">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="9fd57-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fd57-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fd57-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd57-106">Cmdleten **Remove-AzureRmNotificationHubAuthorizationRules** tar bort en auktoriseringsregel för delade Access-signaturer från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="9fd57-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="9fd57-107">Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="9fd57-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="9fd57-108">Behörighets nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="9fd57-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="9fd57-109">Lyssna</span><span class="sxs-lookup"><span data-stu-id="9fd57-109">Listen</span></span>
- <span data-ttu-id="9fd57-110">Bifoga</span><span class="sxs-lookup"><span data-stu-id="9fd57-110">Send</span></span>
- <span data-ttu-id="9fd57-111">Inställningar</span><span class="sxs-lookup"><span data-stu-id="9fd57-111">Manage</span></span>

<span data-ttu-id="9fd57-112">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="9fd57-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9fd57-113">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="9fd57-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="9fd57-114">Om du tar bort en auktoriseringsregel raderas också motsvarande användar behörighet.</span><span class="sxs-lookup"><span data-stu-id="9fd57-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="9fd57-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fd57-115">EXAMPLES</span></span>

### <span data-ttu-id="9fd57-116">Exempel 1: ta bort en auktoriseringsregel från ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="9fd57-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9fd57-117">Det här kommandot tar bort auktoriseringsregeln med namnet ListenRule från meddelande navet ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="9fd57-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="9fd57-118">När du kör det här kommandot måste du ange både namn området och resurs gruppen som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9fd57-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="9fd57-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fd57-119">PARAMETERS</span></span>

### <span data-ttu-id="9fd57-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9fd57-120">-AuthorizationRule</span></span>
<span data-ttu-id="9fd57-121">Anger namnet på den SAS-autentiseringsprocess som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9fd57-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd57-122">-DefaultProfile</span></span>
<span data-ttu-id="9fd57-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9fd57-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fd57-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9fd57-124">-Force</span></span>
<span data-ttu-id="9fd57-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9fd57-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9fd57-126">-Namespace</span></span>
<span data-ttu-id="9fd57-127">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9fd57-127">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9fd57-128">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="9fd57-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-129">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9fd57-129">-NotificationHub</span></span>
<span data-ttu-id="9fd57-130">Anger meddelandets Hub som auktoriseringsregler är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="9fd57-130">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="9fd57-131">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform.</span><span class="sxs-lookup"><span data-stu-id="9fd57-131">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9fd57-132">-ResourceGroup</span></span>
<span data-ttu-id="9fd57-133">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9fd57-133">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9fd57-134">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="9fd57-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9fd57-135">-Confirm</span></span>
<span data-ttu-id="9fd57-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9fd57-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd57-137">-WhatIf</span></span>
<span data-ttu-id="9fd57-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9fd57-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fd57-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9fd57-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd57-140">CommonParameters</span></span>
<span data-ttu-id="9fd57-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd57-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd57-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd57-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fd57-143">INPUTS</span></span>

### <span data-ttu-id="9fd57-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="9fd57-144">None</span></span>
<span data-ttu-id="9fd57-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9fd57-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fd57-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fd57-146">OUTPUTS</span></span>

## <span data-ttu-id="9fd57-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fd57-147">NOTES</span></span>

## <span data-ttu-id="9fd57-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fd57-148">RELATED LINKS</span></span>

[<span data-ttu-id="9fd57-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9fd57-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="9fd57-150">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9fd57-150">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="9fd57-151">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9fd57-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


