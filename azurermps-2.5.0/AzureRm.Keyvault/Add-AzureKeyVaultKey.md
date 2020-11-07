---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7af5afeac742bf9d256ac16470af0169170eb1e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928838"
---
# <span data-ttu-id="9e0fa-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9e0fa-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="9e0fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0fa-103">Skapar en Key i ett nyckelord eller importerar en Key till ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e0fa-104">SYNTAX</span></span>

### <span data-ttu-id="9e0fa-105">Skapa (standard)</span><span class="sxs-lookup"><span data-stu-id="9e0fa-105">Create (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e0fa-106">Importeras</span><span class="sxs-lookup"><span data-stu-id="9e0fa-106">Import</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e0fa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e0fa-107">DESCRIPTION</span></span>
<span data-ttu-id="9e0fa-108">Cmdleten **Add-AzureKeyVaultKey** skapar en Key i ett nyckelord i ett nyckeltal i Azure Key Vault, eller importerar en till en Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-108">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="9e0fa-109">Använd denna cmdlet för att lägga till nycklar på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="9e0fa-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="9e0fa-110">Skapa en knapp i en maskinvarubaserad säkerhetsmodul (HSM) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="9e0fa-111">Skapa en under program vara i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="9e0fa-112">Importera en knapp från din egen Hardware säkerhetsmodul (HSM) till HSMs i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="9e0fa-113">Importera en från en. pfx-fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="9e0fa-114">Importera en knapp från en. pfx-fil på datorn till HSMs (Hardware Security modules) i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="9e0fa-115">Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="9e0fa-116">Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i ditt nyckelord uppdateras den ursprungliga tangenten med de värden som du anger för den nya.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="9e0fa-117">Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="9e0fa-118">Mer information om nyckel versioner och URI-strukturen finns i [om nycklar andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) i nyckel VALVETS REST API-dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-118">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="9e0fa-119">Obs! Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="9e0fa-120">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="9e0fa-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="9e0fa-121">Vi rekommenderar att du säkerhetskopierar din-tangenten efter att den har skapats eller uppdaterats genom att använda Backup-AzureKeyVaultKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="9e0fa-122">Det finns inga funktioner för att ångra borttagning, så om du råkar ta bort en eller flera rader och sedan ändrar dig kan du inte återställa den, såvida du inte har en säkerhets kopia av den.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="9e0fa-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e0fa-123">EXAMPLES</span></span>

### <span data-ttu-id="9e0fa-124">Exempel 1: skapa en-tangenten</span><span class="sxs-lookup"><span data-stu-id="9e0fa-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="9e0fa-125">Det här kommandot skapar en programskyddad nycklar med namnet ITSoftware i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="9e0fa-126">Exempel 2: skapa en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="9e0fa-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="9e0fa-127">Det här kommandot skapar en HSM-skyddad nycklar i det nyckelord som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="9e0fa-128">Exempel 3: skapa en transparens med icke-standardvärden</span><span class="sxs-lookup"><span data-stu-id="9e0fa-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="9e0fa-129">Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="9e0fa-130">Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="9e0fa-131">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="9e0fa-132">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="9e0fa-133">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9e0fa-134">Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9e0fa-135">Det objektet anger den aktuella UTC-tiden.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-135">That object specifies current UTC time.</span></span> <span data-ttu-id="9e0fa-136">I kommandot lagras datumet i $NotBefore variabel.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="9e0fa-137">Med kommandot slut skapas en Key med namnet ITHsmNonDefault som är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="9e0fa-138">Kommandot anger värden för tillåtna operationer som lagras $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="9e0fa-139">Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="9e0fa-140">Den nya knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-140">The new key is disabled.</span></span> <span data-ttu-id="9e0fa-141">Du kan aktivera den med cmdleten **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-141">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="9e0fa-142">Exempel 4: importera en HSM-skyddad nycklar</span><span class="sxs-lookup"><span data-stu-id="9e0fa-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="9e0fa-143">Det här kommandot importerar den nycklar som heter ITByok från platsen som parametern för *fil Sök vägen* anger.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="9e0fa-144">Den importerade knappen är en HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="9e0fa-145">Du måste först skapa ett BYOK-paket (en fil med fil namns tillägget. BYOK) med hjälp av BYOK-verktyg för Azure Key valv för att importera en nyckeln från din egen säkerhets modul för maskin vara.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="9e0fa-146">Mer information finns i [hur du skapar och överför HSM-Protected nycklar för Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="9e0fa-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="9e0fa-147">Exempel 5: importera en skyddad program vara</span><span class="sxs-lookup"><span data-stu-id="9e0fa-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="9e0fa-148">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="9e0fa-149">Om du vill ha mer information skriver du `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="9e0fa-150">Det andra kommandot skapar ett program varu lösen ord i ett contoso-valv.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="9e0fa-151">Kommandot anger platsen för den och det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="9e0fa-152">Exempel 6: importera en nycklar och tilldela attribut</span><span class="sxs-lookup"><span data-stu-id="9e0fa-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="9e0fa-153">Det första kommandot konverterar en sträng till en skyddad sträng med hjälp av cmdleten **ConvertTo-SecureString** och lagrar sedan strängen i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="9e0fa-154">Det andra kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i $expires variabeln.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="9e0fa-155">Det tredje kommandot skapar $tags variabel för att ställa in taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="9e0fa-156">Med kommandot slut importeras en nycklar som en HSM-tangenten från den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="9e0fa-157">Kommandot anger den förfallo tid som är lagrad i $Expires och lösen ord som lagras i $Password och tillämpar taggarna som lagras i $tags.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="9e0fa-158">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e0fa-158">PARAMETERS</span></span>

