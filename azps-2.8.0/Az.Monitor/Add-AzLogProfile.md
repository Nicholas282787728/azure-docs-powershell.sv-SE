---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: c4ed6fc65a3f785f78a86c7f495486e95404f3d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743602"
---
# <span data-ttu-id="a92a9-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a92a9-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="a92a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a92a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a92a9-103">Skapar en ny aktivitets logg profil.</span><span class="sxs-lookup"><span data-stu-id="a92a9-103">Creates a new activity log profile.</span></span> <span data-ttu-id="a92a9-104">Denna profil används till att antingen arkivera aktivitets loggen på ett Azure Storage-konto eller strömma den till en Azure Event Hub i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a92a9-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="a92a9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a92a9-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92a9-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a92a9-106">DESCRIPTION</span></span>
<span data-ttu-id="a92a9-107">Cmdleten **Add-AzLogProfile** skapar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="a92a9-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="a92a9-108">**Lagrings konto** – det finns inget standard lagrings konto (Premium Storage-konto stöds inte).</span><span class="sxs-lookup"><span data-stu-id="a92a9-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="a92a9-109">Det kan antingen vara av typen ARM eller klassiskt.</span><span class="sxs-lookup"><span data-stu-id="a92a9-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="a92a9-110">Om den är inloggad på ett lagrings konto debiteras kostnaden för att lagra aktivitets loggen med normal standard lagrings taxa.</span><span class="sxs-lookup"><span data-stu-id="a92a9-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="a92a9-111">Det kan bara finnas en enda logg profil per prenumeration som bara är ett lagrings konto per prenumeration som kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="a92a9-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="a92a9-112">**Händelsehubben-det** kan bara finnas en enda logg profil per prenumeration som bara en händelse gren per prenumeration kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="a92a9-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="a92a9-113">Om aktivitets loggen strömmas till en händelsehubben tillämpas standard Event Hub-priser.</span><span class="sxs-lookup"><span data-stu-id="a92a9-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="a92a9-114">I aktivitets loggen kan händelser gälla en region eller kan vara "globalt".</span><span class="sxs-lookup"><span data-stu-id="a92a9-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="a92a9-115">Global innebär detta att dessa händelser är region agnostics och att de är oberoende av regionen, i de flesta händelser hamnar i den kategorin.</span><span class="sxs-lookup"><span data-stu-id="a92a9-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="a92a9-116">Om aktivitets loggnings profilen är inställd från portalen lägger den implicit till "global" tillsammans med alla andra regioner som är markerade i användar gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="a92a9-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="a92a9-117">När du använder en cmdlet måste platsen som "global" anges explicit från valfri annan region.</span><span class="sxs-lookup"><span data-stu-id="a92a9-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="a92a9-118">**Obs!** **om du inte anger "globalt" i platserna kommer det att leda till att huvud aktivitets loggen inte exporteras.**</span><span class="sxs-lookup"><span data-stu-id="a92a9-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="a92a9-119">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="a92a9-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a92a9-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a92a9-120">EXAMPLES</span></span>

### <span data-ttu-id="a92a9-121">Exempel 1: lägga till en ny logg profil för att exportera aktivitets loggen som matchar plats tillståndet till ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a92a9-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="a92a9-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a92a9-122">PARAMETERS</span></span>

### <span data-ttu-id="a92a9-123">-Kategori</span><span class="sxs-lookup"><span data-stu-id="a92a9-123">-Category</span></span>
<span data-ttu-id="a92a9-124">Anger listan över kategorier.</span><span class="sxs-lookup"><span data-stu-id="a92a9-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92a9-125">-DefaultProfile</span></span>
<span data-ttu-id="a92a9-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a92a9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92a9-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="a92a9-127">-Location</span></span>
<span data-ttu-id="a92a9-128">Anger platsen för logg profilen.</span><span class="sxs-lookup"><span data-stu-id="a92a9-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="a92a9-129">Giltiga värden: kör nedan cmdlet för att få den senaste listan över platser.</span><span class="sxs-lookup"><span data-stu-id="a92a9-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="a92a9-130">Get-AzLocation | Välj DisplayName</span><span class="sxs-lookup"><span data-stu-id="a92a9-130">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="a92a9-131">-Name</span></span>
<span data-ttu-id="a92a9-132">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="a92a9-132">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a92a9-133">-RetentionInDays</span></span>
<span data-ttu-id="a92a9-134">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="a92a9-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="a92a9-135">Det här är antalet dagar som loggar bevaras i det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a92a9-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="a92a9-136">För att behålla data förinställd på **0** för alltid</span><span class="sxs-lookup"><span data-stu-id="a92a9-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="a92a9-137">Om det inte anges blir standardvärdet **0**.</span><span class="sxs-lookup"><span data-stu-id="a92a9-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="a92a9-138">Vanliga fakturerings avgifter för standard lagring eller Event Hub gäller för data lagring.</span><span class="sxs-lookup"><span data-stu-id="a92a9-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="a92a9-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="a92a9-140">Anger ID för Service Bus-regeln.</span><span class="sxs-lookup"><span data-stu-id="a92a9-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a92a9-141">-StorageAccountId</span></span>
<span data-ttu-id="a92a9-142">Anger ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a92a9-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="a92a9-143">ID är det fullt kvalificerade resurs-ID: t för lagrings kontot, till exempel</span><span class="sxs-lookup"><span data-stu-id="a92a9-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="a92a9-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="a92a9-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92a9-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a92a9-145">-Confirm</span></span>
<span data-ttu-id="a92a9-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a92a9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92a9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92a9-147">-WhatIf</span></span>
<span data-ttu-id="a92a9-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a92a9-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a92a9-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a92a9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92a9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92a9-150">CommonParameters</span></span>
<span data-ttu-id="a92a9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92a9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92a9-152">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a92a9-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92a9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a92a9-153">INPUTS</span></span>

### <span data-ttu-id="a92a9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a92a9-154">System.String</span></span>

### <span data-ttu-id="a92a9-155">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a92a9-155">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a92a9-156">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a92a9-156">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a92a9-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a92a9-157">OUTPUTS</span></span>

### <span data-ttu-id="a92a9-158">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="a92a9-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="a92a9-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a92a9-159">NOTES</span></span>

## <span data-ttu-id="a92a9-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a92a9-160">RELATED LINKS</span></span>

[<span data-ttu-id="a92a9-161">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a92a9-161">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="a92a9-162">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="a92a9-162">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


