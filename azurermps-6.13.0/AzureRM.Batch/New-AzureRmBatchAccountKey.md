---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582804"
---
# <span data-ttu-id="ec7f4-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ec7f4-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="ec7f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7f4-103">Återskapar en Key för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec7f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec7f4-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec7f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ec7f4-106">**New-AzureRmBatchAccountKey** cmdlet återskapar den primära eller sekundära nyckeln för ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="ec7f4-107">Cmdleten returnerar ett **BatchAccountContext** -objekt som har dess aktuella **PrimaryAccountKey** -och **SecondaryAccountKey** -egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="ec7f4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec7f4-108">EXAMPLES</span></span>

### <span data-ttu-id="ec7f4-109">Exempel 1: återskapa primär konto nyckeln på ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="ec7f4-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="ec7f4-110">Det här kommandot återskapar den primära konto nyckeln för batch-kontot som heter pfuller.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="ec7f4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec7f4-111">PARAMETERS</span></span>

### <span data-ttu-id="ec7f4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec7f4-112">-AccountName</span></span>
<span data-ttu-id="ec7f4-113">Anger namnet på det kommando konto som denna cmdlet återskapar en nyckeln för.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ec7f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7f4-114">-DefaultProfile</span></span>
<span data-ttu-id="ec7f4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec7f4-116">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="ec7f4-116">-KeyType</span></span>
<span data-ttu-id="ec7f4-117">Anger den typ av nycklar som denna cmdlet återskapar.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="ec7f4-118">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="ec7f4-118">Valid values are:</span></span> 
- <span data-ttu-id="ec7f4-119">Första</span><span class="sxs-lookup"><span data-stu-id="ec7f4-119">Primary</span></span>
- <span data-ttu-id="ec7f4-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="ec7f4-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec7f4-122">Anger resurs gruppen för det konto som denna cmdlet återskapar en nyckeln för.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ec7f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7f4-123">CommonParameters</span></span>
<span data-ttu-id="ec7f4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec7f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7f4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7f4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec7f4-126">INPUTS</span></span>

### <span data-ttu-id="ec7f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ec7f4-127">System.String</span></span>

## <span data-ttu-id="ec7f4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec7f4-128">OUTPUTS</span></span>

### <span data-ttu-id="ec7f4-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec7f4-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ec7f4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec7f4-130">NOTES</span></span>

## <span data-ttu-id="ec7f4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec7f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec7f4-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ec7f4-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ec7f4-133">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ec7f4-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


