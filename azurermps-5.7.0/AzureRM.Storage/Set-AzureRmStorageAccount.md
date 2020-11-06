---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575427"
---
# <span data-ttu-id="3ad3f-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ad3f-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="3ad3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ad3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad3f-103">Ändrar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ad3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ad3f-104">SYNTAX</span></span>

### <span data-ttu-id="3ad3f-105">StorageEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="3ad3f-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ad3f-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3ad3f-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ad3f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ad3f-108">Cmdleten **set-AzureRmStorageAccount** ändrar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="3ad3f-109">Du kan använda denna cmdlet för att ändra kontotyp, uppdatera en kund domän eller ange taggar på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="3ad3f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ad3f-110">EXAMPLES</span></span>

### <span data-ttu-id="3ad3f-111">Exempel 1: Ange lagrings konto typen</span><span class="sxs-lookup"><span data-stu-id="3ad3f-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="3ad3f-112">Det här kommandot anger lagrings konto typen till Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="3ad3f-113">Exempel 2: Ange en egen domän för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3ad3f-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="3ad3f-114">Det här kommandot anger en egen domän för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="3ad3f-115">Exempel 3: Aktivera kryptering för blob och fil tjänster</span><span class="sxs-lookup"><span data-stu-id="3ad3f-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="3ad3f-116">Det här kommandot aktiverar Storage Service-kryptering för blob och fil för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="3ad3f-117">Exempel 4: ange åtkomst nivå svärdet</span><span class="sxs-lookup"><span data-stu-id="3ad3f-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="3ad3f-118">Kommandot ställer in åtkomst nivå svärdet så att det blir coolt.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="3ad3f-119">Exempel 4: Ange den anpassade domänen och Taggar</span><span class="sxs-lookup"><span data-stu-id="3ad3f-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="3ad3f-120">Kommandot ställer in åtkomst nivå svärdet så att det blir coolt.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="3ad3f-121">Exempel 5: Aktivera kryptering för BLOB-tjänster med ett valv</span><span class="sxs-lookup"><span data-stu-id="3ad3f-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="3ad3f-122">Det här kommandot aktiverar kryptering av lagrings tjänst för BLOB med ett nytt aktiverat.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="3ad3f-123">Exempel 6: inaktivera kryptering på fil tjänster med att en webb adress är inställd på "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="3ad3f-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="3ad3f-124">Det här kommandot inaktiverar kryptering för fil tjänster med att en källkod är inställd på "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="3ad3f-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="3ad3f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ad3f-125">PARAMETERS</span></span>

