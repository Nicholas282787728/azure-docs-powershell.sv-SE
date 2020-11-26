---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323195"
---
# <span data-ttu-id="74fcb-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="74fcb-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="74fcb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="74fcb-103">Skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="74fcb-103">Creates a notification hub.</span></span>

## <span data-ttu-id="74fcb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74fcb-104">SYNTAX</span></span>

### <span data-ttu-id="74fcb-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fcb-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74fcb-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="74fcb-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fcb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74fcb-107">DESCRIPTION</span></span>
<span data-ttu-id="74fcb-108">Cmdleten **New-AzNotificationHub** skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="74fcb-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="74fcb-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="74fcb-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="74fcb-110">Meddelande NAV är ungefär likvärdiga med enskilda appar: alla dina appar har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="74fcb-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="74fcb-111">**New-AzNotificationHub-** cmdleten erbjuder två sätt att skapa en ny meddelande-hubb.</span><span class="sxs-lookup"><span data-stu-id="74fcb-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="74fcb-112">Du kan skapa en instans av **NotificationHubAttributes** -objektet och sedan konfigurera det objektet.</span><span class="sxs-lookup"><span data-stu-id="74fcb-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="74fcb-113">Du kan sedan kopiera de här egenskapsvärdena till det nya navet genom att klicka på *NotificationHubObj* -parametern.</span><span class="sxs-lookup"><span data-stu-id="74fcb-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="74fcb-114">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="74fcb-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="74fcb-115">När det används tillsammans med **New-AzNotificationHub-** cmdleten skapar det föregående JSON-exemplet ett meddelande nav med namnet ContosoNotificationHub som finns på den västra amerikanska data Center.</span><span class="sxs-lookup"><span data-stu-id="74fcb-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="74fcb-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74fcb-116">EXAMPLES</span></span>

### <span data-ttu-id="74fcb-117">Exempel 1: skapa ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="74fcb-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="74fcb-118">Det här kommandot skapar ett meddelande nav i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="74fcb-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="74fcb-119">Det nya navet tilldelas till ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="74fcb-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="74fcb-120">Du behöver inte ange ett namn eller annan konfigurations information för navet; den informationen kommer att hämtas från den indatafil som C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="74fcb-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="74fcb-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74fcb-121">PARAMETERS</span></span>

### <span data-ttu-id="74fcb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fcb-122">-DefaultProfile</span></span>
<span data-ttu-id="74fcb-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="74fcb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74fcb-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="74fcb-124">-InputFile</span></span>
<span data-ttu-id="74fcb-125">Anger sökvägen till en JSON-fil som innehåller konfigurations värden för det nya meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="74fcb-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="74fcb-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="74fcb-126">-Namespace</span></span>
<span data-ttu-id="74fcb-127">Anger namn området som meddelande navet ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="74fcb-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="74fcb-128">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="74fcb-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="74fcb-129">Aviserings NAV måste vara kopplade till ett befintligt namn område.</span><span class="sxs-lookup"><span data-stu-id="74fcb-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="74fcb-130">Cmdleten **New-AzNotificationHub** kan inte skapa ett nytt namn område.</span><span class="sxs-lookup"><span data-stu-id="74fcb-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="74fcb-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="74fcb-131">-NotificationHubObj</span></span>
<span data-ttu-id="74fcb-132">Anger det **NotificationHubAttributes** -objekt som innehåller konfigurations information för det nya navet.</span><span class="sxs-lookup"><span data-stu-id="74fcb-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="74fcb-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="74fcb-133">-ResourceGroup</span></span>
<span data-ttu-id="74fcb-134">Anger den resurs grupp som meddelande navet ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="74fcb-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="74fcb-135">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="74fcb-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="74fcb-136">Du måste använda en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="74fcb-136">You must use an existing resource group.</span></span>
<span data-ttu-id="74fcb-137">Cmdleten **New-AzNotificationHub** kan inte skapa en ny resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="74fcb-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="74fcb-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74fcb-138">-Confirm</span></span>
<span data-ttu-id="74fcb-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74fcb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74fcb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fcb-140">-WhatIf</span></span>
<span data-ttu-id="74fcb-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74fcb-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74fcb-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74fcb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74fcb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fcb-143">CommonParameters</span></span>
<span data-ttu-id="74fcb-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fcb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fcb-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fcb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fcb-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74fcb-146">INPUTS</span></span>

### <span data-ttu-id="74fcb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="74fcb-147">System.String</span></span>

## <span data-ttu-id="74fcb-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74fcb-148">OUTPUTS</span></span>

### <span data-ttu-id="74fcb-149">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="74fcb-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="74fcb-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74fcb-150">NOTES</span></span>

## <span data-ttu-id="74fcb-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74fcb-151">RELATED LINKS</span></span>

[<span data-ttu-id="74fcb-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="74fcb-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="74fcb-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="74fcb-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="74fcb-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="74fcb-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

