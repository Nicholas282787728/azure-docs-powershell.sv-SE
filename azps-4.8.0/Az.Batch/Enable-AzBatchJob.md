---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103072"
---
# <span data-ttu-id="c55d3-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="c55d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c55d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c55d3-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c55d3-103">Enables a Batch job.</span></span>

## <span data-ttu-id="c55d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c55d3-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c55d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c55d3-105">DESCRIPTION</span></span>
<span data-ttu-id="c55d3-106">Cmdleten **Enable-AzBatchJob** aktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c55d3-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="c55d3-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="c55d3-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="c55d3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c55d3-108">EXAMPLES</span></span>

### <span data-ttu-id="c55d3-109">Exempel 1: aktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="c55d3-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="c55d3-110">Det här kommandot aktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="c55d3-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c55d3-111">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="c55d3-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c55d3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c55d3-112">PARAMETERS</span></span>

### <span data-ttu-id="c55d3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c55d3-113">-BatchContext</span></span>
<span data-ttu-id="c55d3-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c55d3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c55d3-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c55d3-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c55d3-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c55d3-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c55d3-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c55d3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c55d3-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c55d3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55d3-119">-DefaultProfile</span></span>
<span data-ttu-id="c55d3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c55d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c55d3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c55d3-121">-Id</span></span>
<span data-ttu-id="c55d3-122">Anger ID för det jobb som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="c55d3-122">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55d3-123">CommonParameters</span></span>
<span data-ttu-id="c55d3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55d3-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c55d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55d3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c55d3-126">INPUTS</span></span>

### <span data-ttu-id="c55d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c55d3-127">System.String</span></span>

### <span data-ttu-id="c55d3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c55d3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c55d3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c55d3-129">OUTPUTS</span></span>

### <span data-ttu-id="c55d3-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="c55d3-130">System.Void</span></span>

## <span data-ttu-id="c55d3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c55d3-131">NOTES</span></span>

## <span data-ttu-id="c55d3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c55d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="c55d3-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="c55d3-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="c55d3-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="c55d3-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="c55d3-137">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c55d3-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="c55d3-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c55d3-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
