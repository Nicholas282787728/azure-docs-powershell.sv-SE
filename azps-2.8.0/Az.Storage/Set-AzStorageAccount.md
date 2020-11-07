---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 69c71cd0401b8509943ef7e5ad7316db99f03670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921020"
---
# <span data-ttu-id="b3b95-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3b95-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="b3b95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3b95-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b95-103">Ändrar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b3b95-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="b3b95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3b95-104">SYNTAX</span></span>

### <span data-ttu-id="b3b95-105">StorageEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="b3b95-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b95-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="b3b95-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b95-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3b95-107">DESCRIPTION</span></span>
<span data-ttu-id="b3b95-108">Cmdleten **set-AzStorageAccount** ändrar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="b3b95-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="b3b95-109">Du kan använda denna cmdlet för att ändra kontotyp, uppdatera en kund domän eller ange taggar på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b3b95-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="b3b95-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3b95-110">EXAMPLES</span></span>

### <span data-ttu-id="b3b95-111">Exempel 1: Ange lagrings konto typen</span><span class="sxs-lookup"><span data-stu-id="b3b95-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="b3b95-112">Det här kommandot anger lagrings konto typen till Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="b3b95-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="b3b95-113">Exempel 2: Ange en egen domän för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b3b95-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="b3b95-114">Det här kommandot anger en egen domän för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b3b95-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="b3b95-115">Exempel 3: Ange värdet för åtkomst nivå</span><span class="sxs-lookup"><span data-stu-id="b3b95-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="b3b95-116">Kommandot ställer in åtkomst nivå svärdet så att det blir coolt.</span><span class="sxs-lookup"><span data-stu-id="b3b95-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="b3b95-117">Exempel 4: Ange den anpassade domänen och Taggar</span><span class="sxs-lookup"><span data-stu-id="b3b95-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="b3b95-118">Kommandot anger den anpassade domänen och taggar för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b3b95-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="b3b95-119">Exempel 5: Ange krypterings-käll-till-valv</span><span class="sxs-lookup"><span data-stu-id="b3b95-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="b3b95-120">Det här kommandot anger krypterings-käll-till-ett nytt.</span><span class="sxs-lookup"><span data-stu-id="b3b95-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="b3b95-121">Exempel 6: Ange krypterings-käll-Source till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="b3b95-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="b3b95-122">Den här kommandon har en krypterings till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="b3b95-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="b3b95-123">Exempel 7: ange egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="b3b95-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="b3b95-124">Det här kommandot anger egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="b3b95-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="b3b95-125">Exempel 8: hämta egenskapen NetworkRuleSet från ett lagrings konto och ange det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b3b95-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="b3b95-126">Det här första kommandot får egenskapen NetworkRuleSet från ett lagrings konto och det andra kommandot ställer in det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b3b95-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="b3b95-127">Exempel 9: uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot med "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="b3b95-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="b3b95-128">Kommandot uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot för "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="b3b95-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="b3b95-129">Exempel 10: uppdatera ett lagrings konto genom att aktivera autentiseringspaketet för Azure-filer.</span><span class="sxs-lookup"><span data-stu-id="b3b95-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="b3b95-130">Kommandot uppdaterar ett lagrings konto genom att aktivera autentiseringspaketet för Azure-filer.</span><span class="sxs-lookup"><span data-stu-id="b3b95-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="b3b95-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3b95-131">PARAMETERS</span></span>

