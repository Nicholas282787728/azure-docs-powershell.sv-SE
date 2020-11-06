---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579779"
---
# <span data-ttu-id="f09e3-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="f09e3-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="f09e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f09e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f09e3-103">Avbryter en misslyckad borttagning av ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="f09e3-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f09e3-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f09e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f09e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f09e3-106">Cmdleten **Stop-AzureBatchCertificateDeletion** avbryter en misslyckad borttagning av ett certifikat i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f09e3-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="f09e3-107">Du kan bara stoppa en borttagning om certifikatet är i **DeleteFailed** -tillståndet.</span><span class="sxs-lookup"><span data-stu-id="f09e3-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="f09e3-108">Denna cmldet återställer certifikatet till det **aktiva** läget.</span><span class="sxs-lookup"><span data-stu-id="f09e3-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="f09e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f09e3-109">EXAMPLES</span></span>

### <span data-ttu-id="f09e3-110">Exempel 1: Avbryt en borttagning</span><span class="sxs-lookup"><span data-stu-id="f09e3-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="f09e3-111">Det här kommandot avbryter borttagningen av certifikatet som har angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="f09e3-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="f09e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f09e3-112">PARAMETERS</span></span>

### <span data-ttu-id="f09e3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f09e3-113">-BatchContext</span></span>
<span data-ttu-id="f09e3-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f09e3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f09e3-115">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f09e3-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f09e3-116">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="f09e3-116">-Thumbprint</span></span>
<span data-ttu-id="f09e3-117">Anger tumavtrycket för det certifikat som denna cmdlet återställer till det **aktiva** tillståndet.</span><span class="sxs-lookup"><span data-stu-id="f09e3-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="f09e3-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f09e3-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f09e3-119">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="f09e3-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="f09e3-120">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="f09e3-120">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09e3-121">-DefaultProfile</span></span>
<span data-ttu-id="f09e3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f09e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f09e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09e3-123">CommonParameters</span></span>
<span data-ttu-id="f09e3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09e3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09e3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f09e3-126">INPUTS</span></span>

### <span data-ttu-id="f09e3-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f09e3-127">BatchAccountContext</span></span>
<span data-ttu-id="f09e3-128">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f09e3-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f09e3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f09e3-129">OUTPUTS</span></span>

## <span data-ttu-id="f09e3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f09e3-130">NOTES</span></span>

## <span data-ttu-id="f09e3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f09e3-131">RELATED LINKS</span></span>

[<span data-ttu-id="f09e3-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f09e3-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f09e3-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f09e3-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="f09e3-134">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f09e3-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


