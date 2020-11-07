---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: c0a3e2231ef0f27689a08b9199876d04c4e68b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756014"
---
# <span data-ttu-id="aed26-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="aed26-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="aed26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aed26-102">SYNOPSIS</span></span>
<span data-ttu-id="aed26-103">Skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="aed26-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aed26-104">SYNTAX</span></span>

### <span data-ttu-id="aed26-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="aed26-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aed26-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="aed26-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed26-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aed26-107">DESCRIPTION</span></span>
<span data-ttu-id="aed26-108">Cmdleten **New-AzureRmNotificationHub** skapar ett meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="aed26-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="aed26-109">Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.</span><span class="sxs-lookup"><span data-stu-id="aed26-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="aed26-110">Meddelande NAV är ungefär likvärdiga med enskilda appar: alla dina appar har vanligt vis sin egen meddelande hubb.</span><span class="sxs-lookup"><span data-stu-id="aed26-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="aed26-111">**New-AzureRmNotificationHub-** cmdleten erbjuder två sätt att skapa en ny meddelande-hubb.</span><span class="sxs-lookup"><span data-stu-id="aed26-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="aed26-112">Du kan skapa en instans av **NotificationHubAttributes** -objektet och sedan konfigurera det objektet.</span><span class="sxs-lookup"><span data-stu-id="aed26-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="aed26-113">Du kan sedan kopiera de här egenskapsvärdena till det nya navet genom att klicka på *NotificationHubObj* -parametern.</span><span class="sxs-lookup"><span data-stu-id="aed26-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="aed26-114">Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="aed26-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="aed26-115">När det används tillsammans med **New-AzureRmNotificationHub-** cmdleten skapar det föregående JSON-exemplet ett meddelande nav med namnet ContosoNotificationHub som finns på den västra amerikanska data Center.</span><span class="sxs-lookup"><span data-stu-id="aed26-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="aed26-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aed26-116">EXAMPLES</span></span>

### <span data-ttu-id="aed26-117">Exempel 1: skapa ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="aed26-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="aed26-118">Det här kommandot skapar ett meddelande nav i namn området ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="aed26-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="aed26-119">Det nya navet tilldelas till ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="aed26-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="aed26-120">Du behöver inte ange ett namn eller annan konfigurations information för navet; den informationen kommer att hämtas från den indatafil som C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="aed26-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="aed26-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aed26-121">PARAMETERS</span></span>

### <span data-ttu-id="aed26-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed26-122">-DefaultProfile</span></span>
<span data-ttu-id="aed26-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aed26-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aed26-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="aed26-124">-InputFile</span></span>
<span data-ttu-id="aed26-125">Anger sökvägen till en JSON-fil som innehåller konfigurations värden för det nya meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="aed26-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="aed26-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="aed26-126">-Namespace</span></span>
<span data-ttu-id="aed26-127">Anger namn området som meddelande navet ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="aed26-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="aed26-128">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="aed26-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="aed26-129">Aviserings NAV måste vara kopplade till ett befintligt namn område.</span><span class="sxs-lookup"><span data-stu-id="aed26-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="aed26-130">Cmdleten **New-AzureRmNotificationHub** kan inte skapa ett nytt namn område.</span><span class="sxs-lookup"><span data-stu-id="aed26-130">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="aed26-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="aed26-131">-NotificationHubObj</span></span>
<span data-ttu-id="aed26-132">Anger det **NotificationHubAttributes** -objekt som innehåller konfigurations information för det nya navet.</span><span class="sxs-lookup"><span data-stu-id="aed26-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="aed26-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aed26-133">-ResourceGroup</span></span>
<span data-ttu-id="aed26-134">Anger den resurs grupp som meddelande navet ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="aed26-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="aed26-135">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="aed26-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="aed26-136">Du måste använda en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="aed26-136">You must use an existing resource group.</span></span>
<span data-ttu-id="aed26-137">Cmdleten **New-AzureRmNotificationHub** kan inte skapa en ny resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="aed26-137">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="aed26-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aed26-138">-Confirm</span></span>
<span data-ttu-id="aed26-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aed26-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed26-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed26-140">-WhatIf</span></span>
<span data-ttu-id="aed26-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aed26-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aed26-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aed26-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed26-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed26-143">CommonParameters</span></span>
<span data-ttu-id="aed26-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed26-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed26-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed26-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed26-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aed26-146">INPUTS</span></span>

### <span data-ttu-id="aed26-147">System. String</span><span class="sxs-lookup"><span data-stu-id="aed26-147">System.String</span></span>

## <span data-ttu-id="aed26-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aed26-148">OUTPUTS</span></span>

### <span data-ttu-id="aed26-149">Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="aed26-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="aed26-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aed26-150">NOTES</span></span>

## <span data-ttu-id="aed26-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aed26-151">RELATED LINKS</span></span>

[<span data-ttu-id="aed26-152">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="aed26-152">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="aed26-153">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="aed26-153">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="aed26-154">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="aed26-154">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


