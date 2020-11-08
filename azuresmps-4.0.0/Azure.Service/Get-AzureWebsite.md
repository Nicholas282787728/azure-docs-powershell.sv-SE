---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099504"
---
# <span data-ttu-id="9cfb0-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="9cfb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cfb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfb0-103">Får Azure-webbplatser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="9cfb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cfb0-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9cfb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cfb0-105">DESCRIPTION</span></span>
<span data-ttu-id="9cfb0-106">Cmdleten **Get-AzureWebsite** hämtar information om Azure-webbplatserna i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="9cfb0-107">Som standard får **Get-AzureWebsite** alla Azure-webbplatser i den aktuella prenumerationen och returnerar ett objekt med grundläggande information om webbplatserna.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="9cfb0-108">När du använder parametern *Name* returnerar **-AzureWebsite** ett objekt med omfattande information, inklusive konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="9cfb0-109">Det aktuella abonnemanget är den prenumeration som är "aktuell".</span><span class="sxs-lookup"><span data-stu-id="9cfb0-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="9cfb0-110">Använd den *aktuella* parametern för cmdleten [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) för att hitta den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="9cfb0-111">Använd cmdleten [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) för att ändra aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="9cfb0-112">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9cfb0-113">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9cfb0-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="9cfb0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cfb0-114">EXAMPLES</span></span>

### <span data-ttu-id="9cfb0-115">Exempel 1: Hämta alla webbplatser i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="9cfb0-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="9cfb0-116">Det här kommandot får alla Azure-webbplatser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="9cfb0-117">Exempel 2: Hämta en webbplats med namn</span><span class="sxs-lookup"><span data-stu-id="9cfb0-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="9cfb0-118">Det här kommandot får detaljerad information om ContosoWeb Azure-webbplatsen, inklusive konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="9cfb0-119">När du använder parametern *Name* returnerar **AzureWebsite** ett **SiteWithConfig** -objekt med utökad information om webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="9cfb0-120">Exempel 3: få detaljerad information om alla webbplatser</span><span class="sxs-lookup"><span data-stu-id="9cfb0-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="9cfb0-121">Det här kommandot får detaljerad information om alla webbplatser i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="9cfb0-122">Den använder kommandot **Get-AzureWebsite** för att hämta alla webbplatser och använder sedan framenser **-Object** cmdlet för att hämta varje webbplats med namn.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="9cfb0-123">Exempel 4: få information om en distributions plats</span><span class="sxs-lookup"><span data-stu-id="9cfb0-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="9cfb0-124">Det här kommandot får du mellanlagrings platsen för ContosoWeb webbplats.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="9cfb0-125">Med distributions platser kan du testa olika versioner av din Azure-webbplats utan att släppa dem till allmänheten.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="9cfb0-126">Exempel 5: Hämta webbplats instanser</span><span class="sxs-lookup"><span data-stu-id="9cfb0-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="9cfb0-127">Kommandona i det här exemplet använder egenskapen instances för en Azure-webbplats för att få information om för tillfället aktiva webbplats instanser.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="9cfb0-128">Egenskapen **instances** lades till i **SiteWithConfig** -objektet i version 0.8.3 i Azure-modulen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="9cfb0-129">Det första kommandot får instans-ID: na för alla instanser av en webbplats som körs för tillfället.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="9cfb0-130">Det andra kommandot får antalet aktiva instanser av webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="9cfb0-131">Du kan använda **Count** -egenskapen på vilken matris som helst.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="9cfb0-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cfb0-132">PARAMETERS</span></span>

### <span data-ttu-id="9cfb0-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cfb0-133">-Name</span></span>
<span data-ttu-id="9cfb0-134">Hämtar detaljerad konfigurations information om den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="9cfb0-135">Ange namnet på en webbplats i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="9cfb0-136">Som standard får **Get-AzureWebsite** alla webbplatser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="9cfb0-137">Värdet *Name* stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-137">The *Name* value does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfb0-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="9cfb0-138">-Profile</span></span>
<span data-ttu-id="9cfb0-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cfb0-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cfb0-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="9cfb0-141">-Slot</span></span>
<span data-ttu-id="9cfb0-142">Hämtar den angivna distributions platsen för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="9cfb0-143">Ange plats namnet, till exempel "organisering" eller "produktion".</span><span class="sxs-lookup"><span data-stu-id="9cfb0-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="9cfb0-144">Mer information om distributions platser finns i stegvis distribution på Microsoft Azure-webbplatser https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="9cfb0-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="9cfb0-145">Använd Set-AzureWebsite cmdlet för att lägga till en distributions plats på en befintlig Azure-webbplats.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cfb0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfb0-146">CommonParameters</span></span>
<span data-ttu-id="9cfb0-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfb0-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cfb0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfb0-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cfb0-149">INPUTS</span></span>

### <span data-ttu-id="9cfb0-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="9cfb0-150">None</span></span>
<span data-ttu-id="9cfb0-151">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="9cfb0-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cfb0-152">OUTPUTS</span></span>

### <span data-ttu-id="9cfb0-153">Microsoft. WindowsAzure. commands. Utilities. sites. Services. webentities. webbplats</span><span class="sxs-lookup"><span data-stu-id="9cfb0-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="9cfb0-154">Som standard returnerar **Get-AzureWebsite** en matris med **webbplats** objekt.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="9cfb0-155">Microsoft. WindowsAzure. commands. Utilities. webentities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="9cfb0-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="9cfb0-156">När du använder parametern *Name* returnerar **AzureWebsite** ett **SiteWithConfig** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9cfb0-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="9cfb0-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cfb0-157">NOTES</span></span>

## <span data-ttu-id="9cfb0-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cfb0-158">RELATED LINKS</span></span>

[<span data-ttu-id="9cfb0-159">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="9cfb0-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="9cfb0-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="9cfb0-162">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="9cfb0-163">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cfb0-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


