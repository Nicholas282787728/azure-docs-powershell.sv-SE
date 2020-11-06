---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: 45e61b79381cc9acddf4dc12c5d8e905627130a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575932"
---
# <span data-ttu-id="50398-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50398-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="50398-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50398-102">SYNOPSIS</span></span>
<span data-ttu-id="50398-103">Ställer in egenskaps värden för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="50398-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50398-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50398-104">SYNTAX</span></span>

### <span data-ttu-id="50398-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="50398-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50398-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="50398-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50398-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50398-107">DESCRIPTION</span></span>
<span data-ttu-id="50398-108">Cmdleten **set-AzureRmNotificationHub** ändrar egenskapsvärdena för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="50398-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="50398-109">Du kan ändra ett egenskaps värde för aviserings navet på två sätt.</span><span class="sxs-lookup"><span data-stu-id="50398-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="50398-110">För en kan du skapa en instans av **NotificationHubAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att det nya navet ska ha.</span><span class="sxs-lookup"><span data-stu-id="50398-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="50398-111">Det här kan du göra i .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="50398-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="50398-112">Du kan sedan kopiera de här egenskaps värdena till navet genom att klicka på *NotificationHubObj* -parametern.</span><span class="sxs-lookup"><span data-stu-id="50398-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="50398-113">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) som innehåller relevanta konfigurations värden och sedan tillämpa värdena genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="50398-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="50398-114">En JSON-fil är en textfil som använder syntax av följande slag:</span><span class="sxs-lookup"><span data-stu-id="50398-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="50398-115">{</span><span class="sxs-lookup"><span data-stu-id="50398-115">{</span></span>  
    <span data-ttu-id="50398-116">"Namn": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="50398-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="50398-117">"Plats": "västra USA",</span><span class="sxs-lookup"><span data-stu-id="50398-117">"Location": "West US",</span></span>  
<span data-ttu-id="50398-118">}</span><span class="sxs-lookup"><span data-stu-id="50398-118">}</span></span>

<span data-ttu-id="50398-119">När det används tillsammans med cmdleten **set-AzureRmNotificationHub** anger det föregående JSON-exemplet plats värde för ett meddelande nav med namnet ContosoNotificationHub till West-US.</span><span class="sxs-lookup"><span data-stu-id="50398-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="50398-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50398-120">EXAMPLES</span></span>

### <span data-ttu-id="50398-121">Exempel 1: ändra egenskaps värden för ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="50398-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="50398-122">Det här kommandot ändrar egenskapsvärdena för ett meddelande nav i ContosoNamespace-namnområdet och tilldelat det till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="50398-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="50398-123">Egenskapsvärdena, samt namnet på navet som ska ändras, anges inte i kommandot.</span><span class="sxs-lookup"><span data-stu-id="50398-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="50398-124">I stället lagras informationen i C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="50398-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="50398-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50398-125">PARAMETERS</span></span>

### <span data-ttu-id="50398-126">-Force</span><span class="sxs-lookup"><span data-stu-id="50398-126">-Force</span></span>
<span data-ttu-id="50398-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50398-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="50398-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="50398-128">-InputFile</span></span>
<span data-ttu-id="50398-129">Anger sökvägen till en JSON-fil som innehåller konfigurations information för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="50398-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="50398-130">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="50398-130">-Namespace</span></span>
<span data-ttu-id="50398-131">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="50398-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="50398-132">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="50398-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="50398-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="50398-133">-NotificationHubObj</span></span>
<span data-ttu-id="50398-134">Anger det **NotificationHubAttributes** -objekt som innehåller konfigurations information för navet som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="50398-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50398-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50398-135">-ResourceGroup</span></span>
<span data-ttu-id="50398-136">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="50398-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="50398-137">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="50398-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="50398-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50398-138">-Confirm</span></span>
<span data-ttu-id="50398-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50398-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50398-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50398-140">-WhatIf</span></span>
<span data-ttu-id="50398-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50398-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50398-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50398-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50398-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50398-143">-DefaultProfile</span></span>
<span data-ttu-id="50398-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50398-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50398-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50398-145">CommonParameters</span></span>
<span data-ttu-id="50398-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50398-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50398-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50398-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50398-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50398-148">INPUTS</span></span>

## <span data-ttu-id="50398-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50398-149">OUTPUTS</span></span>

### <span data-ttu-id="50398-150">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="50398-150">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="50398-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50398-151">NOTES</span></span>

## <span data-ttu-id="50398-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50398-152">RELATED LINKS</span></span>

[<span data-ttu-id="50398-153">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50398-153">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="50398-154">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50398-154">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="50398-155">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50398-155">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)


