---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: c363f32b8c28b2e6f83f4e065c677926800d04b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757883"
---
# <span data-ttu-id="bf54a-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf54a-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="bf54a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf54a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf54a-103">Skapar en Key i ett nyckelord eller importerar en Key till ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bf54a-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf54a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf54a-104">SYNTAX</span></span>

### <span data-ttu-id="bf54a-105">InteractiveCreate (standard)</span><span class="sxs-lookup"><span data-stu-id="bf54a-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf54a-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="bf54a-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf54a-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="bf54a-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf54a-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="bf54a-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf54a-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="bf54a-109">ResourceIdCreate</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf54a-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="bf54a-110">ResourceIdImport</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf54a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf54a-111">DESCRIPTION</span></span>
<span data-ttu-id="bf54a-112">Cmdleten **Add-AzureKeyVaultKey** skapar en Key i ett nyckelord i ett nyckeltal i Azure Key Vault, eller importerar en till en Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bf54a-112">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="bf54a-113">Använd denna cmdlet för att lägga till nycklar på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="bf54a-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="bf54a-114">Skapa en knapp i en maskinvarubaserad säkerhetsmodul (HSM) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="bf54a-115">Skapa en under program vara i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="bf54a-116">Importera en knapp från din egen Hardware säkerhetsmodul (HSM) till HSMs i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="bf54a-117">Importera en från en. pfx-fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="bf54a-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="bf54a-118">Importera en knapp från en. pfx-fil på datorn till HSMs (Hardware Security modules) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="bf54a-119">Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="bf54a-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="bf54a-120">Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i ditt nyckelord uppdateras den ursprungliga tangenten med de värden som du anger för den nya.</span><span class="sxs-lookup"><span data-stu-id="bf54a-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="bf54a-121">Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="bf54a-122">Mer information om nyckel versioner och URI-strukturen finns i [om nycklar och hemligheter](https://go.microsoft.com/fwlink/?linkid=518560) i övriga API-dokumentation för nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="bf54a-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="bf54a-123">Obs! Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="bf54a-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="bf54a-124">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="bf54a-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="bf54a-125">Vi rekommenderar att du säkerhetskopierar din-tangenten efter att den har skapats eller uppdaterats genom att använda Backup-AzureKeyVaultKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf54a-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="bf54a-126">Det finns inga funktioner för att ångra borttagning, så om du råkar ta bort en eller flera rader och sedan ändrar dig kan du inte återställa den, såvida du inte har en säkerhets kopia av den.</span><span class="sxs-lookup"><span data-stu-id="bf54a-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="bf54a-127">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf54a-127">EXAMPLES</span></span>

### <span data-ttu-id="bf54a-128">Exempel 1: skapa en-tangenten</span><span class="sxs-lookup"><span data-stu-id="bf54a-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

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

<span data-ttu-id="bf54a-129">Det här kommandot skapar en programskyddad nycklar med namnet ITSoftware i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="bf54a-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="bf54a-130">Exempel 2: skapa en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="bf54a-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

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

<span data-ttu-id="bf54a-131">Det här kommandot skapar en HSM-skyddad nycklar i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="bf54a-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="bf54a-132">Exempel 3: skapa en transparens med icke-standardvärden</span><span class="sxs-lookup"><span data-stu-id="bf54a-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

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

<span data-ttu-id="bf54a-133">Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.</span><span class="sxs-lookup"><span data-stu-id="bf54a-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="bf54a-134">Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="bf54a-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="bf54a-135">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="bf54a-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="bf54a-136">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="bf54a-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="bf54a-137">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bf54a-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="bf54a-138">Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="bf54a-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="bf54a-139">Det objektet anger den aktuella UTC-tiden.</span><span class="sxs-lookup"><span data-stu-id="bf54a-139">That object specifies current UTC time.</span></span> <span data-ttu-id="bf54a-140">I kommandot lagras datumet i $NotBefore variabel.</span><span class="sxs-lookup"><span data-stu-id="bf54a-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="bf54a-141">Med kommandot slut skapas en Key med namnet ITHsmNonDefault som är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="bf54a-142">Kommandot anger värden för tillåtna operationer som lagras $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="bf54a-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="bf54a-143">Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="bf54a-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="bf54a-144">Den nya knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-144">The new key is disabled.</span></span> <span data-ttu-id="bf54a-145">Du kan aktivera den med cmdleten **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="bf54a-145">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="bf54a-146">Exempel 4: importera en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="bf54a-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

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

<span data-ttu-id="bf54a-147">Det här kommandot importerar den nycklar som heter ITByok från platsen som parametern för *fil Sök vägen* anger.</span><span class="sxs-lookup"><span data-stu-id="bf54a-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="bf54a-148">Den importerade knappen är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="bf54a-149">Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="bf54a-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="bf54a-150">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="bf54a-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="bf54a-151">Exempel 5: importera en skyddad program vara</span><span class="sxs-lookup"><span data-stu-id="bf54a-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

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

