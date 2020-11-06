---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 153cd3099b750732e281992e98cdafb173a71276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580423"
---
# <span data-ttu-id="077fa-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="077fa-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="077fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="077fa-102">SYNOPSIS</span></span>
<span data-ttu-id="077fa-103">Skapar en Key i ett nyckelord eller importerar en Key till ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="077fa-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="077fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="077fa-104">SYNTAX</span></span>

### <span data-ttu-id="077fa-105">InteractiveCreate (standard)</span><span class="sxs-lookup"><span data-stu-id="077fa-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077fa-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="077fa-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077fa-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="077fa-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077fa-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="077fa-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077fa-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="077fa-109">DESCRIPTION</span></span>
<span data-ttu-id="077fa-110">Cmdleten **Add-AzureKeyVaultKey** skapar en Key i ett nyckelord i ett nyckeltal i Azure Key Vault, eller importerar en till en Key Vault.</span><span class="sxs-lookup"><span data-stu-id="077fa-110">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="077fa-111">Använd denna cmdlet för att lägga till nycklar på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="077fa-111">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="077fa-112">Skapa en knapp i en maskinvarubaserad säkerhetsmodul (HSM) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="077fa-112">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="077fa-113">Skapa en under program vara i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="077fa-113">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="077fa-114">Importera en knapp från din egen Hardware säkerhetsmodul (HSM) till HSMs i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="077fa-114">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="077fa-115">Importera en från en. pfx-fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="077fa-115">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="077fa-116">Importera en knapp från en. pfx-fil på datorn till HSMs (Hardware Security modules) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="077fa-116">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="077fa-117">Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="077fa-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="077fa-118">Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i ditt nyckelord uppdateras den ursprungliga tangenten med de värden som du anger för den nya.</span><span class="sxs-lookup"><span data-stu-id="077fa-118">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="077fa-119">Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="077fa-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="077fa-120">Mer information om nyckel versioner och URI-strukturen finns i [om nycklar andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) i nyckel VALVETS REST API-dokumentation.</span><span class="sxs-lookup"><span data-stu-id="077fa-120">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="077fa-121">Obs! Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="077fa-121">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="077fa-122">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="077fa-122">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="077fa-123">Vi rekommenderar att du säkerhetskopierar din-tangenten efter att den har skapats eller uppdaterats genom att använda Backup-AzureKeyVaultKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077fa-123">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="077fa-124">Det finns inga funktioner för att ångra borttagning, så om du råkar ta bort en eller flera rader och sedan ändrar dig kan du inte återställa den, såvida du inte har en säkerhets kopia av den.</span><span class="sxs-lookup"><span data-stu-id="077fa-124">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="077fa-125">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="077fa-125">EXAMPLES</span></span>

### <span data-ttu-id="077fa-126">Exempel 1: skapa en-tangenten</span><span class="sxs-lookup"><span data-stu-id="077fa-126">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="077fa-127">Det här kommandot skapar en programskyddad nycklar med namnet ITSoftware i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="077fa-127">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="077fa-128">Exempel 2: skapa en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="077fa-128">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="077fa-129">Det här kommandot skapar en HSM-skyddad nycklar i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="077fa-129">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="077fa-130">Exempel 3: skapa en transparens med icke-standardvärden</span><span class="sxs-lookup"><span data-stu-id="077fa-130">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="077fa-131">Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.</span><span class="sxs-lookup"><span data-stu-id="077fa-131">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="077fa-132">Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="077fa-132">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="077fa-133">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="077fa-133">That object specifies a time two years in the future.</span></span> <span data-ttu-id="077fa-134">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="077fa-134">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="077fa-135">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="077fa-135">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="077fa-136">Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="077fa-136">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="077fa-137">Det objektet anger den aktuella UTC-tiden.</span><span class="sxs-lookup"><span data-stu-id="077fa-137">That object specifies current UTC time.</span></span> <span data-ttu-id="077fa-138">I kommandot lagras datumet i $NotBefore variabel.</span><span class="sxs-lookup"><span data-stu-id="077fa-138">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="077fa-139">Med kommandot slut skapas en Key med namnet ITHsmNonDefault som är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="077fa-139">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="077fa-140">Kommandot anger värden för tillåtna operationer som lagras $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="077fa-140">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="077fa-141">Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="077fa-141">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="077fa-142">Den nya knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="077fa-142">The new key is disabled.</span></span> <span data-ttu-id="077fa-143">Du kan aktivera den med cmdleten **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="077fa-143">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="077fa-144">Exempel 4: importera en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="077fa-144">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="077fa-145">Det här kommandot importerar den nycklar som heter ITByok från platsen som parametern för *fil Sök vägen* anger.</span><span class="sxs-lookup"><span data-stu-id="077fa-145">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="077fa-146">Den importerade knappen är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="077fa-146">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="077fa-147">Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="077fa-147">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="077fa-148">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="077fa-148">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="077fa-149">Exempel 5: importera en skyddad program vara</span><span class="sxs-lookup"><span data-stu-id="077fa-149">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="077fa-150">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="077fa-150">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="077fa-151">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="077fa-151">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="077fa-152">Det andra kommandot skapar ett program varu lösen ord i ett contoso-valv.</span><span class="sxs-lookup"><span data-stu-id="077fa-152">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="077fa-153">Kommandot anger platsen för den och det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="077fa-153">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="077fa-154">Exempel 6: importera en nycklar och tilldela attribut</span><span class="sxs-lookup"><span data-stu-id="077fa-154">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="077fa-155">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="077fa-155">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="077fa-156">Det andra kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i $expires variabeln.</span><span class="sxs-lookup"><span data-stu-id="077fa-156">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="077fa-157">Det tredje kommandot skapar $tags variabel för att ställa in taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="077fa-157">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="077fa-158">Med kommandot slut importeras en nycklar som en HSM-tangenten från den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="077fa-158">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="077fa-159">Kommandot anger den förfallo tid som är lagrad i $Expires och lösen ord som lagras i $Password och tillämpar taggarna som lagras i $tags.</span><span class="sxs-lookup"><span data-stu-id="077fa-159">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="077fa-160">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="077fa-160">PARAMETERS</span></span>

