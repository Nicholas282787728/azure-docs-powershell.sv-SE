---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: a25e318aca1bca33c309a6f24b862e98c02659e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575927"
---
# <span data-ttu-id="f5b49-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5b49-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="f5b49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5b49-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b49-103">Anger auktoriseringsregler för ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="f5b49-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5b49-104">SYNTAX</span></span>

### <span data-ttu-id="f5b49-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5b49-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5b49-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5b49-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5b49-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5b49-107">DESCRIPTION</span></span>
<span data-ttu-id="f5b49-108">Cmdleten **set-AzureRmNotificationHubsNamespaceAuthorizationRules** ändrar en auktoriseringsregel för en säkerhets Association för en delad Access-signatur som har tilldelats ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="f5b49-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="f5b49-109">Auktoriseringsregler hanterar användar rättigheter till namn området och aviserings hubbarna i namn området.</span><span class="sxs-lookup"><span data-stu-id="f5b49-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="f5b49-110">Denna cmdlet erbjuder två sätt att ändra en auktoriseringsregel som tilldelats ett namn område.</span><span class="sxs-lookup"><span data-stu-id="f5b49-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="f5b49-111">För en kan du skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="f5b49-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="f5b49-112">Du kan använda .NET Framework för att åstadkomma detta.</span><span class="sxs-lookup"><span data-stu-id="f5b49-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="f5b49-113">Du kan sedan kopiera de här egenskaps värdena till regeln via parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="f5b49-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="f5b49-114">Alternativt kan du skapa en JSON-fil (JavaScript Object Notation) med relevanta konfigurations värden och sedan tillämpa dessa värden genom *InputFile* -parametern.</span><span class="sxs-lookup"><span data-stu-id="f5b49-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="f5b49-115">En JSON-fil är en textfil som använder syntax som liknar den här:</span><span class="sxs-lookup"><span data-stu-id="f5b49-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="f5b49-116">{</span><span class="sxs-lookup"><span data-stu-id="f5b49-116">{</span></span>  
    <span data-ttu-id="f5b49-117">"Namn": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="f5b49-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="f5b49-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="f5b49-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="f5b49-119">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="f5b49-119">"Rights": \[</span></span>  
        <span data-ttu-id="f5b49-120">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="f5b49-120">"Listen",</span></span>  
        <span data-ttu-id="f5b49-121">Bifoga</span><span class="sxs-lookup"><span data-stu-id="f5b49-121">"Send"</span></span>  
    \]  
<span data-ttu-id="f5b49-122">}</span><span class="sxs-lookup"><span data-stu-id="f5b49-122">}</span></span>

<span data-ttu-id="f5b49-123">När det används tillsammans med cmdleten **set-AzureRmNotificationHubsNamespaceAuthorizationRules** ändrar det föregående JSON-provet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användare behörighet att avlyssna och skicka rättigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="f5b49-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="f5b49-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5b49-124">EXAMPLES</span></span>

### <span data-ttu-id="f5b49-125">Exempel 1: ändra en auktoriseringsregel som tilldelats ett namn område</span><span class="sxs-lookup"><span data-stu-id="f5b49-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="f5b49-126">Det här kommandot ändrar en auktoriseringsregel som tilldelats namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f5b49-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="f5b49-127">Du måste ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="f5b49-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="f5b49-128">Information om auktoriseringsregeln är inte inkluderad i själva kommandot.</span><span class="sxs-lookup"><span data-stu-id="f5b49-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="f5b49-129">I stället hämtas den informationen från indatafilen C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="f5b49-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="f5b49-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5b49-130">PARAMETERS</span></span>

### <span data-ttu-id="f5b49-131">-Force</span><span class="sxs-lookup"><span data-stu-id="f5b49-131">-Force</span></span>
<span data-ttu-id="f5b49-132">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f5b49-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f5b49-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f5b49-133">-InputFile</span></span>
<span data-ttu-id="f5b49-134">Anger sökvägen till en JSON-fil med konfigurations information för den nya regeln.</span><span class="sxs-lookup"><span data-stu-id="f5b49-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b49-135">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f5b49-135">-Namespace</span></span>
<span data-ttu-id="f5b49-136">Anger namn området som innehåller de auktoriseringsregler som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f5b49-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="f5b49-137">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="f5b49-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f5b49-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5b49-138">-ResourceGroup</span></span>
<span data-ttu-id="f5b49-139">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f5b49-139">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="f5b49-140">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="f5b49-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f5b49-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="f5b49-141">-SASRule</span></span>
<span data-ttu-id="f5b49-142">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de auktoriseringsregler som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f5b49-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b49-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5b49-143">-Confirm</span></span>
<span data-ttu-id="f5b49-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5b49-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5b49-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5b49-145">-WhatIf</span></span>
<span data-ttu-id="f5b49-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5b49-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5b49-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5b49-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5b49-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b49-148">-DefaultProfile</span></span>
<span data-ttu-id="f5b49-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b49-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5b49-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b49-150">CommonParameters</span></span>
<span data-ttu-id="f5b49-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b49-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b49-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b49-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b49-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5b49-153">INPUTS</span></span>

## <span data-ttu-id="f5b49-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5b49-154">OUTPUTS</span></span>

### <span data-ttu-id="f5b49-155">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f5b49-155">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f5b49-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5b49-156">NOTES</span></span>

## <span data-ttu-id="f5b49-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5b49-157">RELATED LINKS</span></span>

[<span data-ttu-id="f5b49-158">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5b49-158">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f5b49-159">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5b49-159">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f5b49-160">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f5b49-160">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


