---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261532"
---
# <span data-ttu-id="f9493-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9493-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="f9493-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9493-102">SYNOPSIS</span></span>
<span data-ttu-id="f9493-103">Skapar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f9493-103">Creates a Storage account.</span></span>

## <span data-ttu-id="f9493-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9493-104">SYNTAX</span></span>

### <span data-ttu-id="f9493-105">AzureActiveDirectoryDomainServicesForFile (standard)</span><span class="sxs-lookup"><span data-stu-id="f9493-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9493-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="f9493-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9493-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9493-107">DESCRIPTION</span></span>
<span data-ttu-id="f9493-108">Cmdleten **New-AzStorageAccount** skapar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="f9493-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="f9493-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9493-109">EXAMPLES</span></span>

### <span data-ttu-id="f9493-110">Exempel 1: skapa ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="f9493-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="f9493-111">Det här kommandot skapar ett lagrings konto för resurs grupps namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f9493-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="f9493-112">Exempel 2: skapa ett Blob Storage-konto med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="f9493-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="f9493-113">Det här kommandot skapar ett BLOB-lagringssystem med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="f9493-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="f9493-114">Exempel 3: skapa ett lagrings konto med Natura StorageV2 och generera och tilldela en identitet för Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="f9493-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="f9493-115">Det här kommandot skapar ett lagrings konto med typen StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f9493-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="f9493-116">Den skapar också och tilldelar en identitet som kan användas för att hantera konto nycklar via Azure-nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="f9493-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="f9493-117">Exempel 4: skapa ett lagrings konto med NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="f9493-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="f9493-118">Det här kommandot skapar ett lagrings konto med egenskapen NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="f9493-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="f9493-119">Exempel 5: skapa ett lagrings konto med hierarkiskt namn område aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f9493-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="f9493-120">Det här kommandot skapar ett lagrings konto med hierarkiskt namn område aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f9493-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="f9493-121">Exempel 6: skapa ett lagrings konto med Azure-filer AAD DS-identifiering och aktivera stor fil delning.</span><span class="sxs-lookup"><span data-stu-id="f9493-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="f9493-122">Det här kommandot skapar ett lagrings konto med Azure-filer AAD DS-autentiseringsprocessen och aktiverar stor fil delning.</span><span class="sxs-lookup"><span data-stu-id="f9493-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="f9493-123">Exempel 7: skapa ett lagrings konto med aktivera filer för Active Directory Domain Service.</span><span class="sxs-lookup"><span data-stu-id="f9493-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="f9493-124">Det här kommandot skapar ett lagrings konto withenable filer Active Directory Domain Service.</span><span class="sxs-lookup"><span data-stu-id="f9493-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="f9493-125">Exempel 8: skapa ett lagrings konto med en kö-och tabell tjänst Använd krypterings nycklar med konto omfång och kräver infrastruktur kryptering.</span><span class="sxs-lookup"><span data-stu-id="f9493-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="f9493-126">Det här kommandot skapar ett lagrings konto med en kö-och tabell tjänst som använder kontots krypterings nyckel och kräver infrastruktur kryptering, så att kön och tabellen använder samma krypterings nyckel med blobben och fil tjänsten och tjänsten tillämpar ett sekundärt krypterings skikt med plattforms hanterade nycklar för data på rest.</span><span class="sxs-lookup"><span data-stu-id="f9493-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="f9493-127">Hämta sedan egenskaperna för lagrings kontot och Visa krypterings typen för kö-och tabell tjänsten och RequireInfrastructureEncryption värde.</span><span class="sxs-lookup"><span data-stu-id="f9493-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="f9493-128">Exempel 9: skapa konto MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="f9493-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="f9493-129">Kommandot skapar konto med MinimumTlsVersion och AllowBlobPublicAccess och visar sedan 2-egenskaperna för det skapade kontot</span><span class="sxs-lookup"><span data-stu-id="f9493-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="f9493-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9493-130">PARAMETERS</span></span>

