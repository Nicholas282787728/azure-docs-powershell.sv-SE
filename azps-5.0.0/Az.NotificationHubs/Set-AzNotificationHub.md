---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 3dc4a81731f42ce6a27ae5d23fb7c81af76cf789
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323171"
---
# <span data-ttu-id="e485c-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e485c-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="e485c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e485c-102">SYNOPSIS</span></span>
<span data-ttu-id="e485c-103">Ställer in egenskaps värden för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e485c-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="e485c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e485c-104">SYNTAX</span></span>

### <span data-ttu-id="e485c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e485c-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e485c-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="e485c-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e485c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e485c-107">DESCRIPTION</span></span>
<span data-ttu-id="e485c-108">Cmdleten **set-AzNotificationHub** ändrar egenskapsvärdena för ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e485c-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="e485c-109">Du kan ändra ett egenskaps värde för aviserings navet på två sätt.</span><span class="sxs-lookup"><span data-stu-id="e485c-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="e485c-110">För en kan du skapa en instans av **NotificationHubAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att det nya navet ska ha.</span><span class="sxs-lookup"><span data-stu-id="e485c-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="e485c-111">Det här kan du göra i .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e485c-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="e485c-112">Du kan sedan kopiera de här egenskaps värdena till navet genom att klicka på *NotificationHubObj* -parametern.</span><span class="sxs-lookup"><span data-stu-id="e485c-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="e485c-113">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) som innehåller relevanta konfigurations värden och sedan tillämpa värdena genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="e485c-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="e485c-114">En JSON-fil är en textfil som använder syntax av följande slag: {</span><span class="sxs-lookup"><span data-stu-id="e485c-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="e485c-115">"Namn": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="e485c-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="e485c-116">"Plats": "västra USA",</span><span class="sxs-lookup"><span data-stu-id="e485c-116">"Location": "West US",</span></span>  
<span data-ttu-id="e485c-117">} När det används tillsammans med cmdleten **set-AzNotificationHub** anger det föregående JSON-exemplet plats värde för ett meddelande nav med namnet ContosoNotificationHub till West-US.</span><span class="sxs-lookup"><span data-stu-id="e485c-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="e485c-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e485c-118">EXAMPLES</span></span>

### <span data-ttu-id="e485c-119">Exempel 1: ändra egenskaps värden för ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="e485c-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="e485c-120">Det här kommandot ändrar egenskapsvärdena för ett meddelande nav i ContosoNamespace-namnområdet och tilldelat det till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="e485c-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="e485c-121">Egenskapsvärdena, samt namnet på navet som ska ändras, anges inte i kommandot.</span><span class="sxs-lookup"><span data-stu-id="e485c-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="e485c-122">I stället lagras informationen i C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="e485c-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="e485c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e485c-123">PARAMETERS</span></span>

### <span data-ttu-id="e485c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e485c-124">-DefaultProfile</span></span>
<span data-ttu-id="e485c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e485c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e485c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e485c-126">-Force</span></span>
<span data-ttu-id="e485c-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e485c-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e485c-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e485c-128">-InputFile</span></span>
<span data-ttu-id="e485c-129">Anger sökvägen till en JSON-fil som innehåller konfigurations information för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="e485c-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="e485c-130">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e485c-130">-Namespace</span></span>
<span data-ttu-id="e485c-131">Anger namn området som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="e485c-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="e485c-132">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="e485c-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e485c-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="e485c-133">-NotificationHubObj</span></span>
<span data-ttu-id="e485c-134">Anger det **NotificationHubAttributes** -objekt som innehåller konfigurations information för navet som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="e485c-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e485c-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e485c-135">-ResourceGroup</span></span>
<span data-ttu-id="e485c-136">Anger den resurs grupp som meddelande navet tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="e485c-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e485c-137">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="e485c-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e485c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e485c-138">-Confirm</span></span>
<span data-ttu-id="e485c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e485c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e485c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e485c-140">-WhatIf</span></span>
<span data-ttu-id="e485c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e485c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e485c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e485c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e485c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e485c-143">CommonParameters</span></span>
<span data-ttu-id="e485c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e485c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e485c-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e485c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e485c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e485c-146">INPUTS</span></span>

### <span data-ttu-id="e485c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e485c-147">System.String</span></span>

## <span data-ttu-id="e485c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e485c-148">OUTPUTS</span></span>

### <span data-ttu-id="e485c-149">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e485c-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="e485c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e485c-150">NOTES</span></span>

## <span data-ttu-id="e485c-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e485c-151">RELATED LINKS</span></span>

[<span data-ttu-id="e485c-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e485c-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="e485c-153">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e485c-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="e485c-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e485c-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