### <span data-ttu-id="3ad3f-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="3ad3f-126">-AccessTier</span></span>
<span data-ttu-id="3ad3f-127">Anger åtkomst nivån för det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="3ad3f-128">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="3ad3f-129">Om du ändrar åtkomst nivån kan det leda till extra avgifter.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="3ad3f-130">Mer information finns i Azure Blob Storage: varmt och coolda lagrings nivåer https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="3ad3f-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="3ad3f-131">Om typen av lagrings konto är lagring ska du inte ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3ad3f-132">-AssignIdentity</span></span>
<span data-ttu-id="3ad3f-133">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3ad3f-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3ad3f-134">-CustomDomainName</span></span>
<span data-ttu-id="3ad3f-135">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="3ad3f-136">-DisableEncryptionService</span></span>
<span data-ttu-id="3ad3f-137">Anger om den här cmdleten inaktiverar kryptering av lagrings tjänst i lagrings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="3ad3f-138">Stöd för Azure-blob och Azure File Services.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="3ad3f-139">-EnableEncryptionService</span></span>
<span data-ttu-id="3ad3f-140">Anger om denna cmdlet aktiverar Storage Service-kryptering för lagrings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="3ad3f-141">Stöd för Azure-blob och Azure File Services.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="3ad3f-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="3ad3f-143">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-144">-Force</span><span class="sxs-lookup"><span data-stu-id="3ad3f-144">-Force</span></span>
<span data-ttu-id="3ad3f-145">Om du ändrar åtkomst nivån kan det leda till extra avgifter.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="3ad3f-146">Mer information finns i Azure Blob Storage: varmt och coolda lagrings nivåer https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="3ad3f-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="3ad3f-147">Om typen av lagrings konto är lagring ska du inte ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="3ad3f-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3ad3f-148">-InformationAction</span></span>
<span data-ttu-id="3ad3f-149">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ad3f-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3ad3f-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ad3f-151">Vidare</span><span class="sxs-lookup"><span data-stu-id="3ad3f-151">Continue</span></span>
- <span data-ttu-id="3ad3f-152">Över</span><span class="sxs-lookup"><span data-stu-id="3ad3f-152">Ignore</span></span>
- <span data-ttu-id="3ad3f-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="3ad3f-153">Inquire</span></span>
- <span data-ttu-id="3ad3f-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3ad3f-154">SilentlyContinue</span></span>
- <span data-ttu-id="3ad3f-155">Stanna</span><span class="sxs-lookup"><span data-stu-id="3ad3f-155">Stop</span></span>
- <span data-ttu-id="3ad3f-156">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3ad3f-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3ad3f-157">-InformationVariable</span></span>
<span data-ttu-id="3ad3f-158">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ad3f-159">-KeyName</span></span>
<span data-ttu-id="3ad3f-160">Krypterings namn för Storage Account Encryption-valv</span><span class="sxs-lookup"><span data-stu-id="3ad3f-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3ad3f-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="3ad3f-162">Om du vill ange Storage Account Encryption-källkod till Microsoft.-valv eller inte.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span>
<span data-ttu-id="3ad3f-163">Om du anger namn, värde versions-och KeyvaultUri för lagrings konto till Microsoft. radiovalv väder den här parametern har ställts in.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3ad3f-164">-KeyVaultUri</span></span>
<span data-ttu-id="3ad3f-165">KeyVaultUri för Storage Account Encryption-valv</span><span class="sxs-lookup"><span data-stu-id="3ad3f-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-166">-Version</span><span class="sxs-lookup"><span data-stu-id="3ad3f-166">-KeyVersion</span></span>
<span data-ttu-id="3ad3f-167">Krypterings knapp version för Storage Account Encryption</span><span class="sxs-lookup"><span data-stu-id="3ad3f-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-168">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ad3f-168">-Name</span></span>
<span data-ttu-id="3ad3f-169">Anger namnet på det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-169">Specifies the name of the Storage account to Modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad3f-170">-ResourceGroupName</span></span>
<span data-ttu-id="3ad3f-171">Anger namnet på den resurs grupp där lagrings kontot ska ändras.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-171">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="3ad3f-172">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3ad3f-172">-SkuName</span></span>
<span data-ttu-id="3ad3f-173">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-173">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="3ad3f-174">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3ad3f-174">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ad3f-175">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-175">Standard_LRS.</span></span>
<span data-ttu-id="3ad3f-176">Lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-176">Locally-redundant storage.</span></span>
- <span data-ttu-id="3ad3f-177">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-177">Standard_ZRS.</span></span>
<span data-ttu-id="3ad3f-178">Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-178">Zone-redundant storage.</span></span>
- <span data-ttu-id="3ad3f-179">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-179">Standard_GRS.</span></span>
<span data-ttu-id="3ad3f-180">Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-180">Geo-redundant storage.</span></span>
- <span data-ttu-id="3ad3f-181">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-181">Standard_RAGRS.</span></span>
<span data-ttu-id="3ad3f-182">Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-182">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="3ad3f-183">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-183">Premium_LRS.</span></span>
<span data-ttu-id="3ad3f-184">Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-184">Premium locally-redundant storage.</span></span>

<span data-ttu-id="3ad3f-185">Du kan inte ändra Standard_ZRS och Premium_LRS typer till andra konto typer.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-185">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="3ad3f-186">Du kan inte ändra andra konto typer till Standard_ZRS eller Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-186">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-187">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3ad3f-187">-StorageEncryption</span></span>
<span data-ttu-id="3ad3f-188">Om du vill ange Storage Account Encryption-källkod till Microsoft. Storage eller inte.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-188">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-189">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3ad3f-189">-Tag</span></span>
<span data-ttu-id="3ad3f-190">Om du anger ett värde för BlobStorage för parametern *sort* i New-AzureRmStorageAccount cmdlet måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3ad3f-190">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="3ad3f-191">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="3ad3f-191">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="3ad3f-192">-UseSubDomain</span></span>
<span data-ttu-id="3ad3f-193">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ad3f-194">-Confirm</span></span>
<span data-ttu-id="3ad3f-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad3f-196">-WhatIf</span></span>
<span data-ttu-id="3ad3f-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad3f-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad3f-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad3f-199">CommonParameters</span></span>
<span data-ttu-id="3ad3f-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad3f-201">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad3f-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad3f-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ad3f-202">INPUTS</span></span>

### <span data-ttu-id="3ad3f-203">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ad3f-203">None</span></span>
<span data-ttu-id="3ad3f-204">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3ad3f-204">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ad3f-205">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ad3f-205">OUTPUTS</span></span>

## <span data-ttu-id="3ad3f-206">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ad3f-206">NOTES</span></span>

## <span data-ttu-id="3ad3f-207">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ad3f-207">RELATED LINKS</span></span>

[<span data-ttu-id="3ad3f-208">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ad3f-208">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="3ad3f-209">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ad3f-209">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="3ad3f-210">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ad3f-210">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
