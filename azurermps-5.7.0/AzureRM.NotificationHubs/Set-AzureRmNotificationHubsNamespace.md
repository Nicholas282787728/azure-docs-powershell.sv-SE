---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758204"
---
# <span data-ttu-id="12d41-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="12d41-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="12d41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12d41-102">SYNOPSIS</span></span>
<span data-ttu-id="12d41-103">Anger egenskaps värden för ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="12d41-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12d41-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12d41-105">DESCRIPTION</span></span>
<span data-ttu-id="12d41-106">Cmdleten **set-AzureRmNotificationHubsNamespace** anger egenskaps värden för ett namn område för en befintlig avisering.</span><span class="sxs-lookup"><span data-stu-id="12d41-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>

<span data-ttu-id="12d41-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="12d41-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="12d41-108">Du måste ha minst ett namn område för aviserings navet.</span><span class="sxs-lookup"><span data-stu-id="12d41-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="12d41-109">Dessutom måste alla aviserings nav ha ett tilldelat namn område.</span><span class="sxs-lookup"><span data-stu-id="12d41-109">Additionally, all notification hubs must have an assigned namespace.</span></span>

<span data-ttu-id="12d41-110">Denna cmdlet används främst för att aktivera och inaktivera ett namn område.</span><span class="sxs-lookup"><span data-stu-id="12d41-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="12d41-111">När ett namn område är inaktiverat kan användare inte ansluta till något av meddelandets nav i namn området, eller administratörer kan inte använda de hubbarna för att skicka push-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="12d41-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="12d41-112">Om du vill återaktivera ett inaktiverat namn område kan du använda denna cmdlet för att ange egenskapen **State** för namn området till aktiv.</span><span class="sxs-lookup"><span data-stu-id="12d41-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>

<span data-ttu-id="12d41-113">Du kan också använda denna cmdlet för att tagga ett namn område som kritiskt.</span><span class="sxs-lookup"><span data-stu-id="12d41-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="12d41-114">Detta förhindrar att namn området raderas.</span><span class="sxs-lookup"><span data-stu-id="12d41-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="12d41-115">Om du vill ta bort ett kritiskt namn område måste du först ta bort den kritiska taggen.</span><span class="sxs-lookup"><span data-stu-id="12d41-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="12d41-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12d41-116">EXAMPLES</span></span>

### <span data-ttu-id="12d41-117">Exempel 1: inaktivera ett namn område</span><span class="sxs-lookup"><span data-stu-id="12d41-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="12d41-118">Det här kommandot inaktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till ContosoNotificationsGroup-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="12d41-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="12d41-119">Exempel 2: aktivera ett namn område</span><span class="sxs-lookup"><span data-stu-id="12d41-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="12d41-120">Det här kommandot aktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="12d41-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="12d41-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12d41-121">PARAMETERS</span></span>

### <span data-ttu-id="12d41-122">-Kritiskt</span><span class="sxs-lookup"><span data-stu-id="12d41-122">-Critical</span></span>
<span data-ttu-id="12d41-123">Anger om namn området är ett kritiskt namn område.</span><span class="sxs-lookup"><span data-stu-id="12d41-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="12d41-124">Kritiska namn områden kan inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="12d41-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="12d41-125">Om du vill ta bort ett kritiskt namn område måste du ange värdet för den här egenskapen till falskt för att markera namn området som icke-kritiskt.</span><span class="sxs-lookup"><span data-stu-id="12d41-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d41-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d41-126">-DefaultProfile</span></span>
<span data-ttu-id="12d41-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12d41-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12d41-128">-Force</span><span class="sxs-lookup"><span data-stu-id="12d41-128">-Force</span></span>
<span data-ttu-id="12d41-129">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="12d41-129">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d41-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="12d41-130">-Location</span></span>
<span data-ttu-id="12d41-131">Anger visnings namnet på det data Center som är värd för namn området.</span><span class="sxs-lookup"><span data-stu-id="12d41-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="12d41-132">Även om du kan ange den här parametern till valfri giltig Azure-plats bör du använda ett Data Center nära de flesta av dina användare.</span><span class="sxs-lookup"><span data-stu-id="12d41-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>