### <span data-ttu-id="9e0fa-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0fa-159">-DefaultProfile</span></span>
<span data-ttu-id="9e0fa-160">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9e0fa-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e0fa-161">-Mål</span><span class="sxs-lookup"><span data-stu-id="9e0fa-161">-Destination</span></span>
<span data-ttu-id="9e0fa-162">Anger om du vill lägga till en nycklar som en programvarubaserad eller en HSM-skyddad nycklar i Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="9e0fa-163">Giltiga värden är: HSM och program vara.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="9e0fa-164">Obs! Om du vill använda HSM som mål måste du ha ett huvud valv som stöder HSMs.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="9e0fa-165">Mer information om tjänst nivåer och funktioner för Azure Key Vault finns på [webbplatsen för Azure Key Vault prissättning](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="9e0fa-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="9e0fa-166">Den här parametern är obligatorisk när du skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="9e0fa-167">Om du importerar en fil med parametern *sökväg* är denna parameter valfri:</span><span class="sxs-lookup"><span data-stu-id="9e0fa-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="9e0fa-168">Om du inte anger den här parametern och den här cmdleten importerar en fil som har namns tillägget. BYOK importeras den till en HSM-skyddad nycklar.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="9e0fa-169">Cmdleten kan inte importera den här tangenten som program skyddad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="9e0fa-170">Om du inte anger den här parametern och den här cmdleten importerar en fil med namn tillägget. pfx importeras den som en programskyddad Server.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
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
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e0fa-171">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="9e0fa-171">-Disable</span></span>
<span data-ttu-id="9e0fa-172">Visar att den aktuella knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="9e0fa-173">Alla försök att använda den här knappen fungerar inte.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="9e0fa-174">Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="9e0fa-175">-Upphör</span><span class="sxs-lookup"><span data-stu-id="9e0fa-175">-Expires</span></span>
<span data-ttu-id="9e0fa-176">Anger förfallo tid, som ett **datetime** -objekt, för den Key som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="9e0fa-177">Den här parametern använder koordinerad Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="9e0fa-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9e0fa-178">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9e0fa-179">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="9e0fa-180">Om du inte anger den här parametern upphör inte den att gälla.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-180">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="9e0fa-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="9e0fa-181">-KeyFilePassword</span></span>
<span data-ttu-id="9e0fa-182">Anger ett lösen ord för den importerade filen som ett **SecureString** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="9e0fa-183">För att få ett **SecureString** -objekt, Använd cmdleten **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="9e0fa-184">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="9e0fa-185">Du måste ange lösen ordet för att importera en fil med fil namns tillägget. pfx.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e0fa-186">-Fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="9e0fa-186">-KeyFilePath</span></span>
<span data-ttu-id="9e0fa-187">Anger sökvägen till en lokal fil som innehåller nyckel material som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="9e0fa-188">De giltiga fil namns tilläggen är. BYOK och. pfx.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="9e0fa-189">Om filen är en. BYOK-fil skyddas tangenten automatiskt av HSMs efter importen och du kan inte åsidosätta denna standard.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="9e0fa-190">Om filen är en. pfx-fil skyddas den automatiskt av program vara efter importen.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="9e0fa-191">Om du vill åsidosätta denna standard ställer du in *mål* parametern på HSM så att tangenten är HSM-skyddad.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="9e0fa-192">Om du anger den här parametern är *mål* parametern valfri.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e0fa-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="9e0fa-193">-KeyOps</span></span>
<span data-ttu-id="9e0fa-194">Anger en matris med åtgärder som kan utföras med hjälp av den här cmdleten som läggs till.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="9e0fa-195">Om du inte anger den här parametern kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="9e0fa-196">De acceptabla värdena för den här parametern är en kommaavgränsad lista med viktiga åtgärder som definieras av [JSON Web Key (JWK)-specifikationen](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="9e0fa-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="9e0fa-197">Inträffade</span><span class="sxs-lookup"><span data-stu-id="9e0fa-197">Encrypt</span></span>
- <span data-ttu-id="9e0fa-198">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="9e0fa-198">Decrypt</span></span>
- <span data-ttu-id="9e0fa-199">Ska</span><span class="sxs-lookup"><span data-stu-id="9e0fa-199">Wrap</span></span>
- <span data-ttu-id="9e0fa-200">Unwrap</span><span class="sxs-lookup"><span data-stu-id="9e0fa-200">Unwrap</span></span>
- <span data-ttu-id="9e0fa-201">Logga in</span><span class="sxs-lookup"><span data-stu-id="9e0fa-201">Sign</span></span>
- <span data-ttu-id="9e0fa-202">Kontroll</span><span class="sxs-lookup"><span data-stu-id="9e0fa-202">Verify</span></span>

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

### <span data-ttu-id="9e0fa-203">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e0fa-203">-Name</span></span>
<span data-ttu-id="9e0fa-204">Anger namnet på den som ska läggas till i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="9e0fa-205">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="9e0fa-206">Namnet måste vara en sträng på mellan 1 och 63 tecken som bara innehåller 0-9, a-z, A-Z och-(streck symbolen).</span><span class="sxs-lookup"><span data-stu-id="9e0fa-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="9e0fa-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9e0fa-207">-NotBefore</span></span>
<span data-ttu-id="9e0fa-208">Anger tiden, som ett **datetime** -objekt, innan det inte går att använda tangenten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="9e0fa-209">Den här parametern använder UTC.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-209">This parameter uses UTC.</span></span> <span data-ttu-id="9e0fa-210">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9e0fa-211">Om du inte anger den här parametern kan du använda den direkt.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-211">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="9e0fa-212">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9e0fa-212">-Tag</span></span>
<span data-ttu-id="9e0fa-213">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e0fa-214">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="9e0fa-214">For example:</span></span>

<span data-ttu-id="9e0fa-215">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9e0fa-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e0fa-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9e0fa-216">-VaultName</span></span>
<span data-ttu-id="9e0fa-217">Anger namnet på det nyckelord som den här cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="9e0fa-218">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="9e0fa-219">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e0fa-219">-Confirm</span></span>
<span data-ttu-id="9e0fa-220">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e0fa-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e0fa-221">-WhatIf</span></span>
<span data-ttu-id="9e0fa-222">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e0fa-223">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e0fa-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0fa-224">CommonParameters</span></span>
<span data-ttu-id="9e0fa-225">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0fa-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0fa-226">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0fa-226">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0fa-227">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e0fa-227">INPUTS</span></span>

## <span data-ttu-id="9e0fa-228">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e0fa-228">OUTPUTS</span></span>

### <span data-ttu-id="9e0fa-229">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="9e0fa-229">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="9e0fa-230">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e0fa-230">NOTES</span></span>

## <span data-ttu-id="9e0fa-231">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e0fa-231">RELATED LINKS</span></span>

[<span data-ttu-id="9e0fa-232">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9e0fa-232">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="9e0fa-233">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9e0fa-233">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="9e0fa-234">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9e0fa-234">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="9e0fa-235">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="9e0fa-235">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
