---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755094"
---
# <span data-ttu-id="1ff38-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ff38-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="1ff38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ff38-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff38-103">Skapar ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="1ff38-103">Creates a Batch account.</span></span>

## <span data-ttu-id="1ff38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ff38-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ff38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ff38-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff38-106">Cmdleten **New-AzBatchAccount** skapar ett Azure Batch-konto för angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="1ff38-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="1ff38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ff38-107">EXAMPLES</span></span>

### <span data-ttu-id="1ff38-108">Exempel 1: skapa ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="1ff38-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="1ff38-109">Det här kommandot skapar ett batch-konto med namnet pfuller med resurs gruppen ResourceGroup03 på platsen för USA.</span><span class="sxs-lookup"><span data-stu-id="1ff38-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="1ff38-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ff38-110">PARAMETERS</span></span>

### <span data-ttu-id="1ff38-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ff38-111">-AccountName</span></span>
<span data-ttu-id="1ff38-112">Anger namnet på det kommando konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1ff38-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="1ff38-113">Namn på kommandofiler måste vara mellan 3 och 24 tecken långa och får endast innehålla siffror och gemener.</span><span class="sxs-lookup"><span data-stu-id="1ff38-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1ff38-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="1ff38-115">Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="1ff38-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff38-116">-DefaultProfile</span></span>
<span data-ttu-id="1ff38-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff38-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff38-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1ff38-118">-KeyVaultId</span></span>
<span data-ttu-id="1ff38-119">Resurs-ID för Azure Key Vault som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="1ff38-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="1ff38-120">-KeyVaultUrl</span></span>
<span data-ttu-id="1ff38-121">Webb adressen för det Azure Key-valv som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="1ff38-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ff38-122">-Location</span></span>
<span data-ttu-id="1ff38-123">Anger den region där den här cmdleten skapar kontot.</span><span class="sxs-lookup"><span data-stu-id="1ff38-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="1ff38-124">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="1ff38-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="1ff38-125">-PoolAllocationMode</span></span>
<span data-ttu-id="1ff38-126">Tilldelnings läget för att skapa pooler i batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="1ff38-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff38-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ff38-128">Anger namnet på resurs gruppen som den här cmdleten skapar för kontot.</span><span class="sxs-lookup"><span data-stu-id="1ff38-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff38-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1ff38-129">-Tag</span></span>
<span data-ttu-id="1ff38-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1ff38-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ff38-131">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1ff38-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ff38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff38-132">CommonParameters</span></span>
<span data-ttu-id="1ff38-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff38-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff38-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff38-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ff38-135">INPUTS</span></span>

### <span data-ttu-id="1ff38-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff38-136">System.String</span></span>

### <span data-ttu-id="1ff38-137">System. Nullable ' 1 [[Microsoft.Azure.Management.BatCH. Models. PoolAllocationMode, Microsoft.Azure.Management.BatCH, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1ff38-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1ff38-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1ff38-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ff38-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ff38-139">OUTPUTS</span></span>

### <span data-ttu-id="1ff38-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ff38-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1ff38-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ff38-141">NOTES</span></span>

## <span data-ttu-id="1ff38-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ff38-142">RELATED LINKS</span></span>

[<span data-ttu-id="1ff38-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ff38-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="1ff38-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ff38-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="1ff38-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ff38-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="1ff38-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1ff38-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)