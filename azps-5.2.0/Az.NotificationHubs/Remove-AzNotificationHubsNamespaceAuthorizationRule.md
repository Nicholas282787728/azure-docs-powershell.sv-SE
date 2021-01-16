---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395227"
---
# <span data-ttu-id="2c481-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c481-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="2c481-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c481-102">SYNOPSIS</span></span>
<span data-ttu-id="2c481-103">Tar bort en auktoriseringsregel från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="2c481-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="2c481-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c481-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c481-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c481-105">DESCRIPTION</span></span>
<span data-ttu-id="2c481-106">Cmdleten **Remove-AzNotificationHubsNamespaceAuthorizationRule** tar bort en auktoriseringsregel för delade Access-signaturer från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="2c481-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="2c481-107">Auktoriseringsregler hanterar åtkomst till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="2c481-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="2c481-108">Detta görs genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="2c481-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="2c481-109">Behörighets nivåerna kan vara följande:</span><span class="sxs-lookup"><span data-stu-id="2c481-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="2c481-110">Lyssna</span><span class="sxs-lookup"><span data-stu-id="2c481-110">Listen</span></span>
- <span data-ttu-id="2c481-111">Bifoga</span><span class="sxs-lookup"><span data-stu-id="2c481-111">Send</span></span>
- <span data-ttu-id="2c481-112">Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="2c481-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="2c481-113">Till exempel dirigeras en klient med lyssnings behörighet till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="2c481-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="2c481-114">Om du tar bort en auktoriseringsregel raderas också motsvarande användar behörighet.</span><span class="sxs-lookup"><span data-stu-id="2c481-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="2c481-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c481-115">EXAMPLES</span></span>

### <span data-ttu-id="2c481-116">Exempel 1: ta bort en auktoriseringsregel från ett namn område</span><span class="sxs-lookup"><span data-stu-id="2c481-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="2c481-117">Det här kommandot tar bort auktoriseringsregeln med namnet ListenRule från namn området med namnet ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="2c481-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="2c481-118">När du kör det här kommandot måste du ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="2c481-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="2c481-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c481-119">PARAMETERS</span></span>

### <span data-ttu-id="2c481-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c481-120">-AuthorizationRule</span></span>
<span data-ttu-id="2c481-121">Anger namnet på den ÖVERVAKNINGSORGAN-regel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c481-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="2c481-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c481-122">-DefaultProfile</span></span>
<span data-ttu-id="2c481-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c481-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c481-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2c481-124">-Force</span></span>
<span data-ttu-id="2c481-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2c481-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c481-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2c481-126">-Namespace</span></span>
<span data-ttu-id="2c481-127">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="2c481-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="2c481-128">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2c481-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2c481-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c481-129">-ResourceGroup</span></span>
<span data-ttu-id="2c481-130">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="2c481-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="2c481-131">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="2c481-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="2c481-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c481-132">-Confirm</span></span>
<span data-ttu-id="2c481-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c481-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c481-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c481-134">-WhatIf</span></span>
<span data-ttu-id="2c481-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c481-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c481-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c481-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c481-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c481-137">CommonParameters</span></span>
<span data-ttu-id="2c481-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c481-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c481-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c481-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c481-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c481-140">INPUTS</span></span>

### <span data-ttu-id="2c481-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c481-141">System.String</span></span>

## <span data-ttu-id="2c481-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c481-142">OUTPUTS</span></span>

### <span data-ttu-id="2c481-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c481-143">System.Boolean</span></span>

## <span data-ttu-id="2c481-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c481-144">NOTES</span></span>

## <span data-ttu-id="2c481-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c481-145">RELATED LINKS</span></span>

[<span data-ttu-id="2c481-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c481-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="2c481-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c481-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="2c481-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c481-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


