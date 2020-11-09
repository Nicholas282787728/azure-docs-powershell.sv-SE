---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323970"
---
# <span data-ttu-id="258bc-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="258bc-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="258bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="258bc-102">SYNOPSIS</span></span>
<span data-ttu-id="258bc-103">Avbryter en misslyckad borttagning av ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="258bc-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="258bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="258bc-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="258bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="258bc-105">DESCRIPTION</span></span>
<span data-ttu-id="258bc-106">Cmdleten **Stop-AzBatchCertificateDeletion** avbryter en misslyckad borttagning av ett certifikat i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="258bc-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="258bc-107">Du kan bara stoppa en borttagning om certifikatet är i **DeleteFailed** -tillståndet.</span><span class="sxs-lookup"><span data-stu-id="258bc-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="258bc-108">Denna cmdlet återställer certifikatet till det **aktiva** tillståndet.</span><span class="sxs-lookup"><span data-stu-id="258bc-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="258bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="258bc-109">EXAMPLES</span></span>

### <span data-ttu-id="258bc-110">Exempel 1: Avbryt en borttagning</span><span class="sxs-lookup"><span data-stu-id="258bc-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="258bc-111">Det här kommandot avbryter borttagningen av certifikatet som har angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="258bc-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="258bc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="258bc-112">PARAMETERS</span></span>

### <span data-ttu-id="258bc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="258bc-113">-BatchContext</span></span>
<span data-ttu-id="258bc-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="258bc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="258bc-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="258bc-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="258bc-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="258bc-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="258bc-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="258bc-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="258bc-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="258bc-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="258bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258bc-119">-DefaultProfile</span></span>
<span data-ttu-id="258bc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="258bc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="258bc-121">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="258bc-121">-Thumbprint</span></span>
<span data-ttu-id="258bc-122">Anger tumavtrycket för det certifikat som denna cmdlet återställer till det **aktiva** tillståndet.</span><span class="sxs-lookup"><span data-stu-id="258bc-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="258bc-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="258bc-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="258bc-124">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="258bc-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="258bc-125">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="258bc-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="258bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258bc-126">CommonParameters</span></span>
<span data-ttu-id="258bc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258bc-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="258bc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258bc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="258bc-129">INPUTS</span></span>

### <span data-ttu-id="258bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="258bc-130">System.String</span></span>

### <span data-ttu-id="258bc-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="258bc-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="258bc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="258bc-132">OUTPUTS</span></span>

### <span data-ttu-id="258bc-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="258bc-133">System.Void</span></span>

## <span data-ttu-id="258bc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="258bc-134">NOTES</span></span>

## <span data-ttu-id="258bc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="258bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="258bc-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="258bc-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="258bc-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="258bc-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="258bc-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="258bc-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
