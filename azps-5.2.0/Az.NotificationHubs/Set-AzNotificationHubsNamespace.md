---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395200"
---
# <span data-ttu-id="d0b68-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0b68-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="d0b68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0b68-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b68-103">Anger egenskaps värden för ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="d0b68-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="d0b68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0b68-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0b68-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b68-106">Cmdleten **set-AzNotificationHubsNamespace** anger egenskaps värden för ett namn område för en befintlig avisering.</span><span class="sxs-lookup"><span data-stu-id="d0b68-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="d0b68-107">Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d0b68-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="d0b68-108">Du måste ha minst ett namn område för aviserings navet.</span><span class="sxs-lookup"><span data-stu-id="d0b68-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="d0b68-109">Dessutom måste alla aviserings nav ha ett tilldelat namn område.</span><span class="sxs-lookup"><span data-stu-id="d0b68-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="d0b68-110">Denna cmdlet används främst för att aktivera och inaktivera ett namn område.</span><span class="sxs-lookup"><span data-stu-id="d0b68-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="d0b68-111">När ett namn område är inaktiverat kan användare inte ansluta till något av meddelandets nav i namn området, eller administratörer kan inte använda de hubbarna för att skicka push-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d0b68-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="d0b68-112">Om du vill återaktivera ett inaktiverat namn område kan du använda denna cmdlet för att ange egenskapen **State** för namn området till aktiv.</span><span class="sxs-lookup"><span data-stu-id="d0b68-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="d0b68-113">Du kan också använda denna cmdlet för att tagga ett namn område som kritiskt.</span><span class="sxs-lookup"><span data-stu-id="d0b68-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="d0b68-114">Detta förhindrar att namn området raderas.</span><span class="sxs-lookup"><span data-stu-id="d0b68-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="d0b68-115">Om du vill ta bort ett kritiskt namn område måste du först ta bort den kritiska taggen.</span><span class="sxs-lookup"><span data-stu-id="d0b68-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="d0b68-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0b68-116">EXAMPLES</span></span>

### <span data-ttu-id="d0b68-117">Exempel 1: inaktivera ett namn område</span><span class="sxs-lookup"><span data-stu-id="d0b68-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="d0b68-118">Det här kommandot inaktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till ContosoNotificationsGroup-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d0b68-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d0b68-119">Exempel 2: aktivera ett namn område</span><span class="sxs-lookup"><span data-stu-id="d0b68-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="d0b68-120">Det här kommandot aktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till resurs gruppen ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d0b68-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="d0b68-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0b68-121">PARAMETERS</span></span>

### <span data-ttu-id="d0b68-122">-Kritiskt</span><span class="sxs-lookup"><span data-stu-id="d0b68-122">-Critical</span></span>
<span data-ttu-id="d0b68-123">Anger om namn området är ett kritiskt namn område.</span><span class="sxs-lookup"><span data-stu-id="d0b68-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="d0b68-124">Kritiska namn områden kan inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="d0b68-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="d0b68-125">Om du vill ta bort ett kritiskt namn område måste du ange värdet för den här egenskapen till falskt för att markera namn området som icke-kritiskt.</span><span class="sxs-lookup"><span data-stu-id="d0b68-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b68-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b68-126">-DefaultProfile</span></span>
<span data-ttu-id="d0b68-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0b68-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0b68-128">-Force</span><span class="sxs-lookup"><span data-stu-id="d0b68-128">-Force</span></span>
<span data-ttu-id="d0b68-129">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d0b68-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d0b68-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="d0b68-130">-Location</span></span>
<span data-ttu-id="d0b68-131">Anger visnings namnet på det data Center som är värd för namn området.</span><span class="sxs-lookup"><span data-stu-id="d0b68-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="d0b68-132">Även om du kan ange den här parametern till valfri giltig Azure-plats bör du använda ett Data Center nära de flesta av dina användare.</span><span class="sxs-lookup"><span data-stu-id="d0b68-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="d0b68-133">Kör följande kommando för att få en aktuell lista över Azure-platser: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="d0b68-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="d0b68-134">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d0b68-134">-Namespace</span></span>
<span data-ttu-id="d0b68-135">Anger den namnrymd som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d0b68-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="d0b68-136">Med namn utrymmen kan du gruppera och kategorisera meddelande nav.</span><span class="sxs-lookup"><span data-stu-id="d0b68-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d0b68-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0b68-137">-ResourceGroup</span></span>
<span data-ttu-id="d0b68-138">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d0b68-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="d0b68-139">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="d0b68-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d0b68-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d0b68-140">-SkuTier</span></span>
<span data-ttu-id="d0b68-141">SKU-nivån i namn området</span><span class="sxs-lookup"><span data-stu-id="d0b68-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="d0b68-142">-State</span><span class="sxs-lookup"><span data-stu-id="d0b68-142">-State</span></span>
<span data-ttu-id="d0b68-143">Anger namn områdets aktuella status.</span><span class="sxs-lookup"><span data-stu-id="d0b68-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="d0b68-144">De acceptabla värdena för denna parameter är: Active och disabled.</span><span class="sxs-lookup"><span data-stu-id="d0b68-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b68-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d0b68-145">-Tag</span></span>
<span data-ttu-id="d0b68-146">Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.</span><span class="sxs-lookup"><span data-stu-id="d0b68-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="d0b68-147">Funktionen Taggar liknar nyckelord och fungerar i en distribution.</span><span class="sxs-lookup"><span data-stu-id="d0b68-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="d0b68-148">Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d0b68-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="d0b68-149">En enskild tagg består av två delar: *namnet* och (valfritt) *värdet*.</span><span class="sxs-lookup"><span data-stu-id="d0b68-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="d0b68-150">I till exempel avdelning: den är namnet avdelning och taggnamnet det.</span><span class="sxs-lookup"><span data-stu-id="d0b68-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="d0b68-151">Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:-Taggar @ {Name = "CalendarYear"; Värde = "2016"} om du vill lägga till flera taggar i samma kommando delar du de enskilda taggarna genom att använda kommatecken:-tagg @ {Name = "CalendarYear"; Värde = "2016"}; @ {name = "räkenskapsåret"; Värde = "2017"}</span><span class="sxs-lookup"><span data-stu-id="d0b68-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b68-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0b68-152">-Confirm</span></span>
<span data-ttu-id="d0b68-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0b68-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b68-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b68-154">-WhatIf</span></span>
<span data-ttu-id="d0b68-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0b68-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0b68-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0b68-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b68-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b68-157">CommonParameters</span></span>
<span data-ttu-id="d0b68-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b68-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b68-159">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b68-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b68-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0b68-160">INPUTS</span></span>

### <span data-ttu-id="d0b68-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b68-161">System.String</span></span>

### <span data-ttu-id="d0b68-162">Microsoft. Azure. commands. NotificationHubs. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="d0b68-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="d0b68-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0b68-163">System.Boolean</span></span>

### <span data-ttu-id="d0b68-164">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d0b68-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d0b68-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0b68-165">OUTPUTS</span></span>

### <span data-ttu-id="d0b68-166">Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d0b68-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="d0b68-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0b68-167">NOTES</span></span>

## <span data-ttu-id="d0b68-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0b68-168">RELATED LINKS</span></span>

[<span data-ttu-id="d0b68-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0b68-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d0b68-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0b68-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d0b68-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0b68-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


