---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262480"
---
# <span data-ttu-id="2ebdd-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ebdd-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="2ebdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ebdd-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebdd-103">Skapar en auktoriseringsregel och tilldelar regeln ett huvud meddelande.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="2ebdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ebdd-104">SYNTAX</span></span>

### <span data-ttu-id="2ebdd-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebdd-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ebdd-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebdd-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ebdd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ebdd-107">DESCRIPTION</span></span>
<span data-ttu-id="2ebdd-108">Cmdleten **New-AzNotificationHubAuthorizationRule** skapar en auktoriseringsregel för delade Access-signaturer för aviserings nav.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="2ebdd-109">Auktoriseringsregler används för att hantera åtkomst till dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="2ebdd-110">Detta görs genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="2ebdd-111">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="2ebdd-112">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="2ebdd-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ebdd-113">EXAMPLES</span></span>

### <span data-ttu-id="2ebdd-114">Exempel 1: skapa en auktoriseringsregel för aviserings nav</span><span class="sxs-lookup"><span data-stu-id="2ebdd-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="2ebdd-115">Det här kommandot skapar en ny auktoriseringsregel och tilldelar den till meddelande navet med namnet ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="2ebdd-116">Det här navet finns i ContosoNamespace-namnområdet och är tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="2ebdd-117">Observera att all konfigurations information för regeln, inklusive regel namnet, kommer att hämtas från den indatafil som C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="2ebdd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ebdd-118">PARAMETERS</span></span>

### <span data-ttu-id="2ebdd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebdd-119">-DefaultProfile</span></span>
<span data-ttu-id="2ebdd-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2ebdd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ebdd-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2ebdd-121">-InputFile</span></span>
<span data-ttu-id="2ebdd-122">Anger indatafilen för den auktoriseringsregel som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebdd-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2ebdd-123">-Namespace</span></span>
<span data-ttu-id="2ebdd-124">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="2ebdd-125">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2ebdd-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2ebdd-126">-NotificationHub</span></span>
<span data-ttu-id="2ebdd-127">Anger huvud meddelandets huvud som auktoriseringsregler tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="2ebdd-128">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="2ebdd-129">Observera att du måste ange namnet på ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="2ebdd-130">Cmdleten **New-AzNotificationHubAuthorizationRule** kan inte skapa nya aviserings nav.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="2ebdd-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2ebdd-131">-ResourceGroup</span></span>
<span data-ttu-id="2ebdd-132">Anger den resurs grupp som meddelande navet är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="2ebdd-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="2ebdd-133">-SASRule</span></span>
<span data-ttu-id="2ebdd-134">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de nya reglerna.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebdd-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ebdd-135">-Confirm</span></span>
<span data-ttu-id="2ebdd-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebdd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebdd-137">-WhatIf</span></span>
<span data-ttu-id="2ebdd-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ebdd-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebdd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebdd-140">CommonParameters</span></span>
<span data-ttu-id="2ebdd-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebdd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebdd-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ebdd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebdd-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ebdd-143">INPUTS</span></span>

### <span data-ttu-id="2ebdd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2ebdd-144">System.String</span></span>

## <span data-ttu-id="2ebdd-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ebdd-145">OUTPUTS</span></span>

### <span data-ttu-id="2ebdd-146">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2ebdd-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2ebdd-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ebdd-147">NOTES</span></span>

## <span data-ttu-id="2ebdd-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ebdd-148">RELATED LINKS</span></span>

[<span data-ttu-id="2ebdd-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ebdd-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="2ebdd-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ebdd-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="2ebdd-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ebdd-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)

