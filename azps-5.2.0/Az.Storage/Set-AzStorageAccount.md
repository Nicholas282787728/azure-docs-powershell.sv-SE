---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403336"
---
# <span data-ttu-id="18afc-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18afc-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="18afc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18afc-102">SYNOPSIS</span></span>
<span data-ttu-id="18afc-103">Ändrar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="18afc-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="18afc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18afc-104">SYNTAX</span></span>

### <span data-ttu-id="18afc-105">StorageEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="18afc-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18afc-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="18afc-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18afc-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="18afc-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18afc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18afc-108">DESCRIPTION</span></span>
<span data-ttu-id="18afc-109">Cmdleten **set-AzStorageAccount** ändrar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="18afc-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="18afc-110">Du kan använda denna cmdlet för att ändra kontotyp, uppdatera en kund domän eller ange taggar på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="18afc-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="18afc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18afc-111">EXAMPLES</span></span>

### <span data-ttu-id="18afc-112">Exempel 1: Ange lagrings konto typen</span><span class="sxs-lookup"><span data-stu-id="18afc-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="18afc-113">Det här kommandot anger lagrings konto typen till Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="18afc-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="18afc-114">Exempel 2: Ange en egen domän för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="18afc-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="18afc-115">Det här kommandot anger en egen domän för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="18afc-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="18afc-116">Exempel 3: Ange värdet för åtkomst nivå</span><span class="sxs-lookup"><span data-stu-id="18afc-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="18afc-117">Kommandot ställer in åtkomst nivå svärdet så att det blir coolt.</span><span class="sxs-lookup"><span data-stu-id="18afc-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="18afc-118">Exempel 4: Ange den anpassade domänen och Taggar</span><span class="sxs-lookup"><span data-stu-id="18afc-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="18afc-119">Kommandot anger den anpassade domänen och taggar för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="18afc-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="18afc-120">Exempel 5: Ange krypterings-käll-till-valv</span><span class="sxs-lookup"><span data-stu-id="18afc-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="18afc-121">Det här kommandot anger krypterings-käll-till-ett nytt.</span><span class="sxs-lookup"><span data-stu-id="18afc-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="18afc-122">Exempel 6: Ange krypterings-käll-Source till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="18afc-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="18afc-123">Den här kommandon har en krypterings till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="18afc-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="18afc-124">Exempel 7: ange egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="18afc-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="18afc-125">Det här kommandot anger egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="18afc-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="18afc-126">Exempel 8: hämta egenskapen NetworkRuleSet från ett lagrings konto och ange det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="18afc-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="18afc-127">Det här första kommandot får egenskapen NetworkRuleSet från ett lagrings konto och det andra kommandot ställer in det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="18afc-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="18afc-128">Exempel 9: uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot med "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="18afc-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="18afc-129">Kommandot uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot för "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="18afc-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="18afc-130">Exempel 10: uppdatera ett lagrings konto genom att aktivera autentiseringspaketet för Azure-filer.</span><span class="sxs-lookup"><span data-stu-id="18afc-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="18afc-131">Kommandot uppdaterar ett lagrings konto genom att aktivera autentiseringspaketet för Azure-filer.</span><span class="sxs-lookup"><span data-stu-id="18afc-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="18afc-132">Exempel 11: uppdatera ett lagrings konto genom att aktivera filer för Active Directory Domain service och Visa sedan inställningen för fil-ID baserat på Inställningar</span><span class="sxs-lookup"><span data-stu-id="18afc-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="18afc-133">Kommandot uppdaterar ett lagrings konto genom att aktivera Azure-filer Active Directory Domain Service-identifiering och visar sedan inställningen för fil identitets baserat autentiseringsinställningarna</span><span class="sxs-lookup"><span data-stu-id="18afc-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="18afc-134">Exempel 12: set MinimumTlsVersion and AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="18afc-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="18afc-135">Kommandot ställer in MinimumTlsVersion och AllowBlobPublicAccess och visar sedan 2-egenskaperna för kontot</span><span class="sxs-lookup"><span data-stu-id="18afc-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="18afc-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18afc-136">PARAMETERS</span></span>

