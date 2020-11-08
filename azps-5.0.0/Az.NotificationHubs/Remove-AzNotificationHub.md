---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269275"
---
# <span data-ttu-id="33463-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33463-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="33463-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33463-102">SYNOPSIS</span></span>
<span data-ttu-id="33463-103">Tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="33463-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="33463-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33463-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33463-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33463-105">DESCRIPTION</span></span>
<span data-ttu-id="33463-106">Cmdleten **Remove-AzNotificationHub** tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="33463-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="33463-107">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="33463-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="33463-108">Plattformerna inkluderar, men är inte begränsade till: iOS, Android, Windows Phone 8 och Windows Store.</span><span class="sxs-lookup"><span data-stu-id="33463-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="33463-109">Meddelande NAV är ungefär likvärdiga med enskilda appar: alla dina appar har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="33463-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="33463-110">Du kan ta bort ett befintligt meddelande nav med hjälp av cmdleten **Remove-AzNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="33463-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="33463-111">När navet har tagits bort kan du inte längre använda navet för att skicka push-meddelanden till användarna.</span><span class="sxs-lookup"><span data-stu-id="33463-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="33463-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33463-112">EXAMPLES</span></span>

### <span data-ttu-id="33463-113">Exempel 1: ta bort ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="33463-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="33463-114">Det här kommandot tar bort meddelande navet med namnet ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="33463-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="33463-115">För att ta bort navet måste du ange namn området där navet finns samt den resurs grupp som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="33463-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="33463-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33463-116">PARAMETERS</span></span>

### <span data-ttu-id="33463-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33463-117">-DefaultProfile</span></span>
<span data-ttu-id="33463-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="33463-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33463-119">-Force</span><span class="sxs-lookup"><span data-stu-id="33463-119">-Force</span></span>
<span data-ttu-id="33463-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="33463-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33463-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="33463-121">-Namespace</span></span>
<span data-ttu-id="33463-122">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="33463-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="33463-123">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="33463-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="33463-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="33463-124">-NotificationHub</span></span>
<span data-ttu-id="33463-125">Anger vilket meddelande nav som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="33463-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="33463-126">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="33463-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="33463-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33463-127">-ResourceGroup</span></span>
<span data-ttu-id="33463-128">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="33463-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="33463-129">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="33463-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="33463-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33463-130">-Confirm</span></span>
<span data-ttu-id="33463-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33463-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33463-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33463-132">-WhatIf</span></span>
<span data-ttu-id="33463-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33463-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33463-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33463-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33463-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33463-135">CommonParameters</span></span>
<span data-ttu-id="33463-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33463-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33463-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33463-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33463-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33463-138">INPUTS</span></span>

### <span data-ttu-id="33463-139">System. String</span><span class="sxs-lookup"><span data-stu-id="33463-139">System.String</span></span>

## <span data-ttu-id="33463-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33463-140">OUTPUTS</span></span>

### <span data-ttu-id="33463-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="33463-141">System.Void</span></span>

## <span data-ttu-id="33463-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33463-142">NOTES</span></span>

## <span data-ttu-id="33463-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33463-143">RELATED LINKS</span></span>

[<span data-ttu-id="33463-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33463-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="33463-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33463-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="33463-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33463-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