<span data-ttu-id="12d41-133">Kör följande kommando för att få en aktuell lista över Azure-platser:</span><span class="sxs-lookup"><span data-stu-id="12d41-133">To get an up-to-date list of Azure locations run the following command:</span></span>

`Get-AzureLocation | Select-Object DisplayName`

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

### <span data-ttu-id="12d41-134">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="12d41-134">-Namespace</span></span>
<span data-ttu-id="12d41-135">Anger den namnrymd som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="12d41-135">Specifies the namespace that this cmdlet modifies.</span></span>

<span data-ttu-id="12d41-136">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="12d41-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="12d41-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12d41-137">-ResourceGroup</span></span>
<span data-ttu-id="12d41-138">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="12d41-138">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="12d41-139">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="12d41-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="12d41-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="12d41-140">-SkuTier</span></span>
<span data-ttu-id="12d41-141">SKU-nivån i namn området</span><span class="sxs-lookup"><span data-stu-id="12d41-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="12d41-142">-State</span><span class="sxs-lookup"><span data-stu-id="12d41-142">-State</span></span>
<span data-ttu-id="12d41-143">Anger namn områdets aktuella status.</span><span class="sxs-lookup"><span data-stu-id="12d41-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="12d41-144">De acceptabla värdena för denna parameter är: Active och disabled.</span><span class="sxs-lookup"><span data-stu-id="12d41-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d41-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="12d41-145">-Tag</span></span>
<span data-ttu-id="12d41-146">Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.</span><span class="sxs-lookup"><span data-stu-id="12d41-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="12d41-147">Funktionen Taggar liknar nyckelord och fungerar i en distribution.</span><span class="sxs-lookup"><span data-stu-id="12d41-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="12d41-148">Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="12d41-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="12d41-149">En enskild tagg består av två delar: *namnet* och (valfritt) *värdet*.</span><span class="sxs-lookup"><span data-stu-id="12d41-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="12d41-150">I till exempel avdelning: den är namnet avdelning och taggnamnet det.</span><span class="sxs-lookup"><span data-stu-id="12d41-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="12d41-151">Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="12d41-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

<span data-ttu-id="12d41-152">-Taggar @ {Name = "CalendarYear"; Värde = "2016"}</span><span class="sxs-lookup"><span data-stu-id="12d41-152">-Tags @{Name="CalendarYear";Value="2016"}</span></span>

<span data-ttu-id="12d41-153">Om du vill lägga till flera taggar i samma kommando avgränsar du de enskilda taggarna genom att använda kommatecken:</span><span class="sxs-lookup"><span data-stu-id="12d41-153">To add multiple tags in the same command, separate the individual tags by using commas:</span></span>

<span data-ttu-id="12d41-154">-Tag @ {Name = "CalendarYear"; Värde = "2016"}; @ {name = "räkenskapsåret"; Värde = "2017"}</span><span class="sxs-lookup"><span data-stu-id="12d41-154">-Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d41-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12d41-155">-Confirm</span></span>
<span data-ttu-id="12d41-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12d41-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d41-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d41-157">-WhatIf</span></span>
<span data-ttu-id="12d41-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12d41-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12d41-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12d41-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d41-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d41-160">CommonParameters</span></span>
<span data-ttu-id="12d41-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d41-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d41-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d41-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d41-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12d41-163">INPUTS</span></span>

### <span data-ttu-id="12d41-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="12d41-164">None</span></span>
<span data-ttu-id="12d41-165">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="12d41-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12d41-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12d41-166">OUTPUTS</span></span>

### <span data-ttu-id="12d41-167">Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="12d41-167">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="12d41-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12d41-168">NOTES</span></span>

## <span data-ttu-id="12d41-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12d41-169">RELATED LINKS</span></span>

[<span data-ttu-id="12d41-170">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="12d41-170">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="12d41-171">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="12d41-171">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="12d41-172">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="12d41-172">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


