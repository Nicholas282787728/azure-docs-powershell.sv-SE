---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575934"
---
# <span data-ttu-id="4cf52-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4cf52-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="4cf52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cf52-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf52-103">Anger auktoriseringsregler för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="4cf52-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cf52-104">SYNTAX</span></span>

### <span data-ttu-id="4cf52-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf52-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf52-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf52-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cf52-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cf52-107">DESCRIPTION</span></span>
<span data-ttu-id="4cf52-108">Cmdleten **set-AzureRmNotificationHubAuthorizationRules** ändrar en auktoriseringsregel för en säkerhets Association för en delad Access-signatur som tilldelats till en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="4cf52-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="4cf52-109">Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, i enlighet med olika behörighets nivåer.</span><span class="sxs-lookup"><span data-stu-id="4cf52-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="4cf52-110">Behörighets nivåerna kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="4cf52-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="4cf52-111">Lyssna</span><span class="sxs-lookup"><span data-stu-id="4cf52-111">Listen</span></span>
- <span data-ttu-id="4cf52-112">Bifoga</span><span class="sxs-lookup"><span data-stu-id="4cf52-112">Send</span></span>
- <span data-ttu-id="4cf52-113">Inställningar</span><span class="sxs-lookup"><span data-stu-id="4cf52-113">Manage</span></span>

<span data-ttu-id="4cf52-114">Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.</span><span class="sxs-lookup"><span data-stu-id="4cf52-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="4cf52-115">Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.</span><span class="sxs-lookup"><span data-stu-id="4cf52-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="4cf52-116">Denna cmdlet erbjuder två sätt att ändra en auktoriseringsregel som tilldelats till ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="4cf52-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="4cf52-117">För en kan du skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="4cf52-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="4cf52-118">Du kan konfigurera objektet med .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4cf52-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="4cf52-119">Du kan sedan kopiera de här egenskaps värdena till regeln genom att använda parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="4cf52-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="4cf52-120">Alternativt kan du skapa en JSON-fil (JavaScript Object Notation) med relevanta konfigurations värden och sedan tillämpa dessa värden genom *InputFile* -parametern.</span><span class="sxs-lookup"><span data-stu-id="4cf52-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="4cf52-121">En JSON-fil är en textfil som använder syntax som liknar den här:</span><span class="sxs-lookup"><span data-stu-id="4cf52-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="4cf52-122">{"Namn": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="4cf52-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="4cf52-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="4cf52-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="4cf52-124">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="4cf52-124">"Rights": \[</span></span>  
        <span data-ttu-id="4cf52-125">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="4cf52-125">"Listen",</span></span>  
        <span data-ttu-id="4cf52-126">Bifoga</span><span class="sxs-lookup"><span data-stu-id="4cf52-126">"Send"</span></span>  
    \]  
<span data-ttu-id="4cf52-127">}</span><span class="sxs-lookup"><span data-stu-id="4cf52-127">}</span></span>

<span data-ttu-id="4cf52-128">När det används tillsammans med New-AzureRmNotificationHubAuthorizationRules cmdlet ändrar det föregående JSON-provet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användarna behörighet att lyssna och skicka till navet.</span><span class="sxs-lookup"><span data-stu-id="4cf52-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="4cf52-129">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cf52-129">EXAMPLES</span></span>

### <span data-ttu-id="4cf52-130">Exempel 1: ändra en auktoriseringsregel som tilldelats till ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="4cf52-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="4cf52-131">Det här kommandot ändrar en auktoriseringsregel som tilldelats till aviserings navet med namnet ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="4cf52-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="4cf52-132">Du måste ange namn området där navet finns samt resurs gruppen som navet är tilldelat.</span><span class="sxs-lookup"><span data-stu-id="4cf52-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="4cf52-133">Information om den regel som ändras är inte inkluderad i själva kommandot.</span><span class="sxs-lookup"><span data-stu-id="4cf52-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="4cf52-134">Den informationen finns i stället i C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="4cf52-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="4cf52-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cf52-135">PARAMETERS</span></span>

### <span data-ttu-id="4cf52-136">-Force</span><span class="sxs-lookup"><span data-stu-id="4cf52-136">-Force</span></span>
<span data-ttu-id="4cf52-137">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4cf52-137">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4cf52-138">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4cf52-138">-InputFile</span></span>
<span data-ttu-id="4cf52-139">Anger sökvägen till en JSON-fil med konfigurations information för den nya regeln.</span><span class="sxs-lookup"><span data-stu-id="4cf52-139">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="4cf52-140">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="4cf52-140">-Namespace</span></span>
<span data-ttu-id="4cf52-141">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="4cf52-141">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4cf52-142">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="4cf52-142">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4cf52-143">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4cf52-143">-NotificationHub</span></span>
<span data-ttu-id="4cf52-144">Anger meddelandets hubb som denna cmdlet tilldelar auktoriseringsregler till.</span><span class="sxs-lookup"><span data-stu-id="4cf52-144">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="4cf52-145">Meddelande nav används för att skicka push-aviseringar till flera klienter oavsett hur dessa klienter används.</span><span class="sxs-lookup"><span data-stu-id="4cf52-145">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="4cf52-146">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4cf52-146">-ResourceGroup</span></span>
<span data-ttu-id="4cf52-147">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="4cf52-147">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="4cf52-148">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="4cf52-148">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4cf52-149">-SASRule</span><span class="sxs-lookup"><span data-stu-id="4cf52-149">-SASRule</span></span>
<span data-ttu-id="4cf52-150">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de auktoriseringsregler som har ändrats.</span><span class="sxs-lookup"><span data-stu-id="4cf52-150">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="4cf52-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cf52-151">-Confirm</span></span>
<span data-ttu-id="4cf52-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cf52-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf52-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf52-153">-WhatIf</span></span>
<span data-ttu-id="4cf52-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cf52-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cf52-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cf52-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf52-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf52-156">-DefaultProfile</span></span>
<span data-ttu-id="4cf52-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf52-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cf52-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf52-158">CommonParameters</span></span>
<span data-ttu-id="4cf52-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf52-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf52-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf52-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf52-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cf52-161">INPUTS</span></span>

## <span data-ttu-id="4cf52-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cf52-162">OUTPUTS</span></span>

### <span data-ttu-id="4cf52-163">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4cf52-163">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4cf52-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cf52-164">NOTES</span></span>

## <span data-ttu-id="4cf52-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cf52-165">RELATED LINKS</span></span>

[<span data-ttu-id="4cf52-166">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4cf52-166">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="4cf52-167">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4cf52-167">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="4cf52-168">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4cf52-168">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


