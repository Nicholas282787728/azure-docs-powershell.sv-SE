---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 6ad682ad80400fa84034b35804c9756775d05eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747611"
---
# <span data-ttu-id="6cf3e-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6cf3e-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="6cf3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cf3e-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf3e-103">Tar bort en auktoriseringsregel från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="6cf3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cf3e-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cf3e-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf3e-106">Cmdleten **Remove-AzNotificationHubAuthorizationRule** tar bort en auktoriseringsregel för delade Access-signaturer från ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="6cf3e-107">Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="6cf3e-108">Behörighets nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="6cf3e-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="6cf3e-109">Lyssna</span><span class="sxs-lookup"><span data-stu-id="6cf3e-109">Listen</span></span>
- <span data-ttu-id="6cf3e-110">Bifoga</span><span class="sxs-lookup"><span data-stu-id="6cf3e-110">Send</span></span>
- <span data-ttu-id="6cf3e-111">Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="6cf3e-112">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="6cf3e-113">Om du tar bort en auktoriseringsregel raderas också motsvarande användar behörighet.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="6cf3e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cf3e-114">EXAMPLES</span></span>

### <span data-ttu-id="6cf3e-115">Exempel 1: ta bort en auktoriseringsregel från ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="6cf3e-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6cf3e-116">Det här kommandot tar bort auktoriseringsregeln med namnet ListenRule från meddelande navet ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="6cf3e-117">När du kör det här kommandot måste du ange både namn området och resurs gruppen som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="6cf3e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cf3e-118">PARAMETERS</span></span>

### <span data-ttu-id="6cf3e-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6cf3e-119">-AuthorizationRule</span></span>
<span data-ttu-id="6cf3e-120">Anger namnet på den SAS-autentiseringsprocess som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6cf3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf3e-121">-DefaultProfile</span></span>
<span data-ttu-id="6cf3e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6cf3e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cf3e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6cf3e-123">-Force</span></span>
<span data-ttu-id="6cf3e-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6cf3e-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6cf3e-125">-Namespace</span></span>
<span data-ttu-id="6cf3e-126">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6cf3e-127">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6cf3e-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6cf3e-128">-NotificationHub</span></span>
<span data-ttu-id="6cf3e-129">Anger meddelandets Hub som auktoriseringsregler är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="6cf3e-130">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett plattform.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="6cf3e-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cf3e-131">-ResourceGroup</span></span>
<span data-ttu-id="6cf3e-132">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6cf3e-133">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6cf3e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cf3e-134">-Confirm</span></span>
<span data-ttu-id="6cf3e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cf3e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf3e-136">-WhatIf</span></span>
<span data-ttu-id="6cf3e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cf3e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cf3e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf3e-139">CommonParameters</span></span>
<span data-ttu-id="6cf3e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf3e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf3e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf3e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf3e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cf3e-142">INPUTS</span></span>

### <span data-ttu-id="6cf3e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf3e-143">System.String</span></span>

## <span data-ttu-id="6cf3e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cf3e-144">OUTPUTS</span></span>

### <span data-ttu-id="6cf3e-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="6cf3e-145">System.Void</span></span>

## <span data-ttu-id="6cf3e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cf3e-146">NOTES</span></span>

## <span data-ttu-id="6cf3e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cf3e-147">RELATED LINKS</span></span>

[<span data-ttu-id="6cf3e-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6cf3e-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="6cf3e-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6cf3e-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="6cf3e-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6cf3e-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)

