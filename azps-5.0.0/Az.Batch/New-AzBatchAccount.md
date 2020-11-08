---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270888"
---
# <span data-ttu-id="62bd0-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62bd0-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="62bd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="62bd0-103">Skapar ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="62bd0-103">Creates a Batch account.</span></span>

## <span data-ttu-id="62bd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62bd0-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bd0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="62bd0-106">Cmdleten **New-AzBatchAccount** skapar ett Azure Batch-konto för angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="62bd0-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="62bd0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="62bd0-108">Exempel 1: skapa ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="62bd0-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="62bd0-109">Det här kommandot skapar ett batch-konto med namnet pfuller med resurs gruppen ResourceGroup03 på platsen för USA.</span><span class="sxs-lookup"><span data-stu-id="62bd0-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="62bd0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="62bd0-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62bd0-111">-AccountName</span></span>
<span data-ttu-id="62bd0-112">Anger namnet på det kommando konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="62bd0-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="62bd0-113">Namn på kommandofiler måste vara mellan 3 och 24 tecken långa och får endast innehålla siffror och gemener.</span><span class="sxs-lookup"><span data-stu-id="62bd0-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="62bd0-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="62bd0-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="62bd0-115">Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="62bd0-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="62bd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bd0-116">-DefaultProfile</span></span>
<span data-ttu-id="62bd0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62bd0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62bd0-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="62bd0-118">-IdentityType</span></span>
<span data-ttu-id="62bd0-119">Identiteten som är associerad med BatchAccount</span><span class="sxs-lookup"><span data-stu-id="62bd0-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd0-120">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="62bd0-120">-KeyVaultId</span></span>
<span data-ttu-id="62bd0-121">Resurs-ID för Azure Key Vault som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="62bd0-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="62bd0-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="62bd0-122">-KeyVaultUrl</span></span>
<span data-ttu-id="62bd0-123">Webb adressen för det Azure Key-valv som är kopplat till batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="62bd0-123">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="62bd0-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="62bd0-124">-Location</span></span>
<span data-ttu-id="62bd0-125">Anger den region där den här cmdleten skapar kontot.</span><span class="sxs-lookup"><span data-stu-id="62bd0-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="62bd0-126">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="62bd0-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="62bd0-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="62bd0-127">-PoolAllocationMode</span></span>
<span data-ttu-id="62bd0-128">Tilldelnings läget för att skapa pooler i batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="62bd0-128">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="62bd0-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="62bd0-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="62bd0-130">Åtkomst typen offentlig nätverk</span><span class="sxs-lookup"><span data-stu-id="62bd0-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bd0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bd0-131">-ResourceGroupName</span></span>
<span data-ttu-id="62bd0-132">Anger namnet på resurs gruppen som den här cmdleten skapar för kontot.</span><span class="sxs-lookup"><span data-stu-id="62bd0-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="62bd0-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="62bd0-133">-Tag</span></span>
<span data-ttu-id="62bd0-134">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="62bd0-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="62bd0-135">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="62bd0-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="62bd0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bd0-136">CommonParameters</span></span>
<span data-ttu-id="62bd0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bd0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bd0-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62bd0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bd0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62bd0-139">INPUTS</span></span>

### <span data-ttu-id="62bd0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="62bd0-140">System.String</span></span>

### <span data-ttu-id="62bd0-141">System. Nullable ' 1 [[Microsoft.Azure.Management.BatCH. Models. PoolAllocationMode, Microsoft.Azure.Management.BatCH, version = 9.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62bd0-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="62bd0-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="62bd0-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="62bd0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62bd0-143">OUTPUTS</span></span>

### <span data-ttu-id="62bd0-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="62bd0-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="62bd0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62bd0-145">NOTES</span></span>

## <span data-ttu-id="62bd0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62bd0-146">RELATED LINKS</span></span>

[<span data-ttu-id="62bd0-147">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62bd0-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="62bd0-148">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62bd0-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="62bd0-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62bd0-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="62bd0-150">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="62bd0-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