### <span data-ttu-id="18afc-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="18afc-137">-AccessTier</span></span>
<span data-ttu-id="18afc-138">Anger åtkomst nivån för det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="18afc-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="18afc-139">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="18afc-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="18afc-140">Om du ändrar åtkomst nivån kan det leda till extra avgifter.</span><span class="sxs-lookup"><span data-stu-id="18afc-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="18afc-141">Mer information finns i [Azure Blob Storage: varmt och coolda lagrings nivåer](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="18afc-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="18afc-142">Om lagrings kontot har typen StorageV2 eller BlobStorage kan du ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="18afc-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="18afc-143">Om lagrings kontot har typen lagring ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="18afc-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="18afc-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="18afc-145">Anger säkerhets-ID (SID) för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="18afc-146">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="18afc-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="18afc-148">Anger domänens GUID.</span><span class="sxs-lookup"><span data-stu-id="18afc-148">Specifies the domain GUID.</span></span> <span data-ttu-id="18afc-149">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="18afc-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="18afc-151">Anger den primära domän som AD DNS-servern är auktoritär för.</span><span class="sxs-lookup"><span data-stu-id="18afc-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="18afc-152">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="18afc-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="18afc-154">Anger säkerhets-ID (SID).</span><span class="sxs-lookup"><span data-stu-id="18afc-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="18afc-155">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="18afc-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="18afc-157">Anger den Active Directory-skog som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="18afc-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="18afc-158">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="18afc-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="18afc-160">Anger NetBIOS-domännamn.</span><span class="sxs-lookup"><span data-stu-id="18afc-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="18afc-161">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="18afc-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="18afc-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="18afc-163">Tillåta eller neka offentlig åtkomst till alla blobbar eller behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="18afc-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18afc-164">-AsJob</span></span>
<span data-ttu-id="18afc-165">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18afc-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18afc-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="18afc-166">-AssignIdentity</span></span>
<span data-ttu-id="18afc-167">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="18afc-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="18afc-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="18afc-168">-CustomDomainName</span></span>
<span data-ttu-id="18afc-169">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="18afc-169">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18afc-170">-DefaultProfile</span></span>
<span data-ttu-id="18afc-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18afc-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18afc-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="18afc-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="18afc-173">Aktivera Azure-filer Active Directory Domain Service-inloggningsautentisering för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="18afc-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="18afc-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="18afc-175">Aktivera Azure-filer Active Directory Domain Service-inloggningsautentisering för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="18afc-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="18afc-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="18afc-177">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="18afc-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="18afc-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="18afc-179">Anger om lagrings kontot kan hantera stora fil resurser med mer än 5 TiB kapacitet.</span><span class="sxs-lookup"><span data-stu-id="18afc-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="18afc-180">När kontot är aktiverat kan funktionen inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="18afc-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="18afc-181">För närvarande stöds endast för LRS-och ZRS-replikeringstyp, därför är det inte möjligt att konvertera konton till geo-redundanta konton.</span><span class="sxs-lookup"><span data-stu-id="18afc-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="18afc-182">Läs mer i https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="18afc-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="18afc-183">-Force</span><span class="sxs-lookup"><span data-stu-id="18afc-183">-Force</span></span>
<span data-ttu-id="18afc-184">Gör att ändringarna skrivs till lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="18afc-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="18afc-185">-Namn</span><span class="sxs-lookup"><span data-stu-id="18afc-185">-KeyName</span></span>
<span data-ttu-id="18afc-186">Om du använder-KeyvaultEncryption för att aktivera kryptering med nyckel valv, anger du egenskapen Key Name med det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="18afc-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="18afc-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="18afc-188">Anger om Microsoft-valv ska användas för krypterings nycklar när kryptering av lagrings tjänst används.</span><span class="sxs-lookup"><span data-stu-id="18afc-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="18afc-189">Om du har angett ett namn, min version och KeyVaultUri, kommer du att få till Microsoft att ange om den här parametern är angiven.</span><span class="sxs-lookup"><span data-stu-id="18afc-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="18afc-190">-KeyVaultUri</span></span>
<span data-ttu-id="18afc-191">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key Vault.</span><span class="sxs-lookup"><span data-stu-id="18afc-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-192">-Version</span><span class="sxs-lookup"><span data-stu-id="18afc-192">-KeyVersion</span></span>
<span data-ttu-id="18afc-193">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key-versionen.</span><span class="sxs-lookup"><span data-stu-id="18afc-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="18afc-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="18afc-195">Den minsta TLS-versionen som ska tillåtas vid begäran till lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-196">-Namn</span><span class="sxs-lookup"><span data-stu-id="18afc-196">-Name</span></span>
<span data-ttu-id="18afc-197">Anger namnet på det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="18afc-197">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="18afc-198">-NetworkRuleSet</span></span>
<span data-ttu-id="18afc-199">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="18afc-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18afc-200">-ResourceGroupName</span></span>
<span data-ttu-id="18afc-201">Anger namnet på den resurs grupp där lagrings kontot ska ändras.</span><span class="sxs-lookup"><span data-stu-id="18afc-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="18afc-202">-SkuName</span></span>
<span data-ttu-id="18afc-203">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="18afc-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="18afc-204">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18afc-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18afc-205">Standard_LRS lokalt redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="18afc-206">Standard_ZRS-Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="18afc-207">Standard_GRS-Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="18afc-208">Standard_RAGRS-Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="18afc-209">Premium_LRS-Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="18afc-210">Standard_GZRS-Geo-redundant Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="18afc-211">Standard_RAGZRS-Läs åtkomst Geo-redundant Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="18afc-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="18afc-212">Du kan inte ändra Standard_ZRS och Premium_LRS typer till andra konto typer.</span><span class="sxs-lookup"><span data-stu-id="18afc-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="18afc-213">Du kan inte ändra andra konto typer till Standard_ZRS eller Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="18afc-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="18afc-214">-StorageEncryption</span></span>
<span data-ttu-id="18afc-215">Anger om kryptering av lagrings konto ska användas för att använda Microsoft-hanterade nycklar.</span><span class="sxs-lookup"><span data-stu-id="18afc-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-216">-Tagg</span><span class="sxs-lookup"><span data-stu-id="18afc-216">-Tag</span></span>
<span data-ttu-id="18afc-217">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="18afc-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="18afc-218">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="18afc-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="18afc-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="18afc-220">Uppgradera lagrings konto från lagring eller BlobStorage till StorageV2.</span><span class="sxs-lookup"><span data-stu-id="18afc-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="18afc-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="18afc-221">-UseSubDomain</span></span>
<span data-ttu-id="18afc-222">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="18afc-222">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-223">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18afc-223">-Confirm</span></span>
<span data-ttu-id="18afc-224">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18afc-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18afc-225">-WhatIf</span></span>
<span data-ttu-id="18afc-226">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18afc-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18afc-227">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18afc-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18afc-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18afc-228">CommonParameters</span></span>
<span data-ttu-id="18afc-229">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18afc-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18afc-230">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18afc-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18afc-231">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18afc-231">INPUTS</span></span>

### <span data-ttu-id="18afc-232">System. String</span><span class="sxs-lookup"><span data-stu-id="18afc-232">System.String</span></span>

### <span data-ttu-id="18afc-233">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="18afc-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18afc-234">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18afc-234">OUTPUTS</span></span>

### <span data-ttu-id="18afc-235">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18afc-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="18afc-236">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18afc-236">NOTES</span></span>

## <span data-ttu-id="18afc-237">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18afc-237">RELATED LINKS</span></span>

[<span data-ttu-id="18afc-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18afc-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="18afc-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18afc-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="18afc-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18afc-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
