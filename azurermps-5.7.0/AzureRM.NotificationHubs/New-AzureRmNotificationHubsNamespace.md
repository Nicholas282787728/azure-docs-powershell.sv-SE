---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 504fe8b5aad0e2e028bf27cf08a29fd335edfa33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577114"
---
# <span data-ttu-id="60973-101">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="60973-101">New-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="60973-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60973-102">SYNOPSIS</span></span>
<span data-ttu-id="60973-103">Skapar ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="60973-103">Creates a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60973-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60973-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60973-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60973-105">DESCRIPTION</span></span>
<span data-ttu-id="60973-106">Cmdleten **New-AzureRmNotificationHubsNamespace** skapar ett namn område för meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="60973-106">The **New-AzureRmNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>

<span data-ttu-id="60973-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="60973-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="60973-108">Du måste ha minst ett namn område för aviserings navet.</span><span class="sxs-lookup"><span data-stu-id="60973-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="60973-109">Ett enskilt namn område kan House flera nav.</span><span class="sxs-lookup"><span data-stu-id="60973-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="60973-110">Du kan ha flera namn utrymmen för att organisera dina nav eller för att ge specifika enskilda personer tillstånd att hantera en viss delmängd av dina nav.</span><span class="sxs-lookup"><span data-stu-id="60973-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>

<span data-ttu-id="60973-111">Om du vill skapa ett namn område kontrollerar du att du anger ett unikt namn för namn området. Ange data Center där namn området ska placeras; och ange den resurs grupp som namn området ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="60973-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="60973-112">När namn området har skapats kan du använda New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet för att tilldela auktoriseringsregler till namn området.</span><span class="sxs-lookup"><span data-stu-id="60973-112">After the namespace has been created you can use the New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="60973-113">Auktoriseringsregler används för att hantera behörigheter till namn området.</span><span class="sxs-lookup"><span data-stu-id="60973-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="60973-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60973-114">EXAMPLES</span></span>

### <span data-ttu-id="60973-115">Exempel 1: skapa ett meddelande nav</span><span class="sxs-lookup"><span data-stu-id="60973-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="60973-116">Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="60973-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="60973-117">Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="60973-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="60973-118">Exempel 2: skapa ett huvud meddelande med Taggar</span><span class="sxs-lookup"><span data-stu-id="60973-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="60973-119">Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="60973-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="60973-120">Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="60973-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="60973-121">Dessutom skapar det här kommandot en tagg med namnet Audience och värdet PartnerOrganizations och är tilldelat till namn området.</span><span class="sxs-lookup"><span data-stu-id="60973-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="60973-122">Då visas namn området när du filtrerar objekt där mål grupps koden är inställd på PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="60973-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="60973-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60973-123">PARAMETERS</span></span>

### <span data-ttu-id="60973-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60973-124">-DefaultProfile</span></span>
<span data-ttu-id="60973-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="60973-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60973-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="60973-126">-Location</span></span>
<span data-ttu-id="60973-127">Anger visnings namnet på det data Center som ska vara värd för namn området.</span><span class="sxs-lookup"><span data-stu-id="60973-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="60973-128">Även om du kan ange den här parametern till vilken plats som helst, för optimal prestanda kan du använda ett Data Center nära de flesta av dina användare.</span><span class="sxs-lookup"><span data-stu-id="60973-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60973-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="60973-129">-Namespace</span></span>
<span data-ttu-id="60973-130">Anger namnet på det nya namn området.</span><span class="sxs-lookup"><span data-stu-id="60973-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="60973-131">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="60973-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="60973-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60973-132">-ResourceGroup</span></span>
<span data-ttu-id="60973-133">Anger den resurs grupp som namn området ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="60973-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="60973-134">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och administration.</span><span class="sxs-lookup"><span data-stu-id="60973-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="60973-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="60973-135">-SkuTier</span></span>
<span data-ttu-id="60973-136">SKU-nivån i namn området</span><span class="sxs-lookup"><span data-stu-id="60973-136">Sku tier of the namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60973-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="60973-137">-Tag</span></span>
<span data-ttu-id="60973-138">Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.</span><span class="sxs-lookup"><span data-stu-id="60973-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="60973-139">Funktionen Taggar liknar nyckelord och fungerar i en distribution.</span><span class="sxs-lookup"><span data-stu-id="60973-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="60973-140">Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="60973-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="60973-141">En enskild tagg består av två delar: *namnet* och, om du vill, *värdet*.</span><span class="sxs-lookup"><span data-stu-id="60973-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="60973-142">I avdelning: det är alltså namnet avdelning och taggnamnet det.</span><span class="sxs-lookup"><span data-stu-id="60973-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="60973-143">Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="60973-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60973-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60973-144">-Confirm</span></span>
<span data-ttu-id="60973-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60973-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60973-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60973-146">-WhatIf</span></span>
<span data-ttu-id="60973-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60973-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60973-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60973-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60973-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60973-149">CommonParameters</span></span>
<span data-ttu-id="60973-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60973-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60973-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60973-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60973-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60973-152">INPUTS</span></span>

### <span data-ttu-id="60973-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="60973-153">None</span></span>
<span data-ttu-id="60973-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="60973-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60973-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60973-155">OUTPUTS</span></span>

### <span data-ttu-id="60973-156">Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="60973-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="60973-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60973-157">NOTES</span></span>

## <span data-ttu-id="60973-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60973-158">RELATED LINKS</span></span>

[<span data-ttu-id="60973-159">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="60973-159">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="60973-160">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="60973-160">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="60973-161">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="60973-161">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


