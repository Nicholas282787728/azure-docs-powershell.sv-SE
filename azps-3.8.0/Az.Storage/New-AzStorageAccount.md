---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090872"
---
# <span data-ttu-id="e18ee-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ee-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="e18ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e18ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e18ee-103">Skapar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e18ee-103">Creates a Storage account.</span></span>

## <span data-ttu-id="e18ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e18ee-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e18ee-105">DESCRIPTION</span></span>
<span data-ttu-id="e18ee-106">Cmdleten **New-AzStorageAccount** skapar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="e18ee-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="e18ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e18ee-107">EXAMPLES</span></span>

### <span data-ttu-id="e18ee-108">Exempel 1: skapa ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="e18ee-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="e18ee-109">Det här kommandot skapar ett lagrings konto för resurs grupps namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e18ee-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="e18ee-110">Exempel 2: skapa ett Blob Storage-konto med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="e18ee-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="e18ee-111">Det här kommandot skapar ett BLOB-lagringssystem med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="e18ee-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="e18ee-112">Exempel 3: skapa ett lagrings konto med Natura StorageV2 och generera och tilldela en identitet för Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="e18ee-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="e18ee-113">Det här kommandot skapar ett lagrings konto med typen StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e18ee-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="e18ee-114">Den skapar också och tilldelar en identitet som kan användas för att hantera konto nycklar via Azure-nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="e18ee-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="e18ee-115">Exempel 4: skapa ett lagrings konto med NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="e18ee-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="e18ee-116">Det här kommandot skapar ett lagrings konto med egenskapen NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="e18ee-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="e18ee-117">Exempel 5: skapa ett lagrings konto med hierarkiskt namn område aktiverat.</span><span class="sxs-lookup"><span data-stu-id="e18ee-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="e18ee-118">Det här kommandot skapar ett lagrings konto med hierarkiskt namn område aktiverat.</span><span class="sxs-lookup"><span data-stu-id="e18ee-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="e18ee-119">Exempel 6: skapa ett lagrings konto med Azure-filer AAD DS-identifiering och aktivera stor fil delning.</span><span class="sxs-lookup"><span data-stu-id="e18ee-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="e18ee-120">Det här kommandot skapar ett lagrings konto med Azure-filer AAD DS-identifiering och aktiverar stor fil resurs..</span><span class="sxs-lookup"><span data-stu-id="e18ee-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="e18ee-121">Exempel 8: skapa ett lagrings konto med konto – begränsad krypterings nycklar för kö och tabell tjänst.</span><span class="sxs-lookup"><span data-stu-id="e18ee-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="e18ee-122">Det här kommandot skapar ett lagrings konto med hanterat konto – begränsat krypterings nycklar, så att kön och tabellen använder samma krypterings nycklar med blobben och fil tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e18ee-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="e18ee-123">Hämta sedan egenskaperna för lagrings kontot och Visa krypterings typen för kö-och tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e18ee-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="e18ee-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e18ee-124">PARAMETERS</span></span>

