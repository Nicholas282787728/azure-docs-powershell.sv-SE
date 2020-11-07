---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 501182c9307319dd84c61a14c2243d49cdb00541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577592"
---
# <span data-ttu-id="09b19-101">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="09b19-101">New-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="09b19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09b19-102">SYNOPSIS</span></span>
<span data-ttu-id="09b19-103">Skapar ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="09b19-103">Creates a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09b19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09b19-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tags] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09b19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09b19-105">DESCRIPTION</span></span>
<span data-ttu-id="09b19-106">Cmdleten **New-AzureRmNotificationHubsNamespace** skapar ett namn område för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="09b19-106">The **New-AzureRmNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>

<span data-ttu-id="09b19-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="09b19-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="09b19-108">Du måste ha minst ett namn område för aviserings navet.</span><span class="sxs-lookup"><span data-stu-id="09b19-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="09b19-109">Ett enskilt namn område kan House flera nav.</span><span class="sxs-lookup"><span data-stu-id="09b19-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="09b19-110">Du kan ha flera namn utrymmen för att organisera dina nav eller för att ge specifika enskilda personer tillstånd att hantera en viss delmängd av dina nav.</span><span class="sxs-lookup"><span data-stu-id="09b19-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>

<span data-ttu-id="09b19-111">Om du vill skapa ett namn område kontrollerar du att du anger ett unikt namn för namn området. Ange data Center där namn området ska placeras; och ange den resurs grupp som namn området ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="09b19-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="09b19-112">När namn området har skapats kan du använda New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet för att tilldela auktoriseringsregler till namn området.</span><span class="sxs-lookup"><span data-stu-id="09b19-112">After the namespace has been created you can use the New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="09b19-113">Auktoriseringsregler används för att hantera behörigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="09b19-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="09b19-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09b19-114">EXAMPLES</span></span>

### <span data-ttu-id="09b19-115">Exempel 1: skapa ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="09b19-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="09b19-116">Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="09b19-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="09b19-117">Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="09b19-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="09b19-118">Exempel 2: skapa ett huvud meddelande med Taggar</span><span class="sxs-lookup"><span data-stu-id="09b19-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="09b19-119">Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="09b19-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="09b19-120">Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="09b19-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="09b19-121">Dessutom skapar det här kommandot en tagg med namnet Audience och värdet PartnerOrganizations och är tilldelat till namn området.</span><span class="sxs-lookup"><span data-stu-id="09b19-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="09b19-122">Då visas namn området när du filtrerar objekt där mål grupps koden är inställd på PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="09b19-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="09b19-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09b19-123">PARAMETERS</span></span>

### <span data-ttu-id="09b19-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="09b19-124">-Location</span></span>
<span data-ttu-id="09b19-125">Anger visnings namnet på det data Center som ska vara värd för namn området.</span><span class="sxs-lookup"><span data-stu-id="09b19-125">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="09b19-126">Även om du kan ange den här parametern till vilken plats som helst, för optimal prestanda kan du använda ett Data Center nära de flesta av dina användare.</span><span class="sxs-lookup"><span data-stu-id="09b19-126">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="09b19-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="09b19-127">-Namespace</span></span>
<span data-ttu-id="09b19-128">Anger namnet på det nya namn området.</span><span class="sxs-lookup"><span data-stu-id="09b19-128">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="09b19-129">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="09b19-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="09b19-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09b19-130">-ResourceGroup</span></span>
<span data-ttu-id="09b19-131">Anger den resurs grupp som namn området ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="09b19-131">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="09b19-132">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och administration.</span><span class="sxs-lookup"><span data-stu-id="09b19-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="09b19-133">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="09b19-133">-SkuTier</span></span>
<span data-ttu-id="09b19-134">SKU-nivån i namn området</span><span class="sxs-lookup"><span data-stu-id="09b19-134">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b19-135">-Taggar</span><span class="sxs-lookup"><span data-stu-id="09b19-135">-Tags</span></span>
<span data-ttu-id="09b19-136">Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.</span><span class="sxs-lookup"><span data-stu-id="09b19-136">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="09b19-137">Funktionen Taggar liknar nyckelord och fungerar i en distribution.</span><span class="sxs-lookup"><span data-stu-id="09b19-137">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="09b19-138">Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09b19-138">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="09b19-139">En enskild tagg består av två delar: *namnet* och, om du vill, *värdet*.</span><span class="sxs-lookup"><span data-stu-id="09b19-139">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="09b19-140">I avdelning: det är alltså namnet avdelning och taggnamnet det.</span><span class="sxs-lookup"><span data-stu-id="09b19-140">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="09b19-141">Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="09b19-141">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b19-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09b19-142">-Confirm</span></span>
<span data-ttu-id="09b19-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09b19-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09b19-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09b19-144">-WhatIf</span></span>
<span data-ttu-id="09b19-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09b19-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09b19-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09b19-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09b19-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b19-147">-DefaultProfile</span></span>
<span data-ttu-id="09b19-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09b19-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b19-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b19-149">CommonParameters</span></span>
<span data-ttu-id="09b19-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b19-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b19-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b19-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b19-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09b19-152">INPUTS</span></span>

## <span data-ttu-id="09b19-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09b19-153">OUTPUTS</span></span>

### <span data-ttu-id="09b19-154">Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="09b19-154">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="09b19-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09b19-155">NOTES</span></span>

## <span data-ttu-id="09b19-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09b19-156">RELATED LINKS</span></span>

[<span data-ttu-id="09b19-157">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="09b19-157">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="09b19-158">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="09b19-158">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="09b19-159">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="09b19-159">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)

