---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: e55bad94b002e6dc606f39ae3e75258207646b5f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928330"
---
# <span data-ttu-id="e1543-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="e1543-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="e1543-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1543-102">SYNOPSIS</span></span>
<span data-ttu-id="e1543-103">Avbryter en misslyckad borttagning av ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="e1543-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="e1543-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1543-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1543-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1543-105">DESCRIPTION</span></span>
<span data-ttu-id="e1543-106">Cmdleten **Stop-AzBatchCertificateDeletion** avbryter en misslyckad borttagning av ett certifikat i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e1543-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="e1543-107">Du kan bara stoppa en borttagning om certifikatet är i **DeleteFailed** -tillståndet.</span><span class="sxs-lookup"><span data-stu-id="e1543-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="e1543-108">Denna cmldet återställer certifikatet till det **aktiva** läget.</span><span class="sxs-lookup"><span data-stu-id="e1543-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="e1543-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1543-109">EXAMPLES</span></span>

### <span data-ttu-id="e1543-110">Exempel 1: Avbryt en borttagning</span><span class="sxs-lookup"><span data-stu-id="e1543-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="e1543-111">Det här kommandot avbryter borttagningen av certifikatet som har angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="e1543-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="e1543-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1543-112">PARAMETERS</span></span>

### <span data-ttu-id="e1543-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e1543-113">-BatchContext</span></span>
<span data-ttu-id="e1543-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e1543-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e1543-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e1543-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e1543-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e1543-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e1543-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e1543-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e1543-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e1543-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e1543-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1543-119">-DefaultProfile</span></span>
<span data-ttu-id="e1543-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1543-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1543-121">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="e1543-121">-Thumbprint</span></span>
<span data-ttu-id="e1543-122">Anger tumavtrycket för det certifikat som denna cmdlet återställer till det **aktiva** tillståndet.</span><span class="sxs-lookup"><span data-stu-id="e1543-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="e1543-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e1543-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e1543-124">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="e1543-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e1543-125">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="e1543-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e1543-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1543-126">CommonParameters</span></span>
<span data-ttu-id="e1543-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1543-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1543-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1543-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1543-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1543-129">INPUTS</span></span>

### <span data-ttu-id="e1543-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e1543-130">System.String</span></span>

### <span data-ttu-id="e1543-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e1543-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e1543-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1543-132">OUTPUTS</span></span>

### <span data-ttu-id="e1543-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="e1543-133">System.Void</span></span>

## <span data-ttu-id="e1543-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1543-134">NOTES</span></span>

## <span data-ttu-id="e1543-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1543-135">RELATED LINKS</span></span>

[<span data-ttu-id="e1543-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e1543-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e1543-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e1543-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="e1543-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e1543-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


