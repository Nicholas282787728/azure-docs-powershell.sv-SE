---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758254"
---
# <span data-ttu-id="fa241-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa241-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="fa241-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa241-102">SYNOPSIS</span></span>
<span data-ttu-id="fa241-103">Skapar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fa241-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa241-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa241-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fa241-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa241-105">DESCRIPTION</span></span>
<span data-ttu-id="fa241-106">Cmdleten **New-AzureRmStorageAccount** skapar ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="fa241-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="fa241-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa241-107">EXAMPLES</span></span>

### <span data-ttu-id="fa241-108">Exempel 1: skapa ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fa241-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="fa241-109">Det här kommandot skapar ett lagrings konto för resurs grupps namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fa241-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="fa241-110">Exempel 2: skapa ett Blob Storage-konto som använder Storage Service Encryption</span><span class="sxs-lookup"><span data-stu-id="fa241-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="fa241-111">Det här kommandot skapar ett Blob Storage-konto som använder typen varm åtkomst.</span><span class="sxs-lookup"><span data-stu-id="fa241-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="fa241-112">Kontot har aktiverat Storage Service-kryptering för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa241-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="fa241-113">Exempel 3: skapa ett lagrings konto som möjliggör kryptering av lagrings tjänst för blob och fil tjänster och skapa och tilldela en identitet för Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="fa241-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="fa241-114">Det här kommandot skapar ett lagrings konto med aktiverat Storage Service-kryptering för blob och fil tjänster.</span><span class="sxs-lookup"><span data-stu-id="fa241-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="fa241-115">Den skapar också och tilldelar en identitet som kan användas för att hantera konto nycklar via Azure-nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="fa241-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="fa241-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa241-116">PARAMETERS</span></span>

### <span data-ttu-id="fa241-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fa241-117">-AccessTier</span></span>
<span data-ttu-id="fa241-118">Anger åtkomst nivån för det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa241-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fa241-119">De acceptabla värdena för denna parameter är: varmt och coolt.</span><span class="sxs-lookup"><span data-stu-id="fa241-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="fa241-120">Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fa241-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="fa241-121">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fa241-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fa241-122">-AssignIdentity</span></span>
<span data-ttu-id="fa241-123">Skapa och tilldela en ny lagrings konto identitet för det här lagrings kontot för användning med hanterings tjänster som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="fa241-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fa241-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fa241-124">-CustomDomainName</span></span>
<span data-ttu-id="fa241-125">Anger namnet på lagrings kontots anpassade domän.</span><span class="sxs-lookup"><span data-stu-id="fa241-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="fa241-126">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="fa241-127">-EnableEncryptionService</span></span>
<span data-ttu-id="fa241-128">Anger om denna cmdlet aktiverar Storage Service-kryptering för lagrings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa241-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="fa241-129">Stöd för Azure-blob och Azure File Services.</span><span class="sxs-lookup"><span data-stu-id="fa241-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="fa241-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="fa241-131">Anger om lagrings kontot endast aktiverar HTTPS-trafik.</span><span class="sxs-lookup"><span data-stu-id="fa241-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="fa241-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fa241-132">-InformationAction</span></span>
<span data-ttu-id="fa241-133">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fa241-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fa241-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fa241-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa241-135">Vidare</span><span class="sxs-lookup"><span data-stu-id="fa241-135">Continue</span></span>
- <span data-ttu-id="fa241-136">Över</span><span class="sxs-lookup"><span data-stu-id="fa241-136">Ignore</span></span>
- <span data-ttu-id="fa241-137">Inquire</span><span class="sxs-lookup"><span data-stu-id="fa241-137">Inquire</span></span>
- <span data-ttu-id="fa241-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fa241-138">SilentlyContinue</span></span>
- <span data-ttu-id="fa241-139">Stanna</span><span class="sxs-lookup"><span data-stu-id="fa241-139">Stop</span></span>
- <span data-ttu-id="fa241-140">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fa241-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fa241-141">-InformationVariable</span></span>
<span data-ttu-id="fa241-142">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fa241-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-143">-Sort</span><span class="sxs-lookup"><span data-stu-id="fa241-143">-Kind</span></span>
<span data-ttu-id="fa241-144">Anger den typ av lagrings konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="fa241-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fa241-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fa241-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa241-146">Lagringsrelaterade.</span><span class="sxs-lookup"><span data-stu-id="fa241-146">Storage.</span></span>
<span data-ttu-id="fa241-147">Allmänt syfte lagrings konto som stöder lagring av blobbar, tabeller, köer, filer och diskar.</span><span class="sxs-lookup"><span data-stu-id="fa241-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="fa241-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fa241-148">BlobStorage.</span></span>
<span data-ttu-id="fa241-149">Blob Storage-konto som endast stöder lagring av BLOB.</span><span class="sxs-lookup"><span data-stu-id="fa241-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="fa241-150">Standardvärdet är lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="fa241-151">-Location</span></span>
<span data-ttu-id="fa241-152">Anger platsen för det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fa241-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa241-153">-Name</span></span>
<span data-ttu-id="fa241-154">Anger namnet på det lagrings konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fa241-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="fa241-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa241-155">-NetworkRuleSet</span></span>
<span data-ttu-id="fa241-156">NetworkRuleSet för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fa241-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="fa241-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa241-157">-ResourceGroupName</span></span>
<span data-ttu-id="fa241-158">Anger namnet på den resurs grupp där lagrings kontot ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="fa241-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="fa241-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fa241-159">-SkuName</span></span>
<span data-ttu-id="fa241-160">Anger SKU-namnet på det lagrings konto som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa241-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fa241-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fa241-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa241-162">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="fa241-162">Standard_LRS.</span></span>
<span data-ttu-id="fa241-163">Lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="fa241-164">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fa241-164">Standard_ZRS.</span></span>
<span data-ttu-id="fa241-165">Zone – redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="fa241-166">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="fa241-166">Standard_GRS.</span></span>
<span data-ttu-id="fa241-167">Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="fa241-168">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="fa241-168">Standard_RAGRS.</span></span>
<span data-ttu-id="fa241-169">Läs åtkomst Geo-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="fa241-170">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fa241-170">Premium_LRS.</span></span>
<span data-ttu-id="fa241-171">Premium lokalt-redundant lagring.</span><span class="sxs-lookup"><span data-stu-id="fa241-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-172">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fa241-172">-Tag</span></span>
<span data-ttu-id="fa241-173">Om du anger ett värde för BlobStorage för parametern *sort* måste du ange ett värde för parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fa241-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="fa241-174">Om du anger ett värde för lagring för denna *sort* parameter ska du inte ange parametern *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fa241-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-175">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="fa241-175">-UseSubDomain</span></span>
<span data-ttu-id="fa241-176">Anger om indirekt CName-verifiering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="fa241-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa241-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa241-177">-DefaultProfile</span></span>
<span data-ttu-id="fa241-178">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa241-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa241-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa241-179">CommonParameters</span></span>
<span data-ttu-id="fa241-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa241-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa241-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa241-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa241-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa241-182">INPUTS</span></span>

## <span data-ttu-id="fa241-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa241-183">OUTPUTS</span></span>

## <span data-ttu-id="fa241-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa241-184">NOTES</span></span>

## <span data-ttu-id="fa241-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa241-185">RELATED LINKS</span></span>

[<span data-ttu-id="fa241-186">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa241-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="fa241-187">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa241-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="fa241-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa241-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


