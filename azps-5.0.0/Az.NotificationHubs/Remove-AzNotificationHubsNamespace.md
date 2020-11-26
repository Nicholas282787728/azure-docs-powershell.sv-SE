---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323178"
---
# <span data-ttu-id="bf278-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf278-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="bf278-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf278-102">SYNOPSIS</span></span>
<span data-ttu-id="bf278-103">Tar bort ett namn område för en avisering.</span><span class="sxs-lookup"><span data-stu-id="bf278-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="bf278-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf278-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf278-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf278-105">DESCRIPTION</span></span>
<span data-ttu-id="bf278-106">Cmdleten **Remove-AzNotificationHubsNamespace** tar bort ett namn område för aviserings navet från din distribution.</span><span class="sxs-lookup"><span data-stu-id="bf278-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="bf278-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="bf278-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="bf278-108">Cmdleten **Remove-AzNotificationHubsNamespace** tar bort ett namn område för aviserings navet från din distribution.</span><span class="sxs-lookup"><span data-stu-id="bf278-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="bf278-109">När du kör denna cmdlet tas det angivna namn området bort tillsammans med alla aviserings nav som är kopplade till namn området.</span><span class="sxs-lookup"><span data-stu-id="bf278-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="bf278-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf278-110">EXAMPLES</span></span>

### <span data-ttu-id="bf278-111">Exempel 1: ta bort ett namn område för en avisering</span><span class="sxs-lookup"><span data-stu-id="bf278-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="bf278-112">Det här kommandot tar bort namn området med namnet ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="bf278-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="bf278-113">Du måste ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="bf278-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="bf278-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf278-114">PARAMETERS</span></span>

### <span data-ttu-id="bf278-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf278-115">-DefaultProfile</span></span>
<span data-ttu-id="bf278-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf278-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf278-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bf278-117">-Force</span></span>
<span data-ttu-id="bf278-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bf278-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bf278-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="bf278-119">-Namespace</span></span>
<span data-ttu-id="bf278-120">Anger det namn område som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="bf278-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="bf278-121">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="bf278-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bf278-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf278-122">-ResourceGroup</span></span>
<span data-ttu-id="bf278-123">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="bf278-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="bf278-124">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="bf278-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bf278-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf278-125">-Confirm</span></span>
<span data-ttu-id="bf278-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf278-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf278-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf278-127">-WhatIf</span></span>
<span data-ttu-id="bf278-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf278-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf278-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf278-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf278-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf278-130">CommonParameters</span></span>
<span data-ttu-id="bf278-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf278-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf278-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf278-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf278-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf278-133">INPUTS</span></span>

### <span data-ttu-id="bf278-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bf278-134">System.String</span></span>

## <span data-ttu-id="bf278-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf278-135">OUTPUTS</span></span>

### <span data-ttu-id="bf278-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="bf278-136">System.Void</span></span>

## <span data-ttu-id="bf278-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf278-137">NOTES</span></span>

## <span data-ttu-id="bf278-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf278-138">RELATED LINKS</span></span>

[<span data-ttu-id="bf278-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf278-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="bf278-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf278-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="bf278-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf278-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)

