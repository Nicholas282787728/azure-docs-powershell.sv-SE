---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 3ded950659546b6ec2a25271bc09718c937d401b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923610"
---
# <span data-ttu-id="51305-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51305-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="51305-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51305-102">SYNOPSIS</span></span>
<span data-ttu-id="51305-103">Skapar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="51305-103">Creates a Storage account.</span></span>

## <span data-ttu-id="51305-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51305-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51305-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51305-105">DESCRIPTION</span></span>
<span data-ttu-id="51305-106">Cmdleten **New-AzStorageAccount** skapar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="51305-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="51305-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51305-107">EXAMPLES</span></span>

### <span data-ttu-id="51305-108">Exempel 1: skapa ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="51305-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="51305-109">Det här kommandot skapar ett lagrings konto för resurs grupps namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51305-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="51305-110">Exempel 2: skapa ett Blob Storage-konto med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="51305-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="51305-111">Det här kommandot skapar ett BLOB-lagringssystem med BlobStorage Natura och hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="51305-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="51305-112">Exempel 3: skapa ett lagrings konto med Natura StorageV2 och generera och tilldela en identitet för Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="51305-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="51305-113">Det här kommandot skapar ett lagrings konto med typen StorageV2.</span><span class="sxs-lookup"><span data-stu-id="51305-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="51305-114">Den skapar också och tilldelar en identitet som kan användas för att hantera konto nycklar via Azure-nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="51305-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="51305-115">Exempel 4: skapa ett lagrings konto med NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="51305-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="51305-116">Det här kommandot skapar ett lagrings konto med egenskapen NetworkRuleSet från JSON</span><span class="sxs-lookup"><span data-stu-id="51305-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="51305-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51305-117">PARAMETERS</span></span>

### <span data-ttu-id="51305-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="51305-118">-AccessTier</span></span>
<span data-ttu-id="51305-119">Anger åtkomst nivån för det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51305-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="51305-120">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="51305-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="51305-121">Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="51305-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="51305-122">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="51305-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="51305-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51305-123">-AsJob</span></span>
<span data-ttu-id="51305-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51305-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51305-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="51305-125">-AssignIdentity</span></span>
<span data-ttu-id="51305-126">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="51305-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="51305-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="51305-127">-CustomDomainName</span></span>
<span data-ttu-id="51305-128">Anger namnet på lagrings kontots anpassade domän.</span><span class="sxs-lookup"><span data-stu-id="51305-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="51305-129">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="51305-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51305-130">-DefaultProfile</span></span>
<span data-ttu-id="51305-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51305-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51305-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="51305-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="51305-133">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="51305-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="51305-134">-Sort</span><span class="sxs-lookup"><span data-stu-id="51305-134">-Kind</span></span>
<span data-ttu-id="51305-135">Anger den typ av lagrings konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="51305-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="51305-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="51305-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51305-137">Lagringsrelaterade.</span><span class="sxs-lookup"><span data-stu-id="51305-137">Storage.</span></span> <span data-ttu-id="51305-138">Allmänt syfte lagrings konto som stöder lagring av blobbar, tabeller, köer, filer och diskar.</span><span class="sxs-lookup"><span data-stu-id="51305-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="51305-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="51305-139">StorageV2.</span></span> <span data-ttu-id="51305-140">Allmänt syfte version 2 (GPv2) lagrings konto som har stöd för blobbar, tabeller, köer, filer och diskar med avancerade funktioner som data lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="51305-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="51305-141">BlobStorage.</span></span> <span data-ttu-id="51305-142">Blob Storage-konto som endast stöder lagring av BLOB.</span><span class="sxs-lookup"><span data-stu-id="51305-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="51305-143">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51305-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="51305-144">-Location</span></span>
<span data-ttu-id="51305-145">Anger platsen för det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="51305-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="51305-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="51305-146">-Name</span></span>
<span data-ttu-id="51305-147">Anger namnet på det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="51305-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="51305-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="51305-148">-NetworkRuleSet</span></span>
<span data-ttu-id="51305-149">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel tjänster som är tillåtna för att kringgå reglerna och för att hantera förfrågningar som inte matchar någon av de definierade reglerna.</span><span class="sxs-lookup"><span data-stu-id="51305-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="51305-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51305-150">-ResourceGroupName</span></span>
<span data-ttu-id="51305-151">Anger namnet på den resurs grupp där lagrings kontot ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="51305-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="51305-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="51305-152">-SkuName</span></span>
<span data-ttu-id="51305-153">Anger SKU-namnet på det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51305-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="51305-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="51305-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51305-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="51305-155">Standard_LRS.</span></span> <span data-ttu-id="51305-156">Lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="51305-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="51305-157">Standard_ZRS.</span></span> <span data-ttu-id="51305-158">Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="51305-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="51305-159">Standard_GRS.</span></span> <span data-ttu-id="51305-160">Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="51305-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="51305-161">Standard_RAGRS.</span></span> <span data-ttu-id="51305-162">Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="51305-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="51305-163">Premium_LRS.</span></span> <span data-ttu-id="51305-164">Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="51305-164">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51305-165">-Tagg</span><span class="sxs-lookup"><span data-stu-id="51305-165">-Tag</span></span>
<span data-ttu-id="51305-166">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="51305-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="51305-167">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="51305-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51305-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="51305-168">-UseSubDomain</span></span>
<span data-ttu-id="51305-169">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="51305-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="51305-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51305-170">CommonParameters</span></span>
<span data-ttu-id="51305-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51305-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51305-172">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51305-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51305-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51305-173">INPUTS</span></span>

### <span data-ttu-id="51305-174">System. String</span><span class="sxs-lookup"><span data-stu-id="51305-174">System.String</span></span>

### <span data-ttu-id="51305-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51305-175">System.Boolean</span></span>

## <span data-ttu-id="51305-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51305-176">OUTPUTS</span></span>

### <span data-ttu-id="51305-177">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51305-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="51305-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51305-178">NOTES</span></span>

## <span data-ttu-id="51305-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51305-179">RELATED LINKS</span></span>

[<span data-ttu-id="51305-180">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51305-180">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="51305-181">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51305-181">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="51305-182">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51305-182">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
