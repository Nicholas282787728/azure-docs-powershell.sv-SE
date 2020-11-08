---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: c4b2ec7bc04664b1b73e3a2d830f56132a8f4b05
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100413"
---
# <span data-ttu-id="dd525-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="dd525-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="dd525-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd525-102">SYNOPSIS</span></span>
<span data-ttu-id="dd525-103">Hämtar ett batchjobb för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dd525-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="dd525-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd525-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd525-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd525-105">DESCRIPTION</span></span>
<span data-ttu-id="dd525-106">Cmdleten **Get-AzBatchAccount** får ett Azure Batch-konto i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dd525-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="dd525-107">Du kan använda parametern *AccountName* för att få ett enskilt konto, eller så kan du använda parametern *ResourceGroupName* för att hämta konton under den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dd525-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="dd525-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd525-108">EXAMPLES</span></span>

### <span data-ttu-id="dd525-109">Exempel 1: Hämta ett batch-konto efter namn</span><span class="sxs-lookup"><span data-stu-id="dd525-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="dd525-110">Det här kommandot får batch-kontot pfuller.</span><span class="sxs-lookup"><span data-stu-id="dd525-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="dd525-111">Exempel 2: Hämta de grupp konton som är kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dd525-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="dd525-112">Det här kommandot hämtar de konton som är kopplade till resurs gruppen CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="dd525-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="dd525-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd525-113">PARAMETERS</span></span>

### <span data-ttu-id="dd525-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd525-114">-AccountName</span></span>
<span data-ttu-id="dd525-115">Anger namnet på ett konto.</span><span class="sxs-lookup"><span data-stu-id="dd525-115">Specifies the name of an account.</span></span>
<span data-ttu-id="dd525-116">Om du anger ett konto namn returneras bara det kontot i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd525-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="dd525-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd525-117">-DefaultProfile</span></span>
<span data-ttu-id="dd525-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd525-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd525-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd525-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd525-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dd525-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dd525-121">Om du anger en resurs grupp får denna cmdlet konton under den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dd525-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="dd525-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dd525-122">-Tag</span></span>
<span data-ttu-id="dd525-123">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dd525-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dd525-124">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} med den här cmdleten får du konton som innehåller taggarna som anges.</span><span class="sxs-lookup"><span data-stu-id="dd525-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd525-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd525-125">CommonParameters</span></span>
<span data-ttu-id="dd525-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd525-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd525-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd525-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd525-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd525-128">INPUTS</span></span>

### <span data-ttu-id="dd525-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dd525-129">System.String</span></span>

### <span data-ttu-id="dd525-130">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="dd525-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd525-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd525-131">OUTPUTS</span></span>

### <span data-ttu-id="dd525-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dd525-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dd525-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd525-133">NOTES</span></span>

## <span data-ttu-id="dd525-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd525-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd525-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="dd525-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="dd525-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="dd525-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="dd525-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="dd525-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="dd525-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="dd525-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
