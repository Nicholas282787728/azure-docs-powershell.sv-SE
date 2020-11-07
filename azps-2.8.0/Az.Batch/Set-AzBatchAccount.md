---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 0a19ede4a990b10244204d8f633ed747adb7d30e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928558"
---
# <span data-ttu-id="097bb-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="097bb-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="097bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="097bb-102">SYNOPSIS</span></span>
<span data-ttu-id="097bb-103">Uppdaterar ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="097bb-103">Updates a Batch account.</span></span>

## <span data-ttu-id="097bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="097bb-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="097bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="097bb-105">DESCRIPTION</span></span>
<span data-ttu-id="097bb-106">Cmdleten **set-AzBatchAccount** uppdaterar ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="097bb-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="097bb-107">För närvarande kan denna cmdlet endast uppdatera taggar.</span><span class="sxs-lookup"><span data-stu-id="097bb-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="097bb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="097bb-108">EXAMPLES</span></span>

### <span data-ttu-id="097bb-109">Exempel 1: uppdatera taggarna för ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="097bb-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="097bb-110">Det här kommandot uppdaterar taggarna för kontot med namnet pfuller.</span><span class="sxs-lookup"><span data-stu-id="097bb-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="097bb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="097bb-111">PARAMETERS</span></span>

### <span data-ttu-id="097bb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="097bb-112">-AccountName</span></span>
<span data-ttu-id="097bb-113">Anger namnet på batch-kontot som uppdateras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="097bb-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="097bb-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="097bb-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="097bb-115">Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="097bb-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="097bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097bb-116">-DefaultProfile</span></span>
<span data-ttu-id="097bb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="097bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="097bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="097bb-119">Anger resurs gruppen för det konto som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="097bb-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="097bb-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="097bb-120">-Tag</span></span>
<span data-ttu-id="097bb-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="097bb-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="097bb-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="097bb-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097bb-123">CommonParameters</span></span>
<span data-ttu-id="097bb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="097bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097bb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="097bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097bb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="097bb-126">INPUTS</span></span>

### <span data-ttu-id="097bb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="097bb-127">System.String</span></span>

### <span data-ttu-id="097bb-128">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="097bb-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="097bb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="097bb-129">OUTPUTS</span></span>

### <span data-ttu-id="097bb-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="097bb-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="097bb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="097bb-131">NOTES</span></span>

## <span data-ttu-id="097bb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="097bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="097bb-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="097bb-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="097bb-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="097bb-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="097bb-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="097bb-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="097bb-136">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="097bb-136">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
