---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577608"
---
# <span data-ttu-id="24aaa-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="24aaa-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="24aaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="24aaa-103">Skapar en auktoriseringsregel och tilldelar regeln ett huvud meddelande.</span><span class="sxs-lookup"><span data-stu-id="24aaa-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24aaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24aaa-104">SYNTAX</span></span>

### <span data-ttu-id="24aaa-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="24aaa-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24aaa-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="24aaa-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24aaa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="24aaa-108">Cmdleten **New-AzureRmNotificationHubAuthorizationRules** skapar en auktoriseringsregel för delade Access-signaturer för aviserings nav.</span><span class="sxs-lookup"><span data-stu-id="24aaa-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="24aaa-109">Auktoriseringsregler används för att hantera åtkomst till dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="24aaa-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="24aaa-110">Detta görs genom att skapa länkar, som URI: er baserat på olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="24aaa-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="24aaa-111">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="24aaa-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="24aaa-112">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="24aaa-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="24aaa-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24aaa-113">EXAMPLES</span></span>

### <span data-ttu-id="24aaa-114">Exempel 1: skapa en auktoriseringsregel för aviserings nav</span><span class="sxs-lookup"><span data-stu-id="24aaa-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="24aaa-115">Det här kommandot skapar en ny auktoriseringsregel och tilldelar den till meddelande navet med namnet ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="24aaa-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="24aaa-116">Det här navet finns i ContosoNamespace-namnområdet och är tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="24aaa-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="24aaa-117">Observera att all konfigurations information för regeln, inklusive regel namnet, kommer att hämtas från den indatafil som C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="24aaa-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="24aaa-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24aaa-118">PARAMETERS</span></span>

### <span data-ttu-id="24aaa-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="24aaa-119">-InputFile</span></span>
<span data-ttu-id="24aaa-120">Anger indatafilen för den auktoriseringsregel som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="24aaa-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="24aaa-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="24aaa-121">-Namespace</span></span>
<span data-ttu-id="24aaa-122">Anger namn området som auktoriseringsregler tilldelas.</span><span class="sxs-lookup"><span data-stu-id="24aaa-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="24aaa-123">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="24aaa-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="24aaa-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="24aaa-124">-NotificationHub</span></span>
<span data-ttu-id="24aaa-125">Anger huvud meddelandets huvud som auktoriseringsregler tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="24aaa-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="24aaa-126">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="24aaa-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="24aaa-127">Observera att du måste ange namnet på ett befintligt meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="24aaa-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="24aaa-128">Cmdleten **New-AzureRmNotificationHubAuthorizationRules** kan inte skapa nya aviserings nav.</span><span class="sxs-lookup"><span data-stu-id="24aaa-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="24aaa-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24aaa-129">-ResourceGroup</span></span>
<span data-ttu-id="24aaa-130">Anger den resurs grupp som meddelande navet är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="24aaa-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="24aaa-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="24aaa-131">-SASRule</span></span>
<span data-ttu-id="24aaa-132">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de nya reglerna.</span><span class="sxs-lookup"><span data-stu-id="24aaa-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="24aaa-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24aaa-133">-Confirm</span></span>
<span data-ttu-id="24aaa-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24aaa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24aaa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24aaa-135">-WhatIf</span></span>
<span data-ttu-id="24aaa-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24aaa-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24aaa-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24aaa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24aaa-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24aaa-138">-DefaultProfile</span></span>
<span data-ttu-id="24aaa-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24aaa-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24aaa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24aaa-140">CommonParameters</span></span>
<span data-ttu-id="24aaa-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24aaa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24aaa-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24aaa-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24aaa-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24aaa-143">INPUTS</span></span>

## <span data-ttu-id="24aaa-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24aaa-144">OUTPUTS</span></span>

### <span data-ttu-id="24aaa-145">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="24aaa-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="24aaa-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24aaa-146">NOTES</span></span>

## <span data-ttu-id="24aaa-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24aaa-147">RELATED LINKS</span></span>

[<span data-ttu-id="24aaa-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="24aaa-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="24aaa-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="24aaa-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="24aaa-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="24aaa-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