### <span data-ttu-id="b3b95-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="b3b95-132">-AccessTier</span></span>
<span data-ttu-id="b3b95-133">Anger åtkomst nivån för det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b3b95-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="b3b95-134">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="b3b95-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="b3b95-135">Om du ändrar åtkomst nivån kan det leda till extra avgifter.</span><span class="sxs-lookup"><span data-stu-id="b3b95-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="b3b95-136">Mer information finns i [Azure Blob Storage: varmt och coolda lagrings nivåer](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="b3b95-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="b3b95-137">Om lagrings kontot har typen StorageV2 eller BlobStorage kan du ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="b3b95-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="b3b95-138">Om lagrings kontot har typen lagring ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="b3b95-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="b3b95-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3b95-139">-AsJob</span></span>
<span data-ttu-id="b3b95-140">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b3b95-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3b95-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b3b95-141">-AssignIdentity</span></span>
<span data-ttu-id="b3b95-142">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="b3b95-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b3b95-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b3b95-143">-CustomDomainName</span></span>
<span data-ttu-id="b3b95-144">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="b3b95-144">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="b3b95-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b95-145">-DefaultProfile</span></span>
<span data-ttu-id="b3b95-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b95-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b95-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="b3b95-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="b3b95-148">Aktivera Azure-filer för Azure Active Directory Domain Service för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b3b95-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="b3b95-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="b3b95-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="b3b95-150">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="b3b95-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="b3b95-151">-Force</span><span class="sxs-lookup"><span data-stu-id="b3b95-151">-Force</span></span>
<span data-ttu-id="b3b95-152">Gör att ändringarna skrivs till lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b3b95-152">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="b3b95-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3b95-153">-KeyName</span></span>
<span data-ttu-id="b3b95-154">Om du använder-KeyvaultEncryption för att aktivera kryptering med nyckel valv, anger du egenskapen Key Name med det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="b3b95-154">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="b3b95-155">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="b3b95-155">-KeyvaultEncryption</span></span>
<span data-ttu-id="b3b95-156">Anger om Microsoft-valv ska användas för krypterings nycklar när kryptering av lagrings tjänst används.</span><span class="sxs-lookup"><span data-stu-id="b3b95-156">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="b3b95-157">Om du har angett ett namn, min version och KeyVaultUri, kommer du att få till Microsoft att ange om den här parametern är angiven.</span><span class="sxs-lookup"><span data-stu-id="b3b95-157">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="b3b95-158">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="b3b95-158">-KeyVaultUri</span></span>
<span data-ttu-id="b3b95-159">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b3b95-159">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="b3b95-160">-Version</span><span class="sxs-lookup"><span data-stu-id="b3b95-160">-KeyVersion</span></span>
<span data-ttu-id="b3b95-161">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key-versionen.</span><span class="sxs-lookup"><span data-stu-id="b3b95-161">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="b3b95-162">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3b95-162">-Name</span></span>
<span data-ttu-id="b3b95-163">Anger namnet på det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="b3b95-163">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="b3b95-164">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3b95-164">-NetworkRuleSet</span></span>
<span data-ttu-id="b3b95-165">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="b3b95-165">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="b3b95-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b95-166">-ResourceGroupName</span></span>
<span data-ttu-id="b3b95-167">Anger namnet på den resurs grupp där lagrings kontot ska ändras.</span><span class="sxs-lookup"><span data-stu-id="b3b95-167">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="b3b95-168">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b3b95-168">-SkuName</span></span>
<span data-ttu-id="b3b95-169">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="b3b95-169">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="b3b95-170">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b3b95-170">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3b95-171">Standard_LRS lokalt redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="b3b95-171">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="b3b95-172">Standard_ZRS-Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="b3b95-172">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="b3b95-173">Standard_GRS-Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="b3b95-173">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="b3b95-174">Standard_RAGRS-Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="b3b95-174">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="b3b95-175">Premium_LRS-Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="b3b95-175">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="b3b95-176">Du kan inte ändra Standard_ZRS och Premium_LRS typer till andra konto typer.</span><span class="sxs-lookup"><span data-stu-id="b3b95-176">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="b3b95-177">Du kan inte ändra andra konto typer till Standard_ZRS eller Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="b3b95-177">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b95-178">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="b3b95-178">-StorageEncryption</span></span>
<span data-ttu-id="b3b95-179">Anger om kryptering av lagrings konto ska användas för att använda Microsoft-hanterade nycklar.</span><span class="sxs-lookup"><span data-stu-id="b3b95-179">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="b3b95-180">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b3b95-180">-Tag</span></span>
<span data-ttu-id="b3b95-181">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="b3b95-181">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="b3b95-182">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b3b95-182">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b3b95-183">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="b3b95-183">-UpgradeToStorageV2</span></span>
<span data-ttu-id="b3b95-184">Uppgradera lagrings konto från lagring eller BlobStorage till StorageV2.</span><span class="sxs-lookup"><span data-stu-id="b3b95-184">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="b3b95-185">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="b3b95-185">-UseSubDomain</span></span>
<span data-ttu-id="b3b95-186">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="b3b95-186">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="b3b95-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3b95-187">-Confirm</span></span>
<span data-ttu-id="b3b95-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3b95-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b95-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b95-189">-WhatIf</span></span>
<span data-ttu-id="b3b95-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3b95-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b95-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3b95-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b95-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b95-192">CommonParameters</span></span>
<span data-ttu-id="b3b95-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b95-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b95-194">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b95-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b95-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3b95-195">INPUTS</span></span>

### <span data-ttu-id="b3b95-196">System. String</span><span class="sxs-lookup"><span data-stu-id="b3b95-196">System.String</span></span>

### <span data-ttu-id="b3b95-197">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b3b95-197">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3b95-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3b95-198">OUTPUTS</span></span>

### <span data-ttu-id="b3b95-199">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3b95-199">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b3b95-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3b95-200">NOTES</span></span>

## <span data-ttu-id="b3b95-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3b95-201">RELATED LINKS</span></span>

[<span data-ttu-id="b3b95-202">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3b95-202">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="b3b95-203">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3b95-203">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="b3b95-204">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3b95-204">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
