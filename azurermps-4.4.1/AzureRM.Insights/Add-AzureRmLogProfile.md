---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585532"
---
# <span data-ttu-id="16ccc-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="16ccc-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="16ccc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="16ccc-103">Skapar en ny aktivitets logg profil.</span><span class="sxs-lookup"><span data-stu-id="16ccc-103">Creates a new activity log profile.</span></span> <span data-ttu-id="16ccc-104">Denna profil används till att antingen arkivera aktivitets loggen på ett Azure Storage-konto eller strömma den till en Azure Event Hub i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="16ccc-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="16ccc-105">**Lagrings konto** – det finns inget standard lagrings konto (Premium Storage-konto stöds inte).</span><span class="sxs-lookup"><span data-stu-id="16ccc-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="16ccc-106">Det kan antingen vara av typen ARM eller klassiskt.</span><span class="sxs-lookup"><span data-stu-id="16ccc-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="16ccc-107">Om den är inloggad på ett lagrings konto debiteras kostnaden för att lagra aktivitets loggen med normal standard lagrings taxa.</span><span class="sxs-lookup"><span data-stu-id="16ccc-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="16ccc-108">Det kan bara finnas en enda logg profil per prenumeration som bara är ett lagrings konto per prenumeration som kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="16ccc-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="16ccc-109">**Händelsehubben-det** kan bara finnas en enda logg profil per prenumeration som bara en händelse gren per prenumeration kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="16ccc-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="16ccc-110">Om aktivitets loggen strömmas till en händelsehubben tillämpas standard Event Hub-priser.</span><span class="sxs-lookup"><span data-stu-id="16ccc-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="16ccc-111">I aktivitets loggen kan händelser gälla en region eller kan vara "globalt".</span><span class="sxs-lookup"><span data-stu-id="16ccc-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="16ccc-112">Global innebär detta att dessa händelser är region agnostics och att de är oberoende av regionen, i de flesta händelser hamnar i den kategorin.</span><span class="sxs-lookup"><span data-stu-id="16ccc-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="16ccc-113">Om aktivitets loggnings profilen är inställd från portalen lägger den implicit till "global" tillsammans med alla andra regioner som är markerade i användar gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="16ccc-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="16ccc-114">När du använder en cmdlet måste platsen som "global" anges explicit från valfri annan region.</span><span class="sxs-lookup"><span data-stu-id="16ccc-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="16ccc-115">**Obs!** **om du inte anger "globalt" i platserna kommer det att leda till att huvud aktivitets loggen inte exporteras.**</span><span class="sxs-lookup"><span data-stu-id="16ccc-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ccc-116">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ccc-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16ccc-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ccc-117">DESCRIPTION</span></span>
<span data-ttu-id="16ccc-118">Cmdleten **Add-AzureRmLogProfile** skapar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="16ccc-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="16ccc-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ccc-119">EXAMPLES</span></span>

### <span data-ttu-id="16ccc-120">Exempel 1: lägga till en ny logg profil för att exportera aktivitets loggen som matchar plats tillståndet till ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="16ccc-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="16ccc-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ccc-121">PARAMETERS</span></span>

### <span data-ttu-id="16ccc-122">-Kategorier</span><span class="sxs-lookup"><span data-stu-id="16ccc-122">-Categories</span></span>
<span data-ttu-id="16ccc-123">Anger listan över kategorier.</span><span class="sxs-lookup"><span data-stu-id="16ccc-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="16ccc-124">-Platser</span><span class="sxs-lookup"><span data-stu-id="16ccc-124">-Locations</span></span>
<span data-ttu-id="16ccc-125">Anger platsen för logg profilen.</span><span class="sxs-lookup"><span data-stu-id="16ccc-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="16ccc-126">Giltiga värden: kör nedan cmdlet för att få den senaste listan över platser.</span><span class="sxs-lookup"><span data-stu-id="16ccc-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="16ccc-127">Get-AzureLocation | Välj DisplayName</span><span class="sxs-lookup"><span data-stu-id="16ccc-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="16ccc-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="16ccc-128">-Name</span></span>
<span data-ttu-id="16ccc-129">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="16ccc-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="16ccc-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="16ccc-130">-RetentionInDays</span></span>
<span data-ttu-id="16ccc-131">Anger bevarande principen i dagar.</span><span class="sxs-lookup"><span data-stu-id="16ccc-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="16ccc-132">Det här är antalet dagar som loggar bevaras i det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="16ccc-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="16ccc-133">För att behålla data förinställd på **0** för alltid</span><span class="sxs-lookup"><span data-stu-id="16ccc-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="16ccc-134">Om det inte anges blir standardvärdet **0**.</span><span class="sxs-lookup"><span data-stu-id="16ccc-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="16ccc-135">Vanliga fakturerings avgifter för standard lagring eller Event Hub gäller för data lagring.</span><span class="sxs-lookup"><span data-stu-id="16ccc-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="16ccc-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="16ccc-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="16ccc-137">Anger ID för Service Bus-regeln.</span><span class="sxs-lookup"><span data-stu-id="16ccc-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="16ccc-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="16ccc-138">-StorageAccountId</span></span>
<span data-ttu-id="16ccc-139">Anger ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="16ccc-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="16ccc-140">ID är det fullt kvalificerade resurs-ID: t för lagrings kontot, till exempel</span><span class="sxs-lookup"><span data-stu-id="16ccc-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="16ccc-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="16ccc-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="16ccc-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ccc-142">-DefaultProfile</span></span>
<span data-ttu-id="16ccc-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16ccc-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ccc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ccc-144">CommonParameters</span></span>
<span data-ttu-id="16ccc-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ccc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ccc-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ccc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ccc-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ccc-147">INPUTS</span></span>

## <span data-ttu-id="16ccc-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ccc-148">OUTPUTS</span></span>

### <span data-ttu-id="16ccc-149">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="16ccc-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="16ccc-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ccc-150">NOTES</span></span>

## <span data-ttu-id="16ccc-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ccc-151">RELATED LINKS</span></span>

[<span data-ttu-id="16ccc-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="16ccc-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="16ccc-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="16ccc-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


