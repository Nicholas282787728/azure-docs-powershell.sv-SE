---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262475"
---
# <span data-ttu-id="7abbb-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7abbb-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7abbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7abbb-102">SYNOPSIS</span></span>
<span data-ttu-id="7abbb-103">Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="7abbb-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="7abbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7abbb-104">SYNTAX</span></span>

### <span data-ttu-id="7abbb-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7abbb-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abbb-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7abbb-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7abbb-107">DESCRIPTION</span></span>
<span data-ttu-id="7abbb-108">Cmdleten **New-AzNotificationHubsNamespaceAuthorizationRule** skapar en auktoriseringsregel för delad åtkomst-signatur (SAS) och tilldelar den till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="7abbb-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="7abbb-109">Auktoriseringsregler hanterar användar rättigheter till namn området och aviserings nav som ingår i namn området.</span><span class="sxs-lookup"><span data-stu-id="7abbb-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="7abbb-110">Denna cmdlet ger två sätt att skapa en ny auktoriseringsregel och tilldela den till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="7abbb-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="7abbb-111">Du kan skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att den nya regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="7abbb-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="7abbb-112">Det här kan du göra med .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7abbb-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="7abbb-113">Du kan sedan kopiera de här egenskaps värdena till den nya regeln genom att använda parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="7abbb-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="7abbb-114">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="7abbb-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="7abbb-115">En JSON-fil är en textfil som använder syntax av följande slag: {</span><span class="sxs-lookup"><span data-stu-id="7abbb-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="7abbb-116">"Namn": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="7abbb-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7abbb-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="7abbb-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7abbb-118">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="7abbb-118">"Rights": \[</span></span>  
        <span data-ttu-id="7abbb-119">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="7abbb-119">"Listen",</span></span>  
        <span data-ttu-id="7abbb-120">Bifoga</span><span class="sxs-lookup"><span data-stu-id="7abbb-120">"Send"</span></span>  
    \]  
<span data-ttu-id="7abbb-121">} När det används tillsammans med **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet skapar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule som gör att användarna lyssnar och skickar rättigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="7abbb-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="7abbb-122">*PrimaryKey* som används för inloggningsautentisering kan skapas slumpmässigt med hjälp av följande Windows PowerShell-kommando: \[ konvertera \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-slump-minimum 0-maximalt 255)}))</span><span class="sxs-lookup"><span data-stu-id="7abbb-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="7abbb-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7abbb-123">EXAMPLES</span></span>

### <span data-ttu-id="7abbb-124">Exempel 1: skapa en auktoriseringsregel och tilldela den till ett namn område</span><span class="sxs-lookup"><span data-stu-id="7abbb-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="7abbb-125">Det här kommandot skapar en auktoriseringsregel och tilldelar regeln till namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="7abbb-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="7abbb-126">När du skapar den här regeln måste du ange lämpligt namnrymd och resurs gruppen som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="7abbb-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="7abbb-127">Men du behöver inte ange någon information om regeln själv: regel informationen kommer att hämtas från den indatafil som C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="7abbb-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="7abbb-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7abbb-128">PARAMETERS</span></span>

### <span data-ttu-id="7abbb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abbb-129">-DefaultProfile</span></span>
<span data-ttu-id="7abbb-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7abbb-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7abbb-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7abbb-131">-InputFile</span></span>
<span data-ttu-id="7abbb-132">Anger sökvägen till en JSON-fil som innehåller konfigurations information för den nya auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="7abbb-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="7abbb-133">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="7abbb-133">-Namespace</span></span>
<span data-ttu-id="7abbb-134">Anger namn området som auktoriseringsregler ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="7abbb-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="7abbb-135">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="7abbb-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="7abbb-136">De nya reglerna måste kopplas till ett befintligt namn område.</span><span class="sxs-lookup"><span data-stu-id="7abbb-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="7abbb-137">Cmdleten **New-AzNotificationHubsNamespaceAuthorizationRule** kan inte skapa ett nytt namn område.</span><span class="sxs-lookup"><span data-stu-id="7abbb-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="7abbb-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7abbb-138">-ResourceGroup</span></span>
<span data-ttu-id="7abbb-139">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="7abbb-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7abbb-140">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="7abbb-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="7abbb-141">Du måste använda en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7abbb-141">You must use an existing resource group.</span></span>
<span data-ttu-id="7abbb-142">Denna cmdlet kan inte skapa en ny resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7abbb-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="7abbb-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7abbb-143">-SASRule</span></span>
<span data-ttu-id="7abbb-144">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de nya reglerna.</span><span class="sxs-lookup"><span data-stu-id="7abbb-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="7abbb-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7abbb-145">-Confirm</span></span>
<span data-ttu-id="7abbb-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7abbb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abbb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abbb-147">-WhatIf</span></span>
<span data-ttu-id="7abbb-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7abbb-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7abbb-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7abbb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abbb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abbb-150">CommonParameters</span></span>
<span data-ttu-id="7abbb-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abbb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abbb-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abbb-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abbb-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7abbb-153">INPUTS</span></span>

### <span data-ttu-id="7abbb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7abbb-154">System.String</span></span>

## <span data-ttu-id="7abbb-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7abbb-155">OUTPUTS</span></span>

### <span data-ttu-id="7abbb-156">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7abbb-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7abbb-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7abbb-157">NOTES</span></span>

## <span data-ttu-id="7abbb-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7abbb-158">RELATED LINKS</span></span>

[<span data-ttu-id="7abbb-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7abbb-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7abbb-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7abbb-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7abbb-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7abbb-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


