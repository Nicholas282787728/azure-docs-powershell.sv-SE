---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093263"
---
# <span data-ttu-id="27ff0-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="27ff0-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="27ff0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="27ff0-103">Hämtar Azure-prenumerationer i Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="27ff0-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="27ff0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27ff0-104">SYNTAX</span></span>

### <span data-ttu-id="27ff0-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="27ff0-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ff0-106">ById</span><span class="sxs-lookup"><span data-stu-id="27ff0-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ff0-107">Vis</span><span class="sxs-lookup"><span data-stu-id="27ff0-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="27ff0-108">Här</span><span class="sxs-lookup"><span data-stu-id="27ff0-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27ff0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27ff0-109">DESCRIPTION</span></span>
<span data-ttu-id="27ff0-110">Cmdleten **Get-AzureSubscription** hämtar abonnemangen på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="27ff0-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="27ff0-111">Du kan använda denna cmdlet för att få information om prenumerationen och för att gå med i prenumerationen på andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ff0-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="27ff0-112">**Get-AzureSubscription** kräver åtkomst till dina Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="27ff0-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="27ff0-113">Innan du kör **Get-AzureSubscription** måste du köra cmdleten **Add-AzureAccount** eller de cmdlets som laddar ned och installerar en fil för publicerings inställningar ( **Get-AzurePublishSettingsFile** , **import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="27ff0-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="27ff0-114">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="27ff0-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="27ff0-115">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="27ff0-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="27ff0-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27ff0-116">EXAMPLES</span></span>

### <span data-ttu-id="27ff0-117">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="27ff0-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="27ff0-118">Det här kommandot får alla abonnemang på kontot.</span><span class="sxs-lookup"><span data-stu-id="27ff0-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="27ff0-119">Exempel 2: skaffa ett abonnemang efter namn</span><span class="sxs-lookup"><span data-stu-id="27ff0-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="27ff0-120">Det här kommandot får bara till "MyProdSubsciption"-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="27ff0-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="27ff0-121">Exempel 3: Hämta standard abonnemanget</span><span class="sxs-lookup"><span data-stu-id="27ff0-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="27ff0-122">Det här kommandot får bara namnet på standard abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="27ff0-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="27ff0-123">Kommandot får först abonnemanget och använder sedan metoden dot för att hämta **SubscriptionName** -egenskapen för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="27ff0-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="27ff0-124">Exempel 4: Hämta valda prenumerations egenskaper</span><span class="sxs-lookup"><span data-stu-id="27ff0-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="27ff0-125">Det här kommandot returnerar en lista med namnet och certifikatet för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="27ff0-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="27ff0-126">Det använder kommandot **Get-AzureSubscription** för att hämta det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="27ff0-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="27ff0-127">Sedan rör det prenumerationen till ett **format List** kommando som visar de markerade egenskaperna i en lista.</span><span class="sxs-lookup"><span data-stu-id="27ff0-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="27ff0-128">Exempel 5: använda en alternativ fil för abonnemang</span><span class="sxs-lookup"><span data-stu-id="27ff0-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="27ff0-129">Det här kommandot hämtar abonnemang från data filen C:\Temp\MySubscriptions.xml-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27ff0-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="27ff0-130">Använd parametern **SubscriptionDataFile** om du har angett en alternativ fil för abonnemang när du körde cmdletarna **Add-AzureAccount** eller **import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="27ff0-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="27ff0-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27ff0-131">PARAMETERS</span></span>

### <span data-ttu-id="27ff0-132">-Aktuell</span><span class="sxs-lookup"><span data-stu-id="27ff0-132">-Current</span></span>
<span data-ttu-id="27ff0-133">Hämtar bara det aktuella abonnemanget, det vill säga prenumerationen som "Current".</span><span class="sxs-lookup"><span data-stu-id="27ff0-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="27ff0-134">Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="27ff0-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="27ff0-135">Om du vill ange ett abonnemang som "Aktuellt" använder du den **aktuella** parametern för cmdleten **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="27ff0-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-136">-Standard</span><span class="sxs-lookup"><span data-stu-id="27ff0-136">-Default</span></span>
<span data-ttu-id="27ff0-137">Hämtar bara standard abonnemanget, det vill säga prenumerationen som "standard".</span><span class="sxs-lookup"><span data-stu-id="27ff0-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="27ff0-138">Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="27ff0-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="27ff0-139">Använd **standard** parametern för cmdleten **Select-AzureSubscription** om du vill ange ett abonnemang som "standard".</span><span class="sxs-lookup"><span data-stu-id="27ff0-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="27ff0-140">-ExtendedDetails</span></span>
<span data-ttu-id="27ff0-141">Returnerar kvot information för abonnemanget, utöver standardinställningarna.</span><span class="sxs-lookup"><span data-stu-id="27ff0-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="27ff0-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="27ff0-142">-Profile</span></span>
<span data-ttu-id="27ff0-143">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="27ff0-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="27ff0-144">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="27ff0-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27ff0-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27ff0-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="27ff0-146">-SubscriptionName</span></span>
<span data-ttu-id="27ff0-147">Hämtar bara det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="27ff0-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="27ff0-148">Ange prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="27ff0-148">Enter the subscription name.</span></span>
<span data-ttu-id="27ff0-149">Värdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="27ff0-149">The value is case-sensitive.</span></span>
<span data-ttu-id="27ff0-150">Jokertecken stöds inte.</span><span class="sxs-lookup"><span data-stu-id="27ff0-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="27ff0-151">Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="27ff0-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ff0-152">CommonParameters</span></span>
<span data-ttu-id="27ff0-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ff0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ff0-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ff0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ff0-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27ff0-155">INPUTS</span></span>

### <span data-ttu-id="27ff0-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="27ff0-156">None</span></span>
<span data-ttu-id="27ff0-157">Du kan ange indata för egenskapen **SubscriptionName** efter namn men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="27ff0-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="27ff0-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27ff0-158">OUTPUTS</span></span>

### <span data-ttu-id="27ff0-159">Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="27ff0-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="27ff0-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27ff0-160">NOTES</span></span>
* <span data-ttu-id="27ff0-161">Get-AzureSubscription hämtar data från den prenumerations data fil som du skapar med cmdletarna **Add-AzureAccount** och **import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="27ff0-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="27ff0-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27ff0-162">RELATED LINKS</span></span>

[<span data-ttu-id="27ff0-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="27ff0-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="27ff0-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="27ff0-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="27ff0-165">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="27ff0-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="27ff0-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="27ff0-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="27ff0-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="27ff0-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


