---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576850"
---
# <span data-ttu-id="88013-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="88013-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="88013-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88013-102">SYNOPSIS</span></span>
<span data-ttu-id="88013-103">Tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="88013-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88013-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88013-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88013-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88013-105">DESCRIPTION</span></span>
<span data-ttu-id="88013-106">Cmdleten **Remove-AzureRmNotificationHub** tar bort ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="88013-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="88013-107">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="88013-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="88013-108">Plattformerna inkluderar, men är inte begränsade till: iOS, Android, Windows Phone 8 och Windows Store.</span><span class="sxs-lookup"><span data-stu-id="88013-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="88013-109">Meddelande NAV är ungefär likvärdiga med enskilda appar: alla dina appar har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="88013-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="88013-110">Du kan ta bort ett befintligt meddelande nav med hjälp av cmdleten **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="88013-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="88013-111">När navet har tagits bort kan du inte längre använda navet för att skicka push-meddelanden till användarna.</span><span class="sxs-lookup"><span data-stu-id="88013-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="88013-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88013-112">EXAMPLES</span></span>

### <span data-ttu-id="88013-113">Exempel 1: ta bort ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="88013-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="88013-114">Det här kommandot tar bort meddelande navet med namnet ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="88013-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="88013-115">För att ta bort navet måste du ange namn området där navet finns samt den resurs grupp som navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="88013-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="88013-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88013-116">PARAMETERS</span></span>

### <span data-ttu-id="88013-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88013-117">-DefaultProfile</span></span>
<span data-ttu-id="88013-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="88013-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88013-119">-Force</span><span class="sxs-lookup"><span data-stu-id="88013-119">-Force</span></span>
<span data-ttu-id="88013-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="88013-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="88013-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="88013-121">-Namespace</span></span>
<span data-ttu-id="88013-122">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="88013-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="88013-123">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="88013-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="88013-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="88013-124">-NotificationHub</span></span>
<span data-ttu-id="88013-125">Anger vilket meddelande nav som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="88013-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="88013-126">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="88013-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="88013-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88013-127">-ResourceGroup</span></span>
<span data-ttu-id="88013-128">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="88013-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="88013-129">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="88013-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="88013-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88013-130">-Confirm</span></span>
<span data-ttu-id="88013-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88013-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88013-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88013-132">-WhatIf</span></span>
<span data-ttu-id="88013-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88013-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88013-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88013-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88013-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88013-135">CommonParameters</span></span>
<span data-ttu-id="88013-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88013-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88013-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88013-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88013-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88013-138">INPUTS</span></span>

### <span data-ttu-id="88013-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88013-139">System.String</span></span>

## <span data-ttu-id="88013-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88013-140">OUTPUTS</span></span>

### <span data-ttu-id="88013-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="88013-141">System.Void</span></span>

## <span data-ttu-id="88013-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88013-142">NOTES</span></span>

## <span data-ttu-id="88013-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88013-143">RELATED LINKS</span></span>

[<span data-ttu-id="88013-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="88013-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="88013-145">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="88013-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="88013-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="88013-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


