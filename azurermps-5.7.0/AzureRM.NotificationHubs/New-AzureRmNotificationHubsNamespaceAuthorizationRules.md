---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582035"
---
# <span data-ttu-id="9a5d4-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9a5d4-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="9a5d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5d4-103">Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a5d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a5d4-104">SYNTAX</span></span>

### <span data-ttu-id="9a5d4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a5d4-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5d4-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a5d4-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a5d4-107">DESCRIPTION</span></span>
<span data-ttu-id="9a5d4-108">Cmdleten **New-AzureRmNotificationHubsNamespaceAuthorizationRules** skapar en auktoriseringsregel för delad åtkomst-signatur (SAS) och tilldelar den till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="9a5d4-109">Auktoriseringsregler hanterar användar rättigheter till namn området och aviserings nav som ingår i namn området.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="9a5d4-110">Denna cmdlet ger två sätt att skapa en ny auktoriseringsregel och tilldela den till ett namn område.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="9a5d4-111">Du kan skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att den nya regeln ska ha.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="9a5d4-112">Det här kan du göra med .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="9a5d4-113">Du kan sedan kopiera de här egenskaps värdena till den nya regeln genom att använda parametern *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="9a5d4-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="9a5d4-114">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="9a5d4-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="9a5d4-115">En JSON-fil är en textfil som använder syntax av följande slag:</span><span class="sxs-lookup"><span data-stu-id="9a5d4-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="9a5d4-116">{</span><span class="sxs-lookup"><span data-stu-id="9a5d4-116">{</span></span>  
    <span data-ttu-id="9a5d4-117">"Namn": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="9a5d4-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="9a5d4-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="9a5d4-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="9a5d4-119">"Rättigheter": \[</span><span class="sxs-lookup"><span data-stu-id="9a5d4-119">"Rights": \[</span></span>  
        <span data-ttu-id="9a5d4-120">"Lyssna",</span><span class="sxs-lookup"><span data-stu-id="9a5d4-120">"Listen",</span></span>  
        <span data-ttu-id="9a5d4-121">Bifoga</span><span class="sxs-lookup"><span data-stu-id="9a5d4-121">"Send"</span></span>  
    \]  
<span data-ttu-id="9a5d4-122">}</span><span class="sxs-lookup"><span data-stu-id="9a5d4-122">}</span></span>

<span data-ttu-id="9a5d4-123">När det används tillsammans med **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet skapar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule som gör att användarna lyssnar och skickar rättigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="9a5d4-124">*PrimaryKey* som används för inloggningsautentisering kan skapas slumpmässigt med hjälp av följande Windows PowerShell-kommando:</span><span class="sxs-lookup"><span data-stu-id="9a5d4-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="9a5d4-125">\[Konvertera \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-slump-minimum 0-maximalt 255)}))</span><span class="sxs-lookup"><span data-stu-id="9a5d4-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="9a5d4-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a5d4-126">EXAMPLES</span></span>

### <span data-ttu-id="9a5d4-127">Exempel 1: skapa en auktoriseringsregel och tilldela den till ett namn område</span><span class="sxs-lookup"><span data-stu-id="9a5d4-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="9a5d4-128">Det här kommandot skapar en auktoriseringsregel och tilldelar regeln till namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="9a5d4-129">När du skapar den här regeln måste du ange lämpligt namnrymd och resurs gruppen som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="9a5d4-130">Men du behöver inte ange någon information om regeln själv: regel informationen kommer att hämtas från den indatafil som C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="9a5d4-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a5d4-131">PARAMETERS</span></span>

### <span data-ttu-id="9a5d4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5d4-132">-DefaultProfile</span></span>
<span data-ttu-id="9a5d4-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9a5d4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-134">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9a5d4-134">-InputFile</span></span>
<span data-ttu-id="9a5d4-135">Anger sökvägen till en JSON-fil som innehåller konfigurations information för den nya auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-135">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-136">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9a5d4-136">-Namespace</span></span>
<span data-ttu-id="9a5d4-137">Anger namn området som auktoriseringsregler ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-137">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="9a5d4-138">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-138">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="9a5d4-139">De nya reglerna måste kopplas till ett befintligt namn område.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-139">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="9a5d4-140">Cmdleten **New-AzureRmNotificationHubsNamespaceAuthorizationRules** kan inte skapa ett nytt namn område.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-140">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-141">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a5d4-141">-ResourceGroup</span></span>
<span data-ttu-id="9a5d4-142">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-142">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="9a5d4-143">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-143">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="9a5d4-144">Du måste använda en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-144">You must use an existing resource group.</span></span>
<span data-ttu-id="9a5d4-145">Denna cmdlet kan inte skapa en ny resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-145">This cmdlet cannot create a new resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-146">-SASRule</span><span class="sxs-lookup"><span data-stu-id="9a5d4-146">-SASRule</span></span>
<span data-ttu-id="9a5d4-147">Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de nya reglerna.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-147">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a5d4-148">-Confirm</span></span>
<span data-ttu-id="9a5d4-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5d4-150">-WhatIf</span></span>
<span data-ttu-id="9a5d4-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a5d4-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5d4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5d4-153">CommonParameters</span></span>
<span data-ttu-id="9a5d4-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5d4-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5d4-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5d4-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a5d4-156">INPUTS</span></span>

### <span data-ttu-id="9a5d4-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a5d4-157">None</span></span>
<span data-ttu-id="9a5d4-158">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9a5d4-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a5d4-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a5d4-159">OUTPUTS</span></span>

### <span data-ttu-id="9a5d4-160">Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9a5d4-160">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9a5d4-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a5d4-161">NOTES</span></span>

## <span data-ttu-id="9a5d4-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a5d4-162">RELATED LINKS</span></span>

[<span data-ttu-id="9a5d4-163">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9a5d4-163">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="9a5d4-164">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9a5d4-164">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="9a5d4-165">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9a5d4-165">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


