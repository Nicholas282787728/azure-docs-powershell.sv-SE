---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583672"
---
# <span data-ttu-id="2492d-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2492d-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="2492d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2492d-102">SYNOPSIS</span></span>
<span data-ttu-id="2492d-103">Tar bort ett certifikat från ett konto.</span><span class="sxs-lookup"><span data-stu-id="2492d-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2492d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2492d-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2492d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2492d-105">DESCRIPTION</span></span>
<span data-ttu-id="2492d-106">Cmdleten **Remove-AzureBatchCertificate** tar bort ett certifikat från det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="2492d-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="2492d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2492d-107">EXAMPLES</span></span>

### <span data-ttu-id="2492d-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="2492d-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="2492d-109">Det här kommandot tar bort certifikatet med angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="2492d-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="2492d-110">Exempel 2: ta bort alla aktiva certifikat</span><span class="sxs-lookup"><span data-stu-id="2492d-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="2492d-111">Det här kommandot får alla certifikat som är aktiva med hjälp av Get-AzureBatchCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2492d-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="2492d-112">Kommandot skickar de aktiva certifikaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2492d-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2492d-113">Varje certifikat tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2492d-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="2492d-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="2492d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2492d-115">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2492d-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2492d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2492d-116">PARAMETERS</span></span>

### <span data-ttu-id="2492d-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2492d-117">-BatchContext</span></span>
<span data-ttu-id="2492d-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2492d-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2492d-119">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2492d-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2492d-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="2492d-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2492d-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="2492d-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2492d-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2492d-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2492d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2492d-123">-DefaultProfile</span></span>
<span data-ttu-id="2492d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2492d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2492d-125">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="2492d-125">-Thumbprint</span></span>
<span data-ttu-id="2492d-126">Anger tumavtrycket för det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2492d-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2492d-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2492d-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="2492d-128">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="2492d-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="2492d-129">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="2492d-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="2492d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2492d-130">-Confirm</span></span>
<span data-ttu-id="2492d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2492d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2492d-132">-WhatIf</span></span>
<span data-ttu-id="2492d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2492d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2492d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2492d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2492d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2492d-135">CommonParameters</span></span>
<span data-ttu-id="2492d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2492d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2492d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2492d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2492d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2492d-138">INPUTS</span></span>

### <span data-ttu-id="2492d-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2492d-139">BatchAccountContext</span></span>
<span data-ttu-id="2492d-140">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2492d-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="2492d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2492d-141">OUTPUTS</span></span>

## <span data-ttu-id="2492d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2492d-142">NOTES</span></span>

## <span data-ttu-id="2492d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2492d-143">RELATED LINKS</span></span>

[<span data-ttu-id="2492d-144">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2492d-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="2492d-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2492d-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2492d-146">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2492d-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="2492d-147">Stopp-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="2492d-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="2492d-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2492d-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


