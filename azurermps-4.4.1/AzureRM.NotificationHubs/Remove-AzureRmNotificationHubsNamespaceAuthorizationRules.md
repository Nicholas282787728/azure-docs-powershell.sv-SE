---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: e9b699e8839f2ba9426945ef0de883c4bfac40d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756908"
---
# <span data-ttu-id="b8fdd-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b8fdd-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="b8fdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fdd-103">Tar bort en auktoriseringsregel från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8fdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8fdd-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8fdd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fdd-106">Cmdleten **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** tar bort en auktoriseringsregel för delade Access-signaturer från ett namn område i ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="b8fdd-107">Auktoriseringsregler hanterar åtkomst till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="b8fdd-108">Detta görs genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b8fdd-109">Behörighets nivåerna kan vara följande:</span><span class="sxs-lookup"><span data-stu-id="b8fdd-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="b8fdd-110">Lyssna</span><span class="sxs-lookup"><span data-stu-id="b8fdd-110">Listen</span></span>
- <span data-ttu-id="b8fdd-111">Bifoga</span><span class="sxs-lookup"><span data-stu-id="b8fdd-111">Send</span></span>
- <span data-ttu-id="b8fdd-112">Inställningar</span><span class="sxs-lookup"><span data-stu-id="b8fdd-112">Manage</span></span>

<span data-ttu-id="b8fdd-113">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b8fdd-114">Till exempel dirigeras en klient med lyssnings behörighet till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="b8fdd-115">Om du tar bort en auktoriseringsregel raderas också motsvarande användar behörighet.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="b8fdd-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8fdd-116">EXAMPLES</span></span>

### <span data-ttu-id="b8fdd-117">Exempel 1: ta bort en auktoriseringsregel från ett namn område</span><span class="sxs-lookup"><span data-stu-id="b8fdd-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b8fdd-118">Det här kommandot tar bort auktoriseringsregeln med namnet ListenRule från namn området med namnet ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="b8fdd-119">När du kör det här kommandot måste du ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="b8fdd-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8fdd-120">PARAMETERS</span></span>

### <span data-ttu-id="b8fdd-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b8fdd-121">-AuthorizationRule</span></span>
<span data-ttu-id="b8fdd-122">Anger namnet på den ÖVERVAKNINGSORGAN-regel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="b8fdd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b8fdd-123">-Force</span></span>
<span data-ttu-id="b8fdd-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b8fdd-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b8fdd-125">-Namespace</span></span>
<span data-ttu-id="b8fdd-126">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-126">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b8fdd-127">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b8fdd-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b8fdd-128">-ResourceGroup</span></span>
<span data-ttu-id="b8fdd-129">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-129">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b8fdd-130">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b8fdd-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8fdd-131">-Confirm</span></span>
<span data-ttu-id="b8fdd-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fdd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fdd-133">-WhatIf</span></span>
<span data-ttu-id="b8fdd-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8fdd-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fdd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fdd-136">-DefaultProfile</span></span>
<span data-ttu-id="b8fdd-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8fdd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fdd-138">CommonParameters</span></span>
<span data-ttu-id="b8fdd-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8fdd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fdd-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fdd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fdd-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8fdd-141">INPUTS</span></span>

## <span data-ttu-id="b8fdd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8fdd-142">OUTPUTS</span></span>

### <span data-ttu-id="b8fdd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8fdd-143">System.Boolean</span></span>

## <span data-ttu-id="b8fdd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8fdd-144">NOTES</span></span>

## <span data-ttu-id="b8fdd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8fdd-145">RELATED LINKS</span></span>

[<span data-ttu-id="b8fdd-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b8fdd-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="b8fdd-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b8fdd-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="b8fdd-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b8fdd-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

