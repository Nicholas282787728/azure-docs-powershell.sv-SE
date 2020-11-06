---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575936"
---
# <span data-ttu-id="2a323-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2a323-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="2a323-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a323-102">SYNOPSIS</span></span>
<span data-ttu-id="2a323-103">Tar bort ett namn område för en avisering.</span><span class="sxs-lookup"><span data-stu-id="2a323-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a323-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a323-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a323-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a323-105">DESCRIPTION</span></span>
<span data-ttu-id="2a323-106">Cmdleten **Remove-AzureRmNotificationHubsNamespace** tar bort ett namn område för aviserings navet från din distribution.</span><span class="sxs-lookup"><span data-stu-id="2a323-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="2a323-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2a323-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="2a323-108">Cmdleten **Remove-AzureRmNotificationHubsNamespace** tar bort ett namn område för aviserings navet från din distribution.</span><span class="sxs-lookup"><span data-stu-id="2a323-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="2a323-109">När du kör denna cmdlet tas det angivna namn området bort tillsammans med alla aviserings nav som är kopplade till namn området.</span><span class="sxs-lookup"><span data-stu-id="2a323-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="2a323-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a323-110">EXAMPLES</span></span>

### <span data-ttu-id="2a323-111">Exempel 1: ta bort ett namn område för en avisering</span><span class="sxs-lookup"><span data-stu-id="2a323-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="2a323-112">Det här kommandot tar bort namn området med namnet ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="2a323-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="2a323-113">Du måste ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="2a323-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="2a323-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a323-114">PARAMETERS</span></span>

### <span data-ttu-id="2a323-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2a323-115">-Force</span></span>
<span data-ttu-id="2a323-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2a323-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2a323-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2a323-117">-Namespace</span></span>
<span data-ttu-id="2a323-118">Anger det namn område som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2a323-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="2a323-119">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2a323-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2a323-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a323-120">-ResourceGroup</span></span>
<span data-ttu-id="2a323-121">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="2a323-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="2a323-122">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="2a323-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="2a323-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a323-123">-Confirm</span></span>
<span data-ttu-id="2a323-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a323-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a323-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a323-125">-WhatIf</span></span>
<span data-ttu-id="2a323-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a323-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a323-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a323-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a323-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a323-128">-DefaultProfile</span></span>
<span data-ttu-id="2a323-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a323-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a323-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a323-130">CommonParameters</span></span>
<span data-ttu-id="2a323-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a323-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a323-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a323-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a323-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a323-133">INPUTS</span></span>

## <span data-ttu-id="2a323-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a323-134">OUTPUTS</span></span>

## <span data-ttu-id="2a323-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a323-135">NOTES</span></span>

## <span data-ttu-id="2a323-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a323-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a323-137">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2a323-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="2a323-138">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2a323-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="2a323-139">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2a323-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


