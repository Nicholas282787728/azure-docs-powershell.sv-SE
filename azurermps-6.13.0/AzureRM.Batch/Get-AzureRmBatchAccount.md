---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: ddc3bab48e766f80375fdf98add15e16e0086fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574037"
---
# <span data-ttu-id="4840a-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4840a-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="4840a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4840a-102">SYNOPSIS</span></span>
<span data-ttu-id="4840a-103">Hämtar ett batchjobb för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4840a-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4840a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4840a-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4840a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4840a-105">DESCRIPTION</span></span>
<span data-ttu-id="4840a-106">Cmdleten **Get-AzureRmBatchAccount** får ett Azure Batch-konto i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4840a-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="4840a-107">Du kan använda parametern *AccountName* för att få ett enskilt konto, eller så kan du använda parametern *ResourceGroupName* för att hämta konton under den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4840a-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="4840a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4840a-108">EXAMPLES</span></span>

### <span data-ttu-id="4840a-109">Exempel 1: Hämta ett batch-konto efter namn</span><span class="sxs-lookup"><span data-stu-id="4840a-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="4840a-110">Det här kommandot får batch-kontot pfuller.</span><span class="sxs-lookup"><span data-stu-id="4840a-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="4840a-111">Exempel 2: Hämta de grupp konton som är kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="4840a-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="4840a-112">Det här kommandot hämtar de konton som är kopplade till resurs gruppen CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="4840a-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="4840a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4840a-113">PARAMETERS</span></span>

### <span data-ttu-id="4840a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4840a-114">-AccountName</span></span>
<span data-ttu-id="4840a-115">Anger namnet på ett konto.</span><span class="sxs-lookup"><span data-stu-id="4840a-115">Specifies the name of an account.</span></span>
<span data-ttu-id="4840a-116">Om du anger ett konto namn returneras bara det kontot i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4840a-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4840a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4840a-117">-DefaultProfile</span></span>
<span data-ttu-id="4840a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4840a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4840a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4840a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4840a-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4840a-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4840a-121">Om du anger en resurs grupp får denna cmdlet konton under den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4840a-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4840a-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4840a-122">-Tag</span></span>
<span data-ttu-id="4840a-123">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4840a-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4840a-124">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} med den här cmdleten får du konton som innehåller taggarna som anges.</span><span class="sxs-lookup"><span data-stu-id="4840a-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4840a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4840a-125">CommonParameters</span></span>
<span data-ttu-id="4840a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4840a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4840a-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4840a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4840a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4840a-128">INPUTS</span></span>

### <span data-ttu-id="4840a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4840a-129">System.String</span></span>

### <span data-ttu-id="4840a-130">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4840a-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4840a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4840a-131">OUTPUTS</span></span>

### <span data-ttu-id="4840a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4840a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4840a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4840a-133">NOTES</span></span>

## <span data-ttu-id="4840a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4840a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4840a-135">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4840a-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="4840a-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4840a-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="4840a-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4840a-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="4840a-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4840a-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