### <span data-ttu-id="077fa-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077fa-161">-DefaultProfile</span></span>
<span data-ttu-id="077fa-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="077fa-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="077fa-163">-Mål</span><span class="sxs-lookup"><span data-stu-id="077fa-163">-Destination</span></span>
<span data-ttu-id="077fa-164">Anger om du vill lägga till en nycklar som en programvarubaserad eller en HSM-skyddad nycklar i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="077fa-164">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="077fa-165">Giltiga värden är: HSM och program vara.</span><span class="sxs-lookup"><span data-stu-id="077fa-165">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="077fa-166">Obs! Om du vill använda HSM som mål måste du ha ett huvud valv som stöder HSMs.</span><span class="sxs-lookup"><span data-stu-id="077fa-166">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="077fa-167">Mer information om tjänst nivåer och funktioner för Azure Key Vault finns på [webbplatsen för Azure Key Vault prissättning](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="077fa-167">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="077fa-168">Den här parametern är obligatorisk när du skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="077fa-168">This parameter is required when you create a new key.</span></span> <span data-ttu-id="077fa-169">Om du importerar en fil med parametern *sökväg* är denna parameter valfri:</span><span class="sxs-lookup"><span data-stu-id="077fa-169">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="077fa-170">Om du inte anger den här parametern och den här cmdleten importerar en fil som har namns tillägget. BYOK importeras den till en HSM-skyddad nycklar.</span><span class="sxs-lookup"><span data-stu-id="077fa-170">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="077fa-171">Cmdleten kan inte importera den här tangenten som program skyddad.</span><span class="sxs-lookup"><span data-stu-id="077fa-171">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="077fa-172">Om du inte anger den här parametern och den här cmdleten importerar en fil med namn tillägget. pfx importeras den som en programskyddad Server.</span><span class="sxs-lookup"><span data-stu-id="077fa-172">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InputObjectCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-173">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="077fa-173">-Disable</span></span>
<span data-ttu-id="077fa-174">Visar att den aktuella knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="077fa-174">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="077fa-175">Alla försök att använda den här knappen fungerar inte.</span><span class="sxs-lookup"><span data-stu-id="077fa-175">Any attempt to use the key will fail.</span></span> <span data-ttu-id="077fa-176">Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.</span><span class="sxs-lookup"><span data-stu-id="077fa-176">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="077fa-177">-Upphör</span><span class="sxs-lookup"><span data-stu-id="077fa-177">-Expires</span></span>
<span data-ttu-id="077fa-178">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="077fa-178">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="077fa-179">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="077fa-179">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="077fa-180">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="077fa-180">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="077fa-181">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="077fa-181">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="077fa-182">Om du inte anger den här parametern upphör inte den att gälla.</span><span class="sxs-lookup"><span data-stu-id="077fa-182">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-183">-InputObject</span><span class="sxs-lookup"><span data-stu-id="077fa-183">-InputObject</span></span>
<span data-ttu-id="077fa-184">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="077fa-184">Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-185">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="077fa-185">-KeyFilePassword</span></span>
<span data-ttu-id="077fa-186">Anger ett lösen ord för den importerade filen som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="077fa-186">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="077fa-187">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="077fa-187">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="077fa-188">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="077fa-188">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="077fa-189">Du måste ange lösen ordet för att importera en fil med fil namns tillägget. pfx.</span><span class="sxs-lookup"><span data-stu-id="077fa-189">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-190">-Fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="077fa-190">-KeyFilePath</span></span>
<span data-ttu-id="077fa-191">Anger sökvägen till en lokal fil som innehåller nyckel material som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="077fa-191">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="077fa-192">De giltiga fil namns tilläggen är. BYOK och. pfx.</span><span class="sxs-lookup"><span data-stu-id="077fa-192">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="077fa-193">Om filen är en. BYOK-fil skyddas tangenten automatiskt av HSMs efter importen och du kan inte åsidosätta denna standard.</span><span class="sxs-lookup"><span data-stu-id="077fa-193">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="077fa-194">Om filen är en. pfx-fil skyddas den automatiskt av program vara efter importen.</span><span class="sxs-lookup"><span data-stu-id="077fa-194">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="077fa-195">Om du vill åsidosätta denna standard ställer du in *mål* parametern på HSM så att tangenten är HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="077fa-195">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="077fa-196">Om du anger den här parametern är *mål* parametern valfri.</span><span class="sxs-lookup"><span data-stu-id="077fa-196">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-197">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="077fa-197">-KeyOps</span></span>
<span data-ttu-id="077fa-198">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="077fa-198">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="077fa-199">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="077fa-199">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="077fa-200">De acceptabla värdena för den här parametern är en kommaavgränsad lista med viktiga åtgärder som definieras av [JSON Web Key (JWK)-specifikationen](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="077fa-200">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="077fa-201">Inträffade</span><span class="sxs-lookup"><span data-stu-id="077fa-201">Encrypt</span></span>
- <span data-ttu-id="077fa-202">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="077fa-202">Decrypt</span></span>
- <span data-ttu-id="077fa-203">Ska</span><span class="sxs-lookup"><span data-stu-id="077fa-203">Wrap</span></span>
- <span data-ttu-id="077fa-204">Unwrap</span><span class="sxs-lookup"><span data-stu-id="077fa-204">Unwrap</span></span>
- <span data-ttu-id="077fa-205">Logga in</span><span class="sxs-lookup"><span data-stu-id="077fa-205">Sign</span></span>
- <span data-ttu-id="077fa-206">Kontroll</span><span class="sxs-lookup"><span data-stu-id="077fa-206">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-207">-Namn</span><span class="sxs-lookup"><span data-stu-id="077fa-207">-Name</span></span>
<span data-ttu-id="077fa-208">Anger namnet på den som ska läggas till i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="077fa-208">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="077fa-209">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="077fa-209">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="077fa-210">Namnet måste vara en sträng på mellan 1 och 63 tecken som bara innehåller 0-9, a-z, A-Z och-(streck symbolen).</span><span class="sxs-lookup"><span data-stu-id="077fa-210">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-211">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="077fa-211">-NotBefore</span></span>
<span data-ttu-id="077fa-212">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="077fa-212">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="077fa-213">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="077fa-213">This parameter uses UTC.</span></span> <span data-ttu-id="077fa-214">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="077fa-214">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="077fa-215">Om du inte anger den här parametern kan du använda den direkt.</span><span class="sxs-lookup"><span data-stu-id="077fa-215">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-216">-Tagg</span><span class="sxs-lookup"><span data-stu-id="077fa-216">-Tag</span></span>
<span data-ttu-id="077fa-217">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="077fa-217">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="077fa-218">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="077fa-218">For example:</span></span>

<span data-ttu-id="077fa-219">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="077fa-219">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-220">-VaultName</span><span class="sxs-lookup"><span data-stu-id="077fa-220">-VaultName</span></span>
<span data-ttu-id="077fa-221">Anger namnet på det nyckelord som den här cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="077fa-221">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="077fa-222">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="077fa-222">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fa-223">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="077fa-223">-Confirm</span></span>
<span data-ttu-id="077fa-224">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="077fa-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077fa-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077fa-225">-WhatIf</span></span>
<span data-ttu-id="077fa-226">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="077fa-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077fa-227">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="077fa-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077fa-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077fa-228">CommonParameters</span></span>
<span data-ttu-id="077fa-229">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077fa-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077fa-230">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077fa-230">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077fa-231">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="077fa-231">INPUTS</span></span>

### <span data-ttu-id="077fa-232">Ingen</span><span class="sxs-lookup"><span data-stu-id="077fa-232">None</span></span>
<span data-ttu-id="077fa-233">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="077fa-233">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="077fa-234">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="077fa-234">OUTPUTS</span></span>

### <span data-ttu-id="077fa-235">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="077fa-235">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="077fa-236">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="077fa-236">NOTES</span></span>

## <span data-ttu-id="077fa-237">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="077fa-237">RELATED LINKS</span></span>

[<span data-ttu-id="077fa-238">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="077fa-238">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="077fa-239">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="077fa-239">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="077fa-240">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="077fa-240">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="077fa-241">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="077fa-241">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
