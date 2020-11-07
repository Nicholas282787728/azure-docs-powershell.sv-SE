---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 5fb832a7a72f0b201ea20660a5e94e67d470ba95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747604"
---
# <span data-ttu-id="b35f5-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b35f5-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b35f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b35f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b35f5-103">Anger auktoriseringsregler för ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="b35f5-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="b35f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b35f5-104">SYNTAX</span></span>

### <span data-ttu-id="b35f5-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35f5-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b35f5-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35f5-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b35f5-107">DESCRIPTION</span></span>
<span data-ttu-id="b35f5-108">Cmdleten **set-AzNotificationHubsNamespaceAuthorizationRule** ändrar en auktoriseringsregel för en säkerhets Association för en delad Access-signatur som har tilldelats ett namn område för ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="b35f5-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="b35f5-109">Auktoriseringsregler hanterar användar rättigheter till namn området och aviserings hubbarna i namn området.</span><span class="sxs-lookup"><span data-stu-id="b35f5-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="b35f5-110">Denna cmdlet erbjuder två sätt att ändra en auktoriseringsregel som tilldelats ett namn område.</span><span class="sxs-lookup"><span data-stu-id="b35f5-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="b35f5-111">För en kan du skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="b35f5-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="b35f5-112">Du kan använda .NET Framework för att åstadkomma detta.</span><span class="sxs-lookup"><span data-stu-id="b35f5-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="b35f5-113">Du kan sedan kopiera de här egenskaps värdena till regeln via parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="b35f5-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="b35f5-114">Alternativt kan du skapa en JSON-fil (JavaScript Object Notation) med relevanta konfigurations värden och sedan tillämpa dessa värden genom *InputFile* -parametern.</span><span class="sxs-lookup"><span data-stu-id="b35f5-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="b35f5-115">En JSON-fil är en textfil som använder syntax som liknar den här: {</span><span class="sxs-lookup"><span data-stu-id="b35f5-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="b35f5-116">"Namn": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="b35f5-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="b35f5-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="b35f5-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="b35f5-118">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="b35f5-118">"Rights": \[</span></span>  
        <span data-ttu-id="b35f5-119">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="b35f5-119">"Listen",</span></span>  
        <span data-ttu-id="b35f5-120">Bifoga</span><span class="sxs-lookup"><span data-stu-id="b35f5-120">"Send"</span></span>  
    \]  
<span data-ttu-id="b35f5-121">} När det används tillsammans med cmdleten **set-AzNotificationHubsNamespaceAuthorizationRule** ändrar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användarna behörighet att avlyssna och skicka rättigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="b35f5-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="b35f5-122">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b35f5-122">EXAMPLES</span></span>

### <span data-ttu-id="b35f5-123">Exempel 1: ändra en auktoriseringsregel som tilldelats ett namn område</span><span class="sxs-lookup"><span data-stu-id="b35f5-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="b35f5-124">Det här kommandot ändrar en auktoriseringsregel som tilldelats namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="b35f5-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="b35f5-125">Du måste ange den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="b35f5-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="b35f5-126">Information om auktoriseringsregeln är inte inkluderad i själva kommandot.</span><span class="sxs-lookup"><span data-stu-id="b35f5-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="b35f5-127">I stället hämtas den informationen från indatafilen C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="b35f5-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="b35f5-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b35f5-128">PARAMETERS</span></span>

### <span data-ttu-id="b35f5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35f5-129">-DefaultProfile</span></span>
<span data-ttu-id="b35f5-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b35f5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b35f5-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b35f5-131">-Force</span></span>
<span data-ttu-id="b35f5-132">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b35f5-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b35f5-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b35f5-133">-InputFile</span></span>
<span data-ttu-id="b35f5-134">Anger sökvägen till en JSON-fil med konfigurations information för den nya regeln.</span><span class="sxs-lookup"><span data-stu-id="b35f5-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="b35f5-135">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b35f5-135">-Namespace</span></span>
<span data-ttu-id="b35f5-136">Anger namn området som innehåller de auktoriseringsregler som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b35f5-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="b35f5-137">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="b35f5-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b35f5-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b35f5-138">-ResourceGroup</span></span>
<span data-ttu-id="b35f5-139">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b35f5-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b35f5-140">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="b35f5-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b35f5-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="b35f5-141">-SASRule</span></span>
<span data-ttu-id="b35f5-142">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de auktoriseringsregler som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b35f5-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b35f5-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b35f5-143">-Confirm</span></span>
<span data-ttu-id="b35f5-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b35f5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35f5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35f5-145">-WhatIf</span></span>
<span data-ttu-id="b35f5-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b35f5-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b35f5-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b35f5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35f5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35f5-148">CommonParameters</span></span>
<span data-ttu-id="b35f5-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35f5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35f5-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b35f5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35f5-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b35f5-151">INPUTS</span></span>

### <span data-ttu-id="b35f5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b35f5-152">System.String</span></span>

## <span data-ttu-id="b35f5-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b35f5-153">OUTPUTS</span></span>

### <span data-ttu-id="b35f5-154">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b35f5-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b35f5-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b35f5-155">NOTES</span></span>

## <span data-ttu-id="b35f5-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b35f5-156">RELATED LINKS</span></span>

[<span data-ttu-id="b35f5-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b35f5-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="b35f5-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b35f5-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="b35f5-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b35f5-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