<span data-ttu-id="bf54a-152">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="bf54a-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="bf54a-153">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bf54a-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bf54a-154">Det andra kommandot skapar ett program varu lösen ord i ett contoso-valv.</span><span class="sxs-lookup"><span data-stu-id="bf54a-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="bf54a-155">Kommandot anger platsen för den och det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="bf54a-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="bf54a-156">Exempel 6: importera en nycklar och tilldela attribut</span><span class="sxs-lookup"><span data-stu-id="bf54a-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

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

<span data-ttu-id="bf54a-157">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="bf54a-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="bf54a-158">Det andra kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i $expires variabeln.</span><span class="sxs-lookup"><span data-stu-id="bf54a-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="bf54a-159">Det tredje kommandot skapar $tags variabel för att ställa in taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="bf54a-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="bf54a-160">Med kommandot slut importeras en nycklar som en HSM-tangenten från den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="bf54a-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="bf54a-161">Kommandot anger den förfallo tid som är lagrad i $Expires och lösen ord som lagras i $Password och tillämpar taggarna som lagras i $tags.</span><span class="sxs-lookup"><span data-stu-id="bf54a-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="bf54a-162">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf54a-162">PARAMETERS</span></span>

### <span data-ttu-id="bf54a-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf54a-163">-DefaultProfile</span></span>
<span data-ttu-id="bf54a-164">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf54a-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf54a-165">-Mål</span><span class="sxs-lookup"><span data-stu-id="bf54a-165">-Destination</span></span>
<span data-ttu-id="bf54a-166">Anger om du vill lägga till en nycklar som en programvarubaserad eller en HSM-skyddad nycklar i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="bf54a-167">Giltiga värden är: HSM och program vara.</span><span class="sxs-lookup"><span data-stu-id="bf54a-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="bf54a-168">Obs! Om du vill använda HSM som mål måste du ha ett huvud valv som stöder HSMs.</span><span class="sxs-lookup"><span data-stu-id="bf54a-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="bf54a-169">Mer information om tjänst nivåer och funktioner för Azure Key Vault finns på [webbplatsen för Azure Key Vault prissättning](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="bf54a-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="bf54a-170">Den här parametern är obligatorisk när du skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="bf54a-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="bf54a-171">Om du importerar en fil med parametern *sökväg* är denna parameter valfri:</span><span class="sxs-lookup"><span data-stu-id="bf54a-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="bf54a-172">Om du inte anger den här parametern och den här cmdleten importerar en fil som har namns tillägget. BYOK importeras den till en HSM-skyddad nycklar.</span><span class="sxs-lookup"><span data-stu-id="bf54a-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="bf54a-173">Cmdleten kan inte importera den här tangenten som program skyddad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="bf54a-174">Om du inte anger den här parametern och den här cmdleten importerar en fil med namn tillägget. pfx importeras den som en programskyddad Server.</span><span class="sxs-lookup"><span data-stu-id="bf54a-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="bf54a-175">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="bf54a-175">-Disable</span></span>
<span data-ttu-id="bf54a-176">Visar att den aktuella knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="bf54a-177">Alla försök att använda den här knappen fungerar inte.</span><span class="sxs-lookup"><span data-stu-id="bf54a-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="bf54a-178">Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.</span><span class="sxs-lookup"><span data-stu-id="bf54a-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="bf54a-179">-Upphör</span><span class="sxs-lookup"><span data-stu-id="bf54a-179">-Expires</span></span>
<span data-ttu-id="bf54a-180">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="bf54a-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="bf54a-181">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="bf54a-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="bf54a-182">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bf54a-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="bf54a-183">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bf54a-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="bf54a-184">Om du inte anger den här parametern upphör inte den att gälla.</span><span class="sxs-lookup"><span data-stu-id="bf54a-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="bf54a-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf54a-185">-InputObject</span></span>
<span data-ttu-id="bf54a-186">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="bf54a-186">Vault object.</span></span>

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

### <span data-ttu-id="bf54a-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="bf54a-187">-KeyFilePassword</span></span>
<span data-ttu-id="bf54a-188">Anger ett lösen ord för den importerade filen som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bf54a-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="bf54a-189">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="bf54a-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="bf54a-190">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bf54a-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="bf54a-191">Du måste ange lösen ordet för att importera en fil med fil namns tillägget. pfx.</span><span class="sxs-lookup"><span data-stu-id="bf54a-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="bf54a-192">-Fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="bf54a-192">-KeyFilePath</span></span>
<span data-ttu-id="bf54a-193">Anger sökvägen till en lokal fil som innehåller nyckel material som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="bf54a-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="bf54a-194">De giltiga fil namns tilläggen är. BYOK och. pfx.</span><span class="sxs-lookup"><span data-stu-id="bf54a-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="bf54a-195">Om filen är en. BYOK-fil skyddas tangenten automatiskt av HSMs efter importen och du kan inte åsidosätta denna standard.</span><span class="sxs-lookup"><span data-stu-id="bf54a-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="bf54a-196">Om filen är en. pfx-fil skyddas den automatiskt av program vara efter importen.</span><span class="sxs-lookup"><span data-stu-id="bf54a-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="bf54a-197">Om du vill åsidosätta denna standard ställer du in *mål* parametern på HSM så att tangenten är HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="bf54a-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="bf54a-198">Om du anger den här parametern är *mål* parametern valfri.</span><span class="sxs-lookup"><span data-stu-id="bf54a-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="bf54a-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="bf54a-199">-KeyOps</span></span>
<span data-ttu-id="bf54a-200">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="bf54a-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="bf54a-201">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="bf54a-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="bf54a-202">De acceptabla värdena för den här parametern är en kommaavgränsad lista med viktiga åtgärder som definieras av [JSON Web Key (JWK)-specifikationen](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="bf54a-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="bf54a-203">Inträffade</span><span class="sxs-lookup"><span data-stu-id="bf54a-203">Encrypt</span></span>
- <span data-ttu-id="bf54a-204">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="bf54a-204">Decrypt</span></span>
- <span data-ttu-id="bf54a-205">Ska</span><span class="sxs-lookup"><span data-stu-id="bf54a-205">Wrap</span></span>
- <span data-ttu-id="bf54a-206">Unwrap</span><span class="sxs-lookup"><span data-stu-id="bf54a-206">Unwrap</span></span>
- <span data-ttu-id="bf54a-207">Logga in</span><span class="sxs-lookup"><span data-stu-id="bf54a-207">Sign</span></span>
- <span data-ttu-id="bf54a-208">Kontroll</span><span class="sxs-lookup"><span data-stu-id="bf54a-208">Verify</span></span>

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

### <span data-ttu-id="bf54a-209">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf54a-209">-Name</span></span>
<span data-ttu-id="bf54a-210">Anger namnet på den som ska läggas till i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="bf54a-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="bf54a-211">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="bf54a-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="bf54a-212">Namnet måste vara en sträng på mellan 1 och 63 tecken som bara innehåller 0-9, a-z, A-Z och-(streck symbolen).</span><span class="sxs-lookup"><span data-stu-id="bf54a-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="bf54a-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="bf54a-213">-NotBefore</span></span>
<span data-ttu-id="bf54a-214">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="bf54a-215">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="bf54a-215">This parameter uses UTC.</span></span> <span data-ttu-id="bf54a-216">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bf54a-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="bf54a-217">Om du inte anger den här parametern kan du använda den direkt.</span><span class="sxs-lookup"><span data-stu-id="bf54a-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="bf54a-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf54a-218">-ResourceId</span></span>
<span data-ttu-id="bf54a-219">Valv resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bf54a-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="bf54a-220">-Storlek</span><span class="sxs-lookup"><span data-stu-id="bf54a-220">-Size</span></span>
<span data-ttu-id="bf54a-221">RSA-nyckelbaserad storlek, i bitar.</span><span class="sxs-lookup"><span data-stu-id="bf54a-221">RSA key size, in bits.</span></span> <span data-ttu-id="bf54a-222">Om det inte anges ger tjänsten ett säkert standardvärde.</span><span class="sxs-lookup"><span data-stu-id="bf54a-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="bf54a-223">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bf54a-223">-Tag</span></span>
<span data-ttu-id="bf54a-224">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bf54a-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bf54a-225">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="bf54a-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bf54a-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bf54a-226">-VaultName</span></span>
<span data-ttu-id="bf54a-227">Anger namnet på det nyckelord som den här cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="bf54a-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="bf54a-228">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="bf54a-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="bf54a-229">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf54a-229">-Confirm</span></span>
<span data-ttu-id="bf54a-230">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf54a-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf54a-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf54a-231">-WhatIf</span></span>
<span data-ttu-id="bf54a-232">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf54a-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf54a-233">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf54a-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf54a-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf54a-234">CommonParameters</span></span>
<span data-ttu-id="bf54a-235">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf54a-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf54a-236">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf54a-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf54a-237">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf54a-237">INPUTS</span></span>

### <span data-ttu-id="bf54a-238">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bf54a-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="bf54a-239">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf54a-239">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="bf54a-240">System. String</span><span class="sxs-lookup"><span data-stu-id="bf54a-240">System.String</span></span>

## <span data-ttu-id="bf54a-241">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf54a-241">OUTPUTS</span></span>

### <span data-ttu-id="bf54a-242">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf54a-242">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="bf54a-243">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf54a-243">NOTES</span></span>

## <span data-ttu-id="bf54a-244">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf54a-244">RELATED LINKS</span></span>

[<span data-ttu-id="bf54a-245">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf54a-245">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="bf54a-246">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf54a-246">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="bf54a-247">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf54a-247">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="bf54a-248">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="bf54a-248">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
