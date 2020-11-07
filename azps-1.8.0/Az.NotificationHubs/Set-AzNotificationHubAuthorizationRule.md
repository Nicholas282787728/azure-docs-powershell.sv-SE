---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74aa4d00d387e832c1abf02a5c65ca5e34e42123
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747607"
---
# <span data-ttu-id="49ac3-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="49ac3-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="49ac3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="49ac3-103">Anger auktoriseringsregler för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="49ac3-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="49ac3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49ac3-104">SYNTAX</span></span>

### <span data-ttu-id="49ac3-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ac3-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ac3-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ac3-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ac3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49ac3-107">DESCRIPTION</span></span>
<span data-ttu-id="49ac3-108">Cmdleten **set-AzNotificationHubAuthorizationRule** ändrar en auktoriseringsregel för en säkerhets Association för en delad Access-signatur som tilldelats till en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="49ac3-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="49ac3-109">Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, i enlighet med olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="49ac3-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="49ac3-110">Behörighets nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="49ac3-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="49ac3-111">Lyssna</span><span class="sxs-lookup"><span data-stu-id="49ac3-111">Listen</span></span>
- <span data-ttu-id="49ac3-112">Bifoga</span><span class="sxs-lookup"><span data-stu-id="49ac3-112">Send</span></span>
- <span data-ttu-id="49ac3-113">Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="49ac3-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="49ac3-114">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="49ac3-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="49ac3-115">Denna cmdlet erbjuder två sätt att ändra en auktoriseringsregel som tilldelats till ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="49ac3-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="49ac3-116">För en kan du skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="49ac3-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="49ac3-117">Du kan konfigurera objektet med .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="49ac3-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="49ac3-118">Du kan sedan kopiera de här egenskaps värdena till regeln genom att använda parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="49ac3-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="49ac3-119">Alternativt kan du skapa en JSON-fil (JavaScript Object Notation) med relevanta konfigurations värden och sedan tillämpa dessa värden genom *InputFile* -parametern.</span><span class="sxs-lookup"><span data-stu-id="49ac3-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="49ac3-120">En JSON-fil är en textfil som använder syntax som liknar den här: {"name": "ContosoAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="49ac3-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="49ac3-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="49ac3-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="49ac3-122">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="49ac3-122">"Rights": \[</span></span>  
        <span data-ttu-id="49ac3-123">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="49ac3-123">"Listen",</span></span>  
        <span data-ttu-id="49ac3-124">Bifoga</span><span class="sxs-lookup"><span data-stu-id="49ac3-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="49ac3-125">} När det används tillsammans med New-AzNotificationHubAuthorizationRule cmdlet ändrar det föregående JSON-provet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användare behörighet att avlyssna och skicka rättigheter till navet.</span><span class="sxs-lookup"><span data-stu-id="49ac3-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="49ac3-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49ac3-126">EXAMPLES</span></span>

### <span data-ttu-id="49ac3-127">Exempel 1: ändra en auktoriseringsregel som tilldelats till ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="49ac3-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="49ac3-128">Det här kommandot ändrar en auktoriseringsregel som tilldelats till aviserings navet med namnet ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="49ac3-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="49ac3-129">Du måste ange namn området där navet finns samt resurs gruppen som navet är tilldelat.</span><span class="sxs-lookup"><span data-stu-id="49ac3-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="49ac3-130">Information om den regel som ändras är inte inkluderad i själva kommandot.</span><span class="sxs-lookup"><span data-stu-id="49ac3-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="49ac3-131">Den informationen finns i stället i C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="49ac3-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="49ac3-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49ac3-132">PARAMETERS</span></span>

### <span data-ttu-id="49ac3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ac3-133">-DefaultProfile</span></span>
<span data-ttu-id="49ac3-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="49ac3-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ac3-135">-Force</span><span class="sxs-lookup"><span data-stu-id="49ac3-135">-Force</span></span>
<span data-ttu-id="49ac3-136">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="49ac3-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="49ac3-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="49ac3-137">-InputFile</span></span>
<span data-ttu-id="49ac3-138">Anger sökvägen till en JSON-fil med konfigurations information för den nya regeln.</span><span class="sxs-lookup"><span data-stu-id="49ac3-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="49ac3-139">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="49ac3-139">-Namespace</span></span>
<span data-ttu-id="49ac3-140">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="49ac3-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="49ac3-141">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="49ac3-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="49ac3-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="49ac3-142">-NotificationHub</span></span>
<span data-ttu-id="49ac3-143">Anger meddelandets hubb som denna cmdlet tilldelar auktoriseringsregler till.</span><span class="sxs-lookup"><span data-stu-id="49ac3-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="49ac3-144">Meddelande nav används för att skicka push-aviseringar till flera klienter oavsett hur dessa klienter används.</span><span class="sxs-lookup"><span data-stu-id="49ac3-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="49ac3-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49ac3-145">-ResourceGroup</span></span>
<span data-ttu-id="49ac3-146">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="49ac3-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="49ac3-147">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="49ac3-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="49ac3-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="49ac3-148">-SASRule</span></span>
<span data-ttu-id="49ac3-149">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de auktoriseringsregler som har ändrats.</span><span class="sxs-lookup"><span data-stu-id="49ac3-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="49ac3-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49ac3-150">-Confirm</span></span>
<span data-ttu-id="49ac3-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49ac3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ac3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ac3-152">-WhatIf</span></span>
<span data-ttu-id="49ac3-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49ac3-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49ac3-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49ac3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ac3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ac3-155">CommonParameters</span></span>
<span data-ttu-id="49ac3-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ac3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ac3-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ac3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ac3-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49ac3-158">INPUTS</span></span>

### <span data-ttu-id="49ac3-159">System. String</span><span class="sxs-lookup"><span data-stu-id="49ac3-159">System.String</span></span>

## <span data-ttu-id="49ac3-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49ac3-160">OUTPUTS</span></span>

### <span data-ttu-id="49ac3-161">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="49ac3-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="49ac3-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49ac3-162">NOTES</span></span>

## <span data-ttu-id="49ac3-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49ac3-163">RELATED LINKS</span></span>

[<span data-ttu-id="49ac3-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="49ac3-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="49ac3-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="49ac3-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="49ac3-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="49ac3-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


