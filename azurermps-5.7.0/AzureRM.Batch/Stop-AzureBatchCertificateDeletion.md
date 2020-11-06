---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 51fca07847ca5bf0c73a5f2c88a41d3de166053c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574412"
---
# <span data-ttu-id="ad309-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="ad309-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="ad309-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad309-102">SYNOPSIS</span></span>
<span data-ttu-id="ad309-103">Avbryter en misslyckad borttagning av ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="ad309-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad309-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad309-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad309-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad309-105">DESCRIPTION</span></span>
<span data-ttu-id="ad309-106">Cmdleten **Stop-AzureBatchCertificateDeletion** avbryter en misslyckad borttagning av ett certifikat i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ad309-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="ad309-107">Du kan bara stoppa en borttagning om certifikatet är i **DeleteFailed** -tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ad309-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="ad309-108">Denna cmldet återställer certifikatet till det **aktiva** läget.</span><span class="sxs-lookup"><span data-stu-id="ad309-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="ad309-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad309-109">EXAMPLES</span></span>

### <span data-ttu-id="ad309-110">Exempel 1: Avbryt en borttagning</span><span class="sxs-lookup"><span data-stu-id="ad309-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="ad309-111">Det här kommandot avbryter borttagningen av certifikatet som har angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="ad309-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="ad309-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad309-112">PARAMETERS</span></span>

### <span data-ttu-id="ad309-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad309-113">-BatchContext</span></span>
<span data-ttu-id="ad309-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ad309-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad309-115">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ad309-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ad309-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ad309-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ad309-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ad309-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ad309-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ad309-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad309-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad309-119">-DefaultProfile</span></span>
<span data-ttu-id="ad309-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad309-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad309-121">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ad309-121">-Thumbprint</span></span>
<span data-ttu-id="ad309-122">Anger tumavtrycket för det certifikat som denna cmdlet återställer till det **aktiva** tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ad309-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad309-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ad309-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ad309-124">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="ad309-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ad309-125">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="ad309-125">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad309-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad309-126">CommonParameters</span></span>
<span data-ttu-id="ad309-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad309-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad309-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad309-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad309-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad309-129">INPUTS</span></span>

### <span data-ttu-id="ad309-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad309-130">BatchAccountContext</span></span>
<span data-ttu-id="ad309-131">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ad309-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ad309-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad309-132">OUTPUTS</span></span>

## <span data-ttu-id="ad309-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad309-133">NOTES</span></span>

## <span data-ttu-id="ad309-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad309-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad309-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad309-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ad309-136">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ad309-136">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="ad309-137">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ad309-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


