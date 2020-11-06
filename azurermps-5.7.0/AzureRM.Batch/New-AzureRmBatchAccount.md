---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: c4a8eb0bc75660c13ce8f8492b72cce8a77280e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576638"
---
# <span data-ttu-id="c025d-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c025d-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="c025d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c025d-102">SYNOPSIS</span></span>
<span data-ttu-id="c025d-103">Skapar ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c025d-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c025d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c025d-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c025d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c025d-105">DESCRIPTION</span></span>
<span data-ttu-id="c025d-106">Cmdleten **New-AzureRmBatchAccount** skapar ett Azure Batch-konto för angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="c025d-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="c025d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c025d-107">EXAMPLES</span></span>

### <span data-ttu-id="c025d-108">Exempel 1: skapa ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="c025d-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="c025d-109">Det här kommandot skapar ett batch-konto med namnet pfuller med resurs gruppen ResourceGroup03 på platsen för USA.</span><span class="sxs-lookup"><span data-stu-id="c025d-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="c025d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c025d-110">PARAMETERS</span></span>

### <span data-ttu-id="c025d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c025d-111">-AccountName</span></span>
<span data-ttu-id="c025d-112">Anger namnet på det kommando konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c025d-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="c025d-113">Namn på kommandofiler måste vara mellan 3 och 24 tecken långa och får endast innehålla siffror och gemener.</span><span class="sxs-lookup"><span data-stu-id="c025d-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c025d-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="c025d-115">Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="c025d-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c025d-116">-DefaultProfile</span></span>
<span data-ttu-id="c025d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c025d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c025d-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c025d-118">-KeyVaultId</span></span>
<span data-ttu-id="c025d-119">Resurs-ID för Azure Key Vault som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="c025d-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="c025d-120">-KeyVaultUrl</span></span>
<span data-ttu-id="c025d-121">Webb adressen för det Azure Key-valv som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="c025d-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="c025d-122">-Location</span></span>
<span data-ttu-id="c025d-123">Anger den region där den här cmdleten skapar kontot.</span><span class="sxs-lookup"><span data-stu-id="c025d-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="c025d-124">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="c025d-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="c025d-125">-PoolAllocationMode</span></span>
<span data-ttu-id="c025d-126">Tilldelnings läget för att skapa pooler i batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="c025d-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: PoolAllocationMode
Parameter Sets: (All)
Aliases: 
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c025d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c025d-128">Anger namnet på resurs gruppen som den här cmdleten skapar för kontot.</span><span class="sxs-lookup"><span data-stu-id="c025d-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c025d-129">-Tag</span></span>
<span data-ttu-id="c025d-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c025d-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c025d-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c025d-131">For example:</span></span>

<span data-ttu-id="c025d-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c025d-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c025d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c025d-133">CommonParameters</span></span>
<span data-ttu-id="c025d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c025d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c025d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c025d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c025d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c025d-136">INPUTS</span></span>

### <span data-ttu-id="c025d-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="c025d-137">None</span></span>
<span data-ttu-id="c025d-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c025d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c025d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c025d-139">OUTPUTS</span></span>

### <span data-ttu-id="c025d-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c025d-140">BatchAccountContext</span></span>

## <span data-ttu-id="c025d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c025d-141">NOTES</span></span>

## <span data-ttu-id="c025d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c025d-142">RELATED LINKS</span></span>

[<span data-ttu-id="c025d-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c025d-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="c025d-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c025d-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="c025d-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c025d-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="c025d-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c025d-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
