---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: c182ee26f66cf20ab50bd778e398061ff39c60c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578727"
---
# <span data-ttu-id="5d039-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d039-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="5d039-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d039-102">SYNOPSIS</span></span>
<span data-ttu-id="5d039-103">Ändrar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5d039-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d039-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d039-104">SYNTAX</span></span>

### <span data-ttu-id="5d039-105">StorageEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="5d039-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d039-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="5d039-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d039-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d039-107">DESCRIPTION</span></span>
<span data-ttu-id="5d039-108">Cmdleten **set-AzureRmStorageAccount** ändrar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="5d039-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="5d039-109">Du kan använda denna cmdlet för att ändra kontotyp, uppdatera en kund domän eller ange taggar på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5d039-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="5d039-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d039-110">EXAMPLES</span></span>

### <span data-ttu-id="5d039-111">Exempel 1: Ange lagrings konto typen</span><span class="sxs-lookup"><span data-stu-id="5d039-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="5d039-112">Det här kommandot anger lagrings konto typen till Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="5d039-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="5d039-113">Exempel 2: Ange en egen domän för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5d039-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="5d039-114">Det här kommandot anger en egen domän för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5d039-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="5d039-115">Exempel 3: Ange värdet för åtkomst nivå</span><span class="sxs-lookup"><span data-stu-id="5d039-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="5d039-116">Kommandot ställer in åtkomst nivå svärdet så att det blir coolt.</span><span class="sxs-lookup"><span data-stu-id="5d039-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="5d039-117">Exempel 4: Ange den anpassade domänen och Taggar</span><span class="sxs-lookup"><span data-stu-id="5d039-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="5d039-118">Kommandot anger den anpassade domänen och taggar för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5d039-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="5d039-119">Exempel 5: Ange krypterings-käll-till-valv</span><span class="sxs-lookup"><span data-stu-id="5d039-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="5d039-120">Det här kommandot anger krypterings-käll-till-ett nytt.</span><span class="sxs-lookup"><span data-stu-id="5d039-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="5d039-121">Exempel 6: Ange krypterings-käll-Source till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="5d039-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="5d039-122">Den här kommandon har en krypterings till "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="5d039-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="5d039-123">Exempel 7: ange egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="5d039-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="5d039-124">Det här kommandot anger egenskapen NetworkRuleSet för ett lagrings konto med JSON</span><span class="sxs-lookup"><span data-stu-id="5d039-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="5d039-125">Exempel 8: hämta egenskapen NetworkRuleSet från ett lagrings konto och ange det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5d039-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="5d039-126">Det här första kommandot får egenskapen NetworkRuleSet från ett lagrings konto och det andra kommandot ställer in det till ett annat lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5d039-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="5d039-127">Exempel 9: uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot med "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="5d039-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="5d039-128">Kommandot uppgradera ett lagrings konto med typen "lagring" eller "BlobStorage" till lagrings kontot för "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="5d039-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="5d039-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d039-129">PARAMETERS</span></span>

