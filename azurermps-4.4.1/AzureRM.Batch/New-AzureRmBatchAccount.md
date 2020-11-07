---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756001"
---
# <span data-ttu-id="1d2c8-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1d2c8-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="1d2c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2c8-103">Skapar ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d2c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d2c8-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d2c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d2c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1d2c8-106">Cmdleten **New-AzureRmBatchAccount** skapar ett Azure Batch-konto för angiven resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="1d2c8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d2c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1d2c8-108">Exempel 1: skapa ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="1d2c8-108">Example 1: Create a Batch account</span></span>
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

<span data-ttu-id="1d2c8-109">Det här kommandot skapar ett batch-konto med namnet pfuller med resurs gruppen ResourceGroup03 på platsen för USA.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="1d2c8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d2c8-110">PARAMETERS</span></span>

### <span data-ttu-id="1d2c8-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d2c8-111">-AccountName</span></span>
<span data-ttu-id="1d2c8-112">Anger namnet på det kommando konto som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="1d2c8-113">Namn på kommandofiler måste vara mellan 3 och 24 tecken långa och får endast innehålla siffror och gemener.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="1d2c8-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d2c8-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="1d2c8-115">Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="1d2c8-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="1d2c8-116">-Location</span></span>
<span data-ttu-id="1d2c8-117">Anger den region där den här cmdleten skapar kontot.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="1d2c8-118">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="1d2c8-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="1d2c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d2c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d2c8-120">Anger namnet på resurs gruppen som den här cmdleten skapar för kontot.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="1d2c8-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1d2c8-121">-Tag</span></span>
<span data-ttu-id="1d2c8-122">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1d2c8-123">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1d2c8-123">For example:</span></span>

<span data-ttu-id="1d2c8-124">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1d2c8-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1d2c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2c8-125">-DefaultProfile</span></span>
<span data-ttu-id="1d2c8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d2c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2c8-127">CommonParameters</span></span>
<span data-ttu-id="1d2c8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d2c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2c8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d2c8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2c8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d2c8-130">INPUTS</span></span>

## <span data-ttu-id="1d2c8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d2c8-131">OUTPUTS</span></span>

### <span data-ttu-id="1d2c8-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1d2c8-132">BatchAccountContext</span></span>

## <span data-ttu-id="1d2c8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d2c8-133">NOTES</span></span>

## <span data-ttu-id="1d2c8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d2c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d2c8-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1d2c8-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="1d2c8-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1d2c8-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="1d2c8-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1d2c8-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="1d2c8-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1d2c8-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
