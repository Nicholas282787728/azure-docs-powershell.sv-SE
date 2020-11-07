---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755135"
---
# <span data-ttu-id="6efc2-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="6efc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6efc2-102">SYNOPSIS</span></span>
<span data-ttu-id="6efc2-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="6efc2-103">Enables a Batch job.</span></span>

## <span data-ttu-id="6efc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6efc2-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6efc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6efc2-105">DESCRIPTION</span></span>
<span data-ttu-id="6efc2-106">Cmdleten **Enable-AzBatchJob** aktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="6efc2-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="6efc2-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="6efc2-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="6efc2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6efc2-108">EXAMPLES</span></span>

### <span data-ttu-id="6efc2-109">Exempel 1: aktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="6efc2-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="6efc2-110">Det här kommandot aktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="6efc2-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6efc2-111">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="6efc2-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6efc2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6efc2-112">PARAMETERS</span></span>

### <span data-ttu-id="6efc2-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6efc2-113">-BatchContext</span></span>
<span data-ttu-id="6efc2-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6efc2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6efc2-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6efc2-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6efc2-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="6efc2-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6efc2-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="6efc2-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6efc2-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6efc2-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6efc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efc2-119">-DefaultProfile</span></span>
<span data-ttu-id="6efc2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6efc2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6efc2-121">-ID</span><span class="sxs-lookup"><span data-stu-id="6efc2-121">-Id</span></span>
<span data-ttu-id="6efc2-122">Anger ID för det jobb som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="6efc2-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="6efc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efc2-123">CommonParameters</span></span>
<span data-ttu-id="6efc2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efc2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efc2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efc2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6efc2-126">INPUTS</span></span>

### <span data-ttu-id="6efc2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6efc2-127">System.String</span></span>

### <span data-ttu-id="6efc2-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6efc2-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6efc2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6efc2-129">OUTPUTS</span></span>

### <span data-ttu-id="6efc2-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="6efc2-130">System.Void</span></span>

## <span data-ttu-id="6efc2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6efc2-131">NOTES</span></span>

## <span data-ttu-id="6efc2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6efc2-132">RELATED LINKS</span></span>

[<span data-ttu-id="6efc2-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="6efc2-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6efc2-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="6efc2-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="6efc2-137">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6efc2-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="6efc2-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6efc2-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