### <span data-ttu-id="e18ee-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="e18ee-125">-AccessTier</span></span>
<span data-ttu-id="e18ee-126">Anger åtkomst nivån för det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e18ee-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e18ee-127">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="e18ee-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="e18ee-128">Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="e18ee-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="e18ee-129">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="e18ee-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="e18ee-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e18ee-130">-AsJob</span></span>
<span data-ttu-id="e18ee-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e18ee-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e18ee-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e18ee-132">-AssignIdentity</span></span>
<span data-ttu-id="e18ee-133">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="e18ee-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e18ee-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e18ee-134">-CustomDomainName</span></span>
<span data-ttu-id="e18ee-135">Anger namnet på lagrings kontots anpassade domän.</span><span class="sxs-lookup"><span data-stu-id="e18ee-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="e18ee-136">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="e18ee-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18ee-137">-DefaultProfile</span></span>
<span data-ttu-id="e18ee-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e18ee-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18ee-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="e18ee-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="e18ee-140">Aktivera Azure-filer för Azure Active Directory Domain Service för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e18ee-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="e18ee-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="e18ee-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="e18ee-142">Anger om lagrings kontot aktiverar ett hierarkiskt namn område.</span><span class="sxs-lookup"><span data-stu-id="e18ee-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="e18ee-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="e18ee-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="e18ee-144">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="e18ee-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="e18ee-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="e18ee-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="e18ee-146">Anger om lagrings kontot kan hantera stora fil resurser med mer än 5 TiB kapacitet.</span><span class="sxs-lookup"><span data-stu-id="e18ee-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="e18ee-147">När kontot är aktiverat kan funktionen inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="e18ee-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="e18ee-148">För närvarande stöds endast för LRS-och ZRS-replikeringstyp, därför är det inte möjligt att konvertera konton till geo-redundanta konton.</span><span class="sxs-lookup"><span data-stu-id="e18ee-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="e18ee-149">Läs mer i https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="e18ee-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="e18ee-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="e18ee-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="e18ee-151">Ange krypterings typen för kön.</span><span class="sxs-lookup"><span data-stu-id="e18ee-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="e18ee-152">Standardvärdet är service.</span><span class="sxs-lookup"><span data-stu-id="e18ee-152">The default value is Service.</span></span>
<span data-ttu-id="e18ee-153">-Konto: kön krypteras med krypterings nycklar med konto omfattning.</span><span class="sxs-lookup"><span data-stu-id="e18ee-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="e18ee-154">-Service: kö kommer alltid att vara krypterad med Service-Managed nycklar.</span><span class="sxs-lookup"><span data-stu-id="e18ee-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="e18ee-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="e18ee-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="e18ee-156">Ange krypterings typ för tabellen.</span><span class="sxs-lookup"><span data-stu-id="e18ee-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="e18ee-157">Standardvärdet är service.</span><span class="sxs-lookup"><span data-stu-id="e18ee-157">The default value is Service.</span></span>
- <span data-ttu-id="e18ee-158">Konto: tabellen krypteras med krypterings nycklar med konto – begränsad.</span><span class="sxs-lookup"><span data-stu-id="e18ee-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="e18ee-159">Tjänst: tabellen kommer alltid att vara krypterad med Service-Managed nycklar.</span><span class="sxs-lookup"><span data-stu-id="e18ee-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="e18ee-160">-Sort</span><span class="sxs-lookup"><span data-stu-id="e18ee-160">-Kind</span></span>
<span data-ttu-id="e18ee-161">Anger den typ av lagrings konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="e18ee-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e18ee-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e18ee-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e18ee-163">Lagringsrelaterade.</span><span class="sxs-lookup"><span data-stu-id="e18ee-163">Storage.</span></span> <span data-ttu-id="e18ee-164">Allmänt syfte lagrings konto som stöder lagring av blobbar, tabeller, köer, filer och diskar.</span><span class="sxs-lookup"><span data-stu-id="e18ee-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="e18ee-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e18ee-165">StorageV2.</span></span> <span data-ttu-id="e18ee-166">Allmänt syfte version 2 (GPv2) lagrings konto som har stöd för blobbar, tabeller, köer, filer och diskar med avancerade funktioner som data lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="e18ee-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="e18ee-167">BlobStorage.</span></span> <span data-ttu-id="e18ee-168">Blob Storage-konto som endast stöder lagring av BLOB.</span><span class="sxs-lookup"><span data-stu-id="e18ee-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="e18ee-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="e18ee-169">BlockBlobStorage.</span></span> <span data-ttu-id="e18ee-170">Spärra Blob Storage-konto som endast stöder lagring av Block-Blob.</span><span class="sxs-lookup"><span data-stu-id="e18ee-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="e18ee-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="e18ee-171">FileStorage.</span></span> <span data-ttu-id="e18ee-172">Fil lagrings konto som endast stöder lagring av filer.</span><span class="sxs-lookup"><span data-stu-id="e18ee-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="e18ee-173">Standardvärdet är StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e18ee-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18ee-174">-Plats</span><span class="sxs-lookup"><span data-stu-id="e18ee-174">-Location</span></span>
<span data-ttu-id="e18ee-175">Anger platsen för det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e18ee-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="e18ee-176">-Namn</span><span class="sxs-lookup"><span data-stu-id="e18ee-176">-Name</span></span>
<span data-ttu-id="e18ee-177">Anger namnet på det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e18ee-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="e18ee-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e18ee-178">-NetworkRuleSet</span></span>
<span data-ttu-id="e18ee-179">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="e18ee-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="e18ee-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18ee-180">-ResourceGroupName</span></span>
<span data-ttu-id="e18ee-181">Anger namnet på den resurs grupp där lagrings kontot ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e18ee-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="e18ee-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e18ee-182">-SkuName</span></span>
<span data-ttu-id="e18ee-183">Anger SKU-namnet på det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e18ee-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e18ee-184">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e18ee-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e18ee-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-185">Standard_LRS.</span></span> <span data-ttu-id="e18ee-186">Lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="e18ee-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-187">Standard_ZRS.</span></span> <span data-ttu-id="e18ee-188">Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="e18ee-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-189">Standard_GRS.</span></span> <span data-ttu-id="e18ee-190">Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="e18ee-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-191">Standard_RAGRS.</span></span> <span data-ttu-id="e18ee-192">Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="e18ee-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-193">Premium_LRS.</span></span> <span data-ttu-id="e18ee-194">Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="e18ee-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="e18ee-195">Premium_ZRS.</span></span> <span data-ttu-id="e18ee-196">Premium Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="e18ee-197">Standard_GZRS-Geo-redundant Zone-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="e18ee-198">Standard_RAGZRS-Läs åtkomst Geo-redundant Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="e18ee-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="e18ee-199">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e18ee-199">-Tag</span></span>
<span data-ttu-id="e18ee-200">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="e18ee-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e18ee-201">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e18ee-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e18ee-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="e18ee-202">-UseSubDomain</span></span>
<span data-ttu-id="e18ee-203">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="e18ee-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="e18ee-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18ee-204">CommonParameters</span></span>
<span data-ttu-id="e18ee-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18ee-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18ee-206">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e18ee-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18ee-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e18ee-207">INPUTS</span></span>

### <span data-ttu-id="e18ee-208">System. String</span><span class="sxs-lookup"><span data-stu-id="e18ee-208">System.String</span></span>

## <span data-ttu-id="e18ee-209">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e18ee-209">OUTPUTS</span></span>

### <span data-ttu-id="e18ee-210">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ee-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e18ee-211">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e18ee-211">NOTES</span></span>

## <span data-ttu-id="e18ee-212">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e18ee-212">RELATED LINKS</span></span>

[<span data-ttu-id="e18ee-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ee-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="e18ee-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ee-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="e18ee-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ee-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
