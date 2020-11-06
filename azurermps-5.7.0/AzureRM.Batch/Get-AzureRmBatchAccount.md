---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574420"
---
# <span data-ttu-id="f4381-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f4381-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="f4381-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4381-102">SYNOPSIS</span></span>
<span data-ttu-id="f4381-103">Hämtar ett batchjobb för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f4381-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4381-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4381-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4381-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4381-105">DESCRIPTION</span></span>
<span data-ttu-id="f4381-106">Cmdleten **Get-AzureRmBatchAccount** får ett Azure Batch-konto i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f4381-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="f4381-107">Du kan använda parametern *AccountName* för att få ett enskilt konto, eller så kan du använda parametern *ResourceGroupName* för att hämta konton under den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4381-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="f4381-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4381-108">EXAMPLES</span></span>

### <span data-ttu-id="f4381-109">Exempel 1: Hämta ett batch-konto efter namn</span><span class="sxs-lookup"><span data-stu-id="f4381-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="f4381-110">Det här kommandot får batch-kontot pfuller.</span><span class="sxs-lookup"><span data-stu-id="f4381-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="f4381-111">Exempel 2: Hämta de grupp konton som är kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f4381-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="f4381-112">Det här kommandot hämtar de konton som är kopplade till resurs gruppen CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="f4381-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="f4381-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4381-113">PARAMETERS</span></span>

### <span data-ttu-id="f4381-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4381-114">-AccountName</span></span>
<span data-ttu-id="f4381-115">Anger namnet på ett konto.</span><span class="sxs-lookup"><span data-stu-id="f4381-115">Specifies the name of an account.</span></span>
<span data-ttu-id="f4381-116">Om du anger ett konto namn returneras bara det kontot i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4381-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4381-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4381-117">-DefaultProfile</span></span>
<span data-ttu-id="f4381-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4381-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4381-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4381-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4381-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f4381-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f4381-121">Om du anger en resurs grupp får denna cmdlet konton under den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4381-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4381-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f4381-122">-Tag</span></span>
<span data-ttu-id="f4381-123">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f4381-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4381-124">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="f4381-124">For example:</span></span>

<span data-ttu-id="f4381-125">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f4381-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="f4381-126">Denna cmdlet hämtar konton som innehåller de taggar som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f4381-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4381-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4381-127">CommonParameters</span></span>
<span data-ttu-id="f4381-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4381-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4381-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4381-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4381-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4381-130">INPUTS</span></span>

### <span data-ttu-id="f4381-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="f4381-131">None</span></span>
<span data-ttu-id="f4381-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f4381-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4381-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4381-133">OUTPUTS</span></span>

### <span data-ttu-id="f4381-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4381-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f4381-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4381-135">NOTES</span></span>

## <span data-ttu-id="f4381-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4381-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4381-137">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f4381-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="f4381-138">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f4381-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="f4381-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f4381-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="f4381-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f4381-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