### <span data-ttu-id="5d039-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="5d039-130">-AccessTier</span></span>
<span data-ttu-id="5d039-131">Anger åtkomst nivån för det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5d039-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="5d039-132">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="5d039-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="5d039-133">Om du ändrar åtkomst nivån kan det leda till extra avgifter.</span><span class="sxs-lookup"><span data-stu-id="5d039-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="5d039-134">Mer information finns i [Azure Blob Storage: varmt och coolda lagrings nivåer](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="5d039-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="5d039-135">Om lagrings kontot har typen StorageV2 eller BlobStorage kan du ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="5d039-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="5d039-136">Om lagrings kontot har typen lagring ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="5d039-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="5d039-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d039-137">-AsJob</span></span>
<span data-ttu-id="5d039-138">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5d039-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d039-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5d039-139">-AssignIdentity</span></span>
<span data-ttu-id="5d039-140">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="5d039-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="5d039-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="5d039-141">-CustomDomainName</span></span>
<span data-ttu-id="5d039-142">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="5d039-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="5d039-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d039-143">-DefaultProfile</span></span>
<span data-ttu-id="5d039-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d039-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d039-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="5d039-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="5d039-146">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="5d039-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d039-147">-Force</span><span class="sxs-lookup"><span data-stu-id="5d039-147">-Force</span></span>
<span data-ttu-id="5d039-148">Gör att ändringarna skrivs till lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5d039-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="5d039-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d039-149">-KeyName</span></span>
<span data-ttu-id="5d039-150">Om du använder-KeyvaultEncryption för att aktivera kryptering med nyckel valv, anger du egenskapen Key Name med det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="5d039-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="5d039-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="5d039-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="5d039-152">Anger om Microsoft-valv ska användas för krypterings nycklar när kryptering av lagrings tjänst används.</span><span class="sxs-lookup"><span data-stu-id="5d039-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="5d039-153">Om du har angett ett namn, min version och KeyVaultUri, kommer du att få till Microsoft att ange om den här parametern är angiven.</span><span class="sxs-lookup"><span data-stu-id="5d039-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="5d039-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="5d039-154">-KeyVaultUri</span></span>
<span data-ttu-id="5d039-155">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5d039-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="5d039-156">-Version</span><span class="sxs-lookup"><span data-stu-id="5d039-156">-KeyVersion</span></span>
<span data-ttu-id="5d039-157">När du använder Key valv Encryption genom att ange parametern-KeyvaultEncryption kan du använda det här alternativet för att ange URI till Key-versionen.</span><span class="sxs-lookup"><span data-stu-id="5d039-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="5d039-158">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d039-158">-Name</span></span>
<span data-ttu-id="5d039-159">Anger namnet på det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="5d039-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="5d039-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d039-160">-NetworkRuleSet</span></span>
<span data-ttu-id="5d039-161">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="5d039-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="5d039-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d039-162">-ResourceGroupName</span></span>
<span data-ttu-id="5d039-163">Anger namnet på den resurs grupp där lagrings kontot ska ändras.</span><span class="sxs-lookup"><span data-stu-id="5d039-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="5d039-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5d039-164">-SkuName</span></span>
<span data-ttu-id="5d039-165">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="5d039-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="5d039-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5d039-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d039-167">Standard_LRS lokalt redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="5d039-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="5d039-168">Standard_ZRS-Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="5d039-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="5d039-169">Standard_GRS-Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="5d039-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="5d039-170">Standard_RAGRS-Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="5d039-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="5d039-171">Premium_LRS-Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="5d039-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="5d039-172">Du kan inte ändra Standard_ZRS och Premium_LRS typer till andra konto typer.</span><span class="sxs-lookup"><span data-stu-id="5d039-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="5d039-173">Du kan inte ändra andra konto typer till Standard_ZRS eller Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="5d039-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="5d039-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="5d039-174">-StorageEncryption</span></span>
<span data-ttu-id="5d039-175">Anger om kryptering av lagrings konto ska användas för att använda Microsoft-hanterade nycklar.</span><span class="sxs-lookup"><span data-stu-id="5d039-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="5d039-176">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5d039-176">-Tag</span></span>
<span data-ttu-id="5d039-177">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="5d039-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="5d039-178">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="5d039-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5d039-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="5d039-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="5d039-180">Uppgradera lagrings konto från lagring eller BlobStorage till StorageV2.</span><span class="sxs-lookup"><span data-stu-id="5d039-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="5d039-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="5d039-181">-UseSubDomain</span></span>
<span data-ttu-id="5d039-182">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="5d039-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="5d039-183">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d039-183">-Confirm</span></span>
<span data-ttu-id="5d039-184">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d039-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d039-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d039-185">-WhatIf</span></span>
<span data-ttu-id="5d039-186">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d039-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d039-187">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d039-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d039-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d039-188">CommonParameters</span></span>
<span data-ttu-id="5d039-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d039-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d039-190">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d039-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d039-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d039-191">INPUTS</span></span>

### <span data-ttu-id="5d039-192">System. String</span><span class="sxs-lookup"><span data-stu-id="5d039-192">System.String</span></span>

### <span data-ttu-id="5d039-193">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5d039-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5d039-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d039-194">System.Boolean</span></span>

## <span data-ttu-id="5d039-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d039-195">OUTPUTS</span></span>

### <span data-ttu-id="5d039-196">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d039-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5d039-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d039-197">NOTES</span></span>

## <span data-ttu-id="5d039-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d039-198">RELATED LINKS</span></span>

[<span data-ttu-id="5d039-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d039-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="5d039-200">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d039-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="5d039-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d039-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)