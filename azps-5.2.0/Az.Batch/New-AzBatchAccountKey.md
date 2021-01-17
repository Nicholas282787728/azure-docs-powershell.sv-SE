---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405547"
---
# <span data-ttu-id="f39fa-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f39fa-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="f39fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f39fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f39fa-103">Återskapar en Key för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="f39fa-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="f39fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f39fa-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f39fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f39fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f39fa-106">**New-AzBatchAccountKey** cmdlet återskapar den primära eller sekundära nyckeln för ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="f39fa-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="f39fa-107">Cmdleten returnerar ett **BatchAccountContext** -objekt som har dess aktuella **PrimaryAccountKey** -och **SecondaryAccountKey** -egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f39fa-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="f39fa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f39fa-108">EXAMPLES</span></span>

### <span data-ttu-id="f39fa-109">Exempel 1: återskapa primär konto nyckeln på ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="f39fa-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="f39fa-110">Det här kommandot återskapar den primära konto nyckeln för batch-kontot som heter pfuller.</span><span class="sxs-lookup"><span data-stu-id="f39fa-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="f39fa-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f39fa-111">PARAMETERS</span></span>

### <span data-ttu-id="f39fa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f39fa-112">-AccountName</span></span>
<span data-ttu-id="f39fa-113">Anger namnet på det kommando konto som denna cmdlet återskapar en nyckeln för.</span><span class="sxs-lookup"><span data-stu-id="f39fa-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="f39fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39fa-114">-DefaultProfile</span></span>
<span data-ttu-id="f39fa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f39fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39fa-116">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="f39fa-116">-KeyType</span></span>
<span data-ttu-id="f39fa-117">Anger den typ av nycklar som denna cmdlet återskapar.</span><span class="sxs-lookup"><span data-stu-id="f39fa-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="f39fa-118">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f39fa-118">Valid values are:</span></span>
- <span data-ttu-id="f39fa-119">Första</span><span class="sxs-lookup"><span data-stu-id="f39fa-119">Primary</span></span>
- <span data-ttu-id="f39fa-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="f39fa-120">Secondary</span></span>

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

### <span data-ttu-id="f39fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="f39fa-122">Anger resurs gruppen för det konto som denna cmdlet återskapar en nyckeln för.</span><span class="sxs-lookup"><span data-stu-id="f39fa-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="f39fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39fa-123">CommonParameters</span></span>
<span data-ttu-id="f39fa-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39fa-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f39fa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39fa-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f39fa-126">INPUTS</span></span>

### <span data-ttu-id="f39fa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f39fa-127">System.String</span></span>

## <span data-ttu-id="f39fa-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f39fa-128">OUTPUTS</span></span>

### <span data-ttu-id="f39fa-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f39fa-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f39fa-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f39fa-130">NOTES</span></span>

## <span data-ttu-id="f39fa-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f39fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="f39fa-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f39fa-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f39fa-133">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f39fa-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
