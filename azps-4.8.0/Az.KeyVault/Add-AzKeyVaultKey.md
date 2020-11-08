---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102830"
---
# <span data-ttu-id="26a75-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26a75-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="26a75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26a75-102">SYNOPSIS</span></span>
<span data-ttu-id="26a75-103">Skapar en Key i ett nyckelord eller importerar en Key till ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="26a75-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="26a75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26a75-104">SYNTAX</span></span>

### <span data-ttu-id="26a75-105">InteractiveCreate (standard)</span><span class="sxs-lookup"><span data-stu-id="26a75-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a75-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="26a75-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a75-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="26a75-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a75-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="26a75-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a75-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="26a75-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a75-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="26a75-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a75-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26a75-111">DESCRIPTION</span></span>
<span data-ttu-id="26a75-112">Cmdleten **Add-AzKeyVaultKey** skapar en Key i ett nyckelord i ett nyckeltal i Azure Key Vault, eller importerar en till en Key Vault.</span><span class="sxs-lookup"><span data-stu-id="26a75-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="26a75-113">Använd denna cmdlet för att lägga till nycklar på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="26a75-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="26a75-114">Skapa en knapp i en maskinvarubaserad säkerhetsmodul (HSM) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26a75-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="26a75-115">Skapa en under program vara i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26a75-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="26a75-116">Importera en knapp från din egen Hardware säkerhetsmodul (HSM) till HSMs i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26a75-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="26a75-117">Importera en från en. pfx-fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="26a75-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="26a75-118">Importera en knapp från en. pfx-fil på datorn till HSMs (Hardware Security modules) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26a75-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="26a75-119">Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="26a75-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="26a75-120">Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i ditt nyckelord uppdateras den ursprungliga tangenten med de värden som du anger för den nya.</span><span class="sxs-lookup"><span data-stu-id="26a75-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="26a75-121">Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="26a75-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="26a75-122">Mer information om nyckel versioner och URI-strukturen finns i [om nycklar och hemligheter](http://go.microsoft.com/fwlink/?linkid=518560) i övriga API-dokumentation för nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="26a75-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="26a75-123">Obs! Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="26a75-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="26a75-124">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="26a75-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="26a75-125">Vi rekommenderar att du säkerhetskopierar din-tangenten efter att den har skapats eller uppdaterats genom att använda Backup-AzKeyVaultKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a75-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="26a75-126">Det finns inga funktioner för att ångra borttagning, så om du råkar ta bort en eller flera rader och sedan ändrar dig kan du inte återställa den, såvida du inte har en säkerhets kopia av den.</span><span class="sxs-lookup"><span data-stu-id="26a75-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="26a75-127">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26a75-127">EXAMPLES</span></span>

### <span data-ttu-id="26a75-128">Exempel 1: skapa en-tangenten</span><span class="sxs-lookup"><span data-stu-id="26a75-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="26a75-129">Det här kommandot skapar en programskyddad nycklar med namnet ITSoftware i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="26a75-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="26a75-130">Exempel 2: skapa en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="26a75-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="26a75-131">Det här kommandot skapar en HSM-skyddad nycklar i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="26a75-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="26a75-132">Exempel 3: skapa en transparens med icke-standardvärden</span><span class="sxs-lookup"><span data-stu-id="26a75-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="26a75-133">Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.</span><span class="sxs-lookup"><span data-stu-id="26a75-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="26a75-134">Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="26a75-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="26a75-135">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="26a75-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="26a75-136">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="26a75-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="26a75-137">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="26a75-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="26a75-138">Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="26a75-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="26a75-139">Det objektet anger den aktuella UTC-tiden.</span><span class="sxs-lookup"><span data-stu-id="26a75-139">That object specifies current UTC time.</span></span> <span data-ttu-id="26a75-140">I kommandot lagras datumet i $NotBefore variabel.</span><span class="sxs-lookup"><span data-stu-id="26a75-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="26a75-141">Med kommandot slut skapas en Key med namnet ITHsmNonDefault som är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="26a75-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="26a75-142">Kommandot anger värden för tillåtna operationer som lagras $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="26a75-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="26a75-143">Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="26a75-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="26a75-144">Den nya knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="26a75-144">The new key is disabled.</span></span> <span data-ttu-id="26a75-145">Du kan aktivera den med cmdleten **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="26a75-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="26a75-146">Exempel 4: importera en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="26a75-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="26a75-147">Det här kommandot importerar den nycklar som heter ITByok från platsen som parametern för *fil Sök vägen* anger.</span><span class="sxs-lookup"><span data-stu-id="26a75-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="26a75-148">Den importerade knappen är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="26a75-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="26a75-149">Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="26a75-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="26a75-150">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="26a75-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="26a75-151">Exempel 5: importera en skyddad program vara</span><span class="sxs-lookup"><span data-stu-id="26a75-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="26a75-152">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="26a75-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="26a75-153">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="26a75-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="26a75-154">Det andra kommandot skapar ett program varu lösen ord i ett contoso-valv.</span><span class="sxs-lookup"><span data-stu-id="26a75-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="26a75-155">Kommandot anger platsen för den och det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="26a75-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="26a75-156">Exempel 6: importera en nycklar och tilldela attribut</span><span class="sxs-lookup"><span data-stu-id="26a75-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="26a75-157">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="26a75-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="26a75-158">Det andra kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i $expires variabeln.</span><span class="sxs-lookup"><span data-stu-id="26a75-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="26a75-159">Det tredje kommandot skapar $tags variabel för att ställa in taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="26a75-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="26a75-160">Med kommandot slut importeras en nycklar som en HSM-tangenten från den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="26a75-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="26a75-161">Kommandot anger den förfallo tid som är lagrad i $Expires och lösen ord som lagras i $Password och tillämpar taggarna som lagras i $tags.</span><span class="sxs-lookup"><span data-stu-id="26a75-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="26a75-162">Exempel 7: generera en KEK för nyckeln "skaffa en egen nyckeln" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="26a75-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="26a75-163">Skapar en snabb kurs (kallas KEK).</span><span class="sxs-lookup"><span data-stu-id="26a75-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="26a75-164">KEK måste vara en RSA-HSM som bara har åtgärden Importera.</span><span class="sxs-lookup"><span data-stu-id="26a75-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="26a75-165">Endast nyckel valv Premium SKU har stöd för RSA-HSM-nycklar.</span><span class="sxs-lookup"><span data-stu-id="26a75-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="26a75-166">Mer information finns i https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="26a75-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="26a75-167">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26a75-167">PARAMETERS</span></span>

### <span data-ttu-id="26a75-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a75-168">-DefaultProfile</span></span>
<span data-ttu-id="26a75-169">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26a75-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26a75-170">-Mål</span><span class="sxs-lookup"><span data-stu-id="26a75-170">-Destination</span></span>
<span data-ttu-id="26a75-171">Anger om du vill lägga till en nycklar som en programvarubaserad eller en HSM-skyddad nycklar i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26a75-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="26a75-172">Giltiga värden är: HSM och program vara.</span><span class="sxs-lookup"><span data-stu-id="26a75-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="26a75-173">Obs! Om du vill använda HSM som mål måste du ha ett huvud valv som stöder HSMs.</span><span class="sxs-lookup"><span data-stu-id="26a75-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="26a75-174">Mer information om tjänst nivåer och funktioner för Azure Key Vault finns på [webbplatsen för Azure Key Vault prissättning](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="26a75-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="26a75-175">Den här parametern är obligatorisk när du skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="26a75-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="26a75-176">Om du importerar en fil med parametern *sökväg* är denna parameter valfri:</span><span class="sxs-lookup"><span data-stu-id="26a75-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="26a75-177">Om du inte anger den här parametern och den här cmdleten importerar en fil som har namns tillägget. BYOK importeras den till en HSM-skyddad nycklar.</span><span class="sxs-lookup"><span data-stu-id="26a75-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="26a75-178">Cmdleten kan inte importera den här tangenten som program skyddad.</span><span class="sxs-lookup"><span data-stu-id="26a75-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="26a75-179">Om du inte anger den här parametern och den här cmdleten importerar en fil med namn tillägget. pfx importeras den som en programskyddad Server.</span><span class="sxs-lookup"><span data-stu-id="26a75-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-180">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="26a75-180">-Disable</span></span>
<span data-ttu-id="26a75-181">Visar att den aktuella knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="26a75-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="26a75-182">Alla försök att använda den här knappen fungerar inte.</span><span class="sxs-lookup"><span data-stu-id="26a75-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="26a75-183">Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.</span><span class="sxs-lookup"><span data-stu-id="26a75-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="26a75-184">-Upphör</span><span class="sxs-lookup"><span data-stu-id="26a75-184">-Expires</span></span>
<span data-ttu-id="26a75-185">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="26a75-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="26a75-186">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="26a75-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="26a75-187">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="26a75-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="26a75-188">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="26a75-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="26a75-189">Om du inte anger den här parametern upphör inte den att gälla.</span><span class="sxs-lookup"><span data-stu-id="26a75-189">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26a75-190">-InputObject</span></span>
<span data-ttu-id="26a75-191">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="26a75-191">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="26a75-192">-KeyFilePassword</span></span>
<span data-ttu-id="26a75-193">Anger ett lösen ord för den importerade filen som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="26a75-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="26a75-194">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="26a75-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="26a75-195">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="26a75-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="26a75-196">Du måste ange lösen ordet för att importera en fil med fil namns tillägget. pfx.</span><span class="sxs-lookup"><span data-stu-id="26a75-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-197">-Fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="26a75-197">-KeyFilePath</span></span>
<span data-ttu-id="26a75-198">Anger sökvägen till en lokal fil som innehåller nyckel material som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="26a75-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="26a75-199">De giltiga fil namns tilläggen är. BYOK och. pfx.</span><span class="sxs-lookup"><span data-stu-id="26a75-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="26a75-200">Om filen är en. BYOK-fil skyddas tangenten automatiskt av HSMs efter importen och du kan inte åsidosätta denna standard.</span><span class="sxs-lookup"><span data-stu-id="26a75-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="26a75-201">Om filen är en. pfx-fil skyddas den automatiskt av program vara efter importen.</span><span class="sxs-lookup"><span data-stu-id="26a75-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="26a75-202">Om du vill åsidosätta denna standard ställer du in *mål* parametern på HSM så att tangenten är HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="26a75-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="26a75-203">Om du anger den här parametern är *mål* parametern valfri.</span><span class="sxs-lookup"><span data-stu-id="26a75-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="26a75-204">-KeyOps</span></span>
<span data-ttu-id="26a75-205">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="26a75-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="26a75-206">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="26a75-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="26a75-207">De acceptabla värdena för den här parametern är en kommaavgränsad lista med viktiga åtgärder som definieras av [JSON Web Key (JWK)-specifikationen](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="26a75-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="26a75-208">inträffade</span><span class="sxs-lookup"><span data-stu-id="26a75-208">encrypt</span></span>
- <span data-ttu-id="26a75-209">dekryptera</span><span class="sxs-lookup"><span data-stu-id="26a75-209">decrypt</span></span>
- <span data-ttu-id="26a75-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="26a75-210">wrapKey</span></span>
- <span data-ttu-id="26a75-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="26a75-211">unwrapKey</span></span>
- <span data-ttu-id="26a75-212">Logga in</span><span class="sxs-lookup"><span data-stu-id="26a75-212">sign</span></span>
- <span data-ttu-id="26a75-213">kontroll</span><span class="sxs-lookup"><span data-stu-id="26a75-213">verify</span></span>
- <span data-ttu-id="26a75-214">Importera (endast för KEK, se exempel 7)</span><span class="sxs-lookup"><span data-stu-id="26a75-214">import (for KEK only, see example 7)</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-215">-Namn</span><span class="sxs-lookup"><span data-stu-id="26a75-215">-Name</span></span>
<span data-ttu-id="26a75-216">Anger namnet på den som ska läggas till i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="26a75-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="26a75-217">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="26a75-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="26a75-218">Namnet måste vara en sträng på mellan 1 och 63 tecken som bara innehåller 0-9, a-z, A-Z och-(streck symbolen).</span><span class="sxs-lookup"><span data-stu-id="26a75-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="26a75-219">-NotBefore</span></span>
<span data-ttu-id="26a75-220">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="26a75-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="26a75-221">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="26a75-221">This parameter uses UTC.</span></span> <span data-ttu-id="26a75-222">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="26a75-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="26a75-223">Om du inte anger den här parametern kan du använda den direkt.</span><span class="sxs-lookup"><span data-stu-id="26a75-223">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26a75-224">-ResourceId</span></span>
<span data-ttu-id="26a75-225">Valv resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="26a75-225">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-226">-Storlek</span><span class="sxs-lookup"><span data-stu-id="26a75-226">-Size</span></span>
<span data-ttu-id="26a75-227">RSA-nyckelbaserad storlek, i bitar.</span><span class="sxs-lookup"><span data-stu-id="26a75-227">RSA key size, in bits.</span></span> <span data-ttu-id="26a75-228">Om det inte anges ger tjänsten ett säkert standardvärde.</span><span class="sxs-lookup"><span data-stu-id="26a75-228">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-229">-Tagg</span><span class="sxs-lookup"><span data-stu-id="26a75-229">-Tag</span></span>
<span data-ttu-id="26a75-230">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="26a75-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26a75-231">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="26a75-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="26a75-232">-VaultName</span></span>
<span data-ttu-id="26a75-233">Anger namnet på det nyckelord som den här cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="26a75-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="26a75-234">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="26a75-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a75-235">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26a75-235">-Confirm</span></span>
<span data-ttu-id="26a75-236">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26a75-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a75-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a75-237">-WhatIf</span></span>
<span data-ttu-id="26a75-238">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26a75-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a75-239">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26a75-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a75-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a75-240">CommonParameters</span></span>
<span data-ttu-id="26a75-241">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a75-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a75-242">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26a75-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a75-243">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26a75-243">INPUTS</span></span>

### <span data-ttu-id="26a75-244">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="26a75-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="26a75-245">System. String</span><span class="sxs-lookup"><span data-stu-id="26a75-245">System.String</span></span>

## <span data-ttu-id="26a75-246">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26a75-246">OUTPUTS</span></span>

### <span data-ttu-id="26a75-247">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26a75-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="26a75-248">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26a75-248">NOTES</span></span>

## <span data-ttu-id="26a75-249">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26a75-249">RELATED LINKS</span></span>

[<span data-ttu-id="26a75-250">Säkerhets kopiering-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26a75-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="26a75-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26a75-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="26a75-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26a75-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="26a75-253">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="26a75-253">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
