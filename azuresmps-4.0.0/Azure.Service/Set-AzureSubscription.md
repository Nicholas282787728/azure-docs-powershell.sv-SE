---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099180"
---
# <span data-ttu-id="da5d2-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="da5d2-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="da5d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="da5d2-103">Ändrar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="da5d2-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="da5d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da5d2-104">SYNTAX</span></span>

### <span data-ttu-id="da5d2-105">UpdateSubscriptionByIdParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="da5d2-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="da5d2-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="da5d2-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="da5d2-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="da5d2-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="da5d2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da5d2-108">DESCRIPTION</span></span>
<span data-ttu-id="da5d2-109">Cmdleten **set-AzureSubscription** etablerar och ändrar egenskaperna för ett objekt i Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da5d2-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="da5d2-110">Du kan använda denna cmdlet för att arbeta i ett Azure-abonnemang som inte är ditt standard abonnemang eller för att ändra ditt nuvarande lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="da5d2-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="da5d2-111">Information om aktuella och standard abonnemang finns i cmdleten **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="da5d2-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="da5d2-112">Denna cmdlet fungerar på ett Azure Subscription-objekt, inte ditt faktiska Azure-abonnemang.</span><span class="sxs-lookup"><span data-stu-id="da5d2-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="da5d2-113">Om du vill skapa och etablera ett Azure-abonnemang går du till [Azure-portalen](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="da5d2-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="da5d2-114">Denna cmdlet ändrar data i den prenumerations data fil som du skapar när du lägger till ett Azure-konto i Windows PowerShell med cmdleten **Add-AzureAccount** eller **import-AzurePublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="da5d2-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="da5d2-115">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="da5d2-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="da5d2-116">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="da5d2-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="da5d2-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da5d2-117">EXAMPLES</span></span>

### <span data-ttu-id="da5d2-118">Exempel 1: ändra en befintlig abonnemang1</span><span class="sxs-lookup"><span data-stu-id="da5d2-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="da5d2-119">Det här exemplet ändrar certifikatet för prenumerationen som heter ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="da5d2-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="da5d2-120">Exempel 2: ändra tjänstens slut punkt</span><span class="sxs-lookup"><span data-stu-id="da5d2-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="da5d2-121">Det här kommandot lägger till eller ändrar en anpassad tjänst slut punkt för ContosoEngineering-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da5d2-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="da5d2-122">Exempel 3: Rensa egenskaps värden</span><span class="sxs-lookup"><span data-stu-id="da5d2-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="da5d2-123">Det här kommandot anger värdena för egenskaperna certifikat och ResourceManagerEndpoint till null ($Null).</span><span class="sxs-lookup"><span data-stu-id="da5d2-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="da5d2-124">Då raderas värdena för dessa egenskaper utan att andra inställningar ändras.</span><span class="sxs-lookup"><span data-stu-id="da5d2-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="da5d2-125">Exempel 4: använda en alternativ fil för abonnemang</span><span class="sxs-lookup"><span data-stu-id="da5d2-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="da5d2-126">Det här kommandot ändrar det aktuella lagrings kontot för ContosoFinance-prenumerationen till ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="da5d2-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="da5d2-127">Kommandot använder parametern **SubscriptionDataFile** för att ändra data i C:\Azure\SubscriptionData.xml-prenumerationens datafil.</span><span class="sxs-lookup"><span data-stu-id="da5d2-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="da5d2-128">Standardinställningen är att **set-AzureSubscription** använder standard filen för abonnemang i din centrala användar profil.</span><span class="sxs-lookup"><span data-stu-id="da5d2-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="da5d2-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da5d2-129">PARAMETERS</span></span>

### <span data-ttu-id="da5d2-130">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="da5d2-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-131">-Kontext</span><span class="sxs-lookup"><span data-stu-id="da5d2-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="da5d2-132">-CurrentStorageAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-133">-Miljö</span><span class="sxs-lookup"><span data-stu-id="da5d2-133">-Environment</span></span>
<span data-ttu-id="da5d2-134">Anger en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="da5d2-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="da5d2-135">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="da5d2-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="da5d2-136">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="da5d2-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="da5d2-137">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da5d2-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da5d2-138">-PassThru</span></span>
<span data-ttu-id="da5d2-139">Returnerar $True om kommandot lyckas och $False om det inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="da5d2-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="da5d2-140">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="da5d2-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="da5d2-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="da5d2-141">-Profile</span></span>
<span data-ttu-id="da5d2-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="da5d2-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="da5d2-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="da5d2-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da5d2-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="da5d2-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="da5d2-145">Anger slut punkten för Azure Resource Manager-data, inklusive data om resurs grupper som är kopplade till kontot.</span><span class="sxs-lookup"><span data-stu-id="da5d2-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="da5d2-146">Mer information om Azure Resource Manager finns i [Azure Resource Manager-cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) och [med Windows PowerShell med Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="da5d2-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="da5d2-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="da5d2-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="da5d2-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da5d2-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="da5d2-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5d2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5d2-150">CommonParameters</span></span>
<span data-ttu-id="da5d2-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5d2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5d2-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da5d2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5d2-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da5d2-153">INPUTS</span></span>

### <span data-ttu-id="da5d2-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="da5d2-154">None</span></span>
<span data-ttu-id="da5d2-155">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="da5d2-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="da5d2-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da5d2-156">OUTPUTS</span></span>

### <span data-ttu-id="da5d2-157">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="da5d2-157">None or System.Boolean</span></span>
<span data-ttu-id="da5d2-158">När du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="da5d2-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="da5d2-159">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="da5d2-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="da5d2-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da5d2-160">NOTES</span></span>

## <span data-ttu-id="da5d2-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da5d2-161">RELATED LINKS</span></span>

[<span data-ttu-id="da5d2-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="da5d2-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="da5d2-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="da5d2-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="da5d2-164">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="da5d2-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="da5d2-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="da5d2-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="da5d2-166">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="da5d2-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