### <span data-ttu-id="f9493-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="f9493-131">-AccessTier</span></span>
<span data-ttu-id="f9493-132">Anger åtkomst nivån för det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9493-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="f9493-133">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="f9493-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="f9493-134">Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="f9493-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="f9493-135">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="f9493-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="f9493-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="f9493-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="f9493-137">Anger säkerhets-ID (SID) för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="f9493-138">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="f9493-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="f9493-140">Anger domänens GUID.</span><span class="sxs-lookup"><span data-stu-id="f9493-140">Specifies the domain GUID.</span></span> <span data-ttu-id="f9493-141">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="f9493-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="f9493-143">Anger den primära domän som AD DNS-servern är auktoritär för.</span><span class="sxs-lookup"><span data-stu-id="f9493-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="f9493-144">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="f9493-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="f9493-146">Anger säkerhets-ID (SID).</span><span class="sxs-lookup"><span data-stu-id="f9493-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="f9493-147">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="f9493-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="f9493-149">Anger den Active Directory-skog som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="f9493-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="f9493-150">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="f9493-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="f9493-152">Anger NetBIOS-domännamn.</span><span class="sxs-lookup"><span data-stu-id="f9493-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="f9493-153">Den här parametern måste anges när-EnableActiveDirectoryDomainServicesForFile är inställt på True.</span><span class="sxs-lookup"><span data-stu-id="f9493-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="f9493-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="f9493-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="f9493-155">Tillåt offentlig åtkomst till alla blobbar eller behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="f9493-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="f9493-156">Standard tolkningen är sant för den här egenskapen.</span><span class="sxs-lookup"><span data-stu-id="f9493-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="f9493-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9493-157">-AsJob</span></span>
<span data-ttu-id="f9493-158">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f9493-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9493-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f9493-159">-AssignIdentity</span></span>
<span data-ttu-id="f9493-160">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="f9493-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f9493-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f9493-161">-CustomDomainName</span></span>
<span data-ttu-id="f9493-162">Anger namnet på lagrings kontots anpassade domän.</span><span class="sxs-lookup"><span data-stu-id="f9493-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="f9493-163">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="f9493-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9493-164">-DefaultProfile</span></span>
<span data-ttu-id="f9493-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9493-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9493-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="f9493-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="f9493-167">Aktivera Azure-filer Active Directory Domain Service-inloggningsautentisering för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="f9493-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="f9493-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="f9493-169">Aktivera Azure-filer för Azure Active Directory Domain Service för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="f9493-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="f9493-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="f9493-171">Anger om lagrings kontot aktiverar ett hierarkiskt namn område.</span><span class="sxs-lookup"><span data-stu-id="f9493-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="f9493-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="f9493-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="f9493-173">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="f9493-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="f9493-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="f9493-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="f9493-175">Anger om lagrings kontot kan hantera stora fil resurser med mer än 5 TiB kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f9493-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="f9493-176">När kontot är aktiverat kan funktionen inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="f9493-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="f9493-177">För närvarande stöds endast för LRS-och ZRS-replikeringstyp, därför är det inte möjligt att konvertera konton till geo-redundanta konton.</span><span class="sxs-lookup"><span data-stu-id="f9493-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="f9493-178">Läs mer i https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="f9493-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="f9493-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="f9493-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="f9493-180">Ange krypterings typen för kön.</span><span class="sxs-lookup"><span data-stu-id="f9493-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="f9493-181">Standardvärdet är service.</span><span class="sxs-lookup"><span data-stu-id="f9493-181">The default value is Service.</span></span>
<span data-ttu-id="f9493-182">-Konto: kön krypteras med krypterings nycklar med konto omfattning.</span><span class="sxs-lookup"><span data-stu-id="f9493-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="f9493-183">-Service: kö kommer alltid att vara krypterad med Service-Managed nycklar.</span><span class="sxs-lookup"><span data-stu-id="f9493-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="f9493-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="f9493-185">Ange krypterings typ för tabellen.</span><span class="sxs-lookup"><span data-stu-id="f9493-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="f9493-186">Standardvärdet är service.</span><span class="sxs-lookup"><span data-stu-id="f9493-186">The default value is Service.</span></span>
- <span data-ttu-id="f9493-187">Konto: tabellen krypteras med krypterings nycklar med konto – begränsad.</span><span class="sxs-lookup"><span data-stu-id="f9493-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="f9493-188">Tjänst: tabellen kommer alltid att vara krypterad med Service-Managed nycklar.</span><span class="sxs-lookup"><span data-stu-id="f9493-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-189">-Sort</span><span class="sxs-lookup"><span data-stu-id="f9493-189">-Kind</span></span>
<span data-ttu-id="f9493-190">Anger den typ av lagrings konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="f9493-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="f9493-191">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f9493-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9493-192">Lagringsrelaterade.</span><span class="sxs-lookup"><span data-stu-id="f9493-192">Storage.</span></span> <span data-ttu-id="f9493-193">Allmänt syfte lagrings konto som stöder lagring av blobbar, tabeller, köer, filer och diskar.</span><span class="sxs-lookup"><span data-stu-id="f9493-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="f9493-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f9493-194">StorageV2.</span></span> <span data-ttu-id="f9493-195">Allmänt syfte version 2 (GPv2) lagrings konto som har stöd för blobbar, tabeller, köer, filer och diskar med avancerade funktioner som data lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="f9493-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="f9493-196">BlobStorage.</span></span> <span data-ttu-id="f9493-197">Blob Storage-konto som endast stöder lagring av BLOB.</span><span class="sxs-lookup"><span data-stu-id="f9493-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="f9493-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="f9493-198">BlockBlobStorage.</span></span> <span data-ttu-id="f9493-199">Spärra Blob Storage-konto som endast stöder lagring av Block-Blob.</span><span class="sxs-lookup"><span data-stu-id="f9493-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="f9493-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="f9493-200">FileStorage.</span></span> <span data-ttu-id="f9493-201">Fil lagrings konto som endast stöder lagring av filer.</span><span class="sxs-lookup"><span data-stu-id="f9493-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="f9493-202">Standardvärdet är StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f9493-202">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-203">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9493-203">-Location</span></span>
<span data-ttu-id="f9493-204">Anger platsen för det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f9493-204">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f9493-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="f9493-206">Den minsta TLS-versionen som ska tillåtas vid begäran till lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="f9493-207">Standard tolkningen är TLS 1,0 för den här egenskapen.</span><span class="sxs-lookup"><span data-stu-id="f9493-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="f9493-208">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9493-208">-Name</span></span>
<span data-ttu-id="f9493-209">Anger namnet på det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f9493-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="f9493-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9493-210">-NetworkRuleSet</span></span>
<span data-ttu-id="f9493-211">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="f9493-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="f9493-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="f9493-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="f9493-213">Tjänsten tillämpar ett sekundärt krypterings lager med plattforms hanterade nycklar för data på rest.</span><span class="sxs-lookup"><span data-stu-id="f9493-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="f9493-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9493-214">-ResourceGroupName</span></span>
<span data-ttu-id="f9493-215">Anger namnet på den resurs grupp där lagrings kontot ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f9493-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="f9493-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f9493-216">-SkuName</span></span>
<span data-ttu-id="f9493-217">Anger SKU-namnet på det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9493-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="f9493-218">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f9493-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9493-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-219">Standard_LRS.</span></span> <span data-ttu-id="f9493-220">Lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="f9493-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-221">Standard_ZRS.</span></span> <span data-ttu-id="f9493-222">Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="f9493-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-223">Standard_GRS.</span></span> <span data-ttu-id="f9493-224">Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="f9493-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-225">Standard_RAGRS.</span></span> <span data-ttu-id="f9493-226">Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="f9493-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-227">Premium_LRS.</span></span> <span data-ttu-id="f9493-228">Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="f9493-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="f9493-229">Premium_ZRS.</span></span> <span data-ttu-id="f9493-230">Premium Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="f9493-231">Standard_GZRS-Geo-redundant Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="f9493-232">Standard_RAGZRS-Läs åtkomst Geo-redundant Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="f9493-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9493-233">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f9493-233">-Tag</span></span>
<span data-ttu-id="f9493-234">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="f9493-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f9493-235">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f9493-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f9493-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="f9493-236">-UseSubDomain</span></span>
<span data-ttu-id="f9493-237">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="f9493-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="f9493-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9493-238">CommonParameters</span></span>
<span data-ttu-id="f9493-239">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9493-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9493-240">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9493-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9493-241">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9493-241">INPUTS</span></span>

### <span data-ttu-id="f9493-242">System. String</span><span class="sxs-lookup"><span data-stu-id="f9493-242">System.String</span></span>

## <span data-ttu-id="f9493-243">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9493-243">OUTPUTS</span></span>

### <span data-ttu-id="f9493-244">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9493-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f9493-245">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9493-245">NOTES</span></span>

## <span data-ttu-id="f9493-246">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9493-246">RELATED LINKS</span></span>

[<span data-ttu-id="f9493-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9493-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="f9493-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9493-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="f9493-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9493-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
