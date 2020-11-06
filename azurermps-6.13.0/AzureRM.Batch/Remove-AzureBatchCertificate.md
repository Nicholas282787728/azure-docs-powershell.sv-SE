---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579007"
---
# <span data-ttu-id="c1190-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c1190-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="c1190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1190-102">SYNOPSIS</span></span>
<span data-ttu-id="c1190-103">Tar bort ett certifikat från ett konto.</span><span class="sxs-lookup"><span data-stu-id="c1190-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1190-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1190-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1190-105">DESCRIPTION</span></span>
<span data-ttu-id="c1190-106">Cmdleten **Remove-AzureBatchCertificate** tar bort ett certifikat från det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="c1190-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="c1190-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1190-107">EXAMPLES</span></span>

### <span data-ttu-id="c1190-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c1190-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="c1190-109">Det här kommandot tar bort certifikatet med angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="c1190-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="c1190-110">Exempel 2: ta bort alla aktiva certifikat</span><span class="sxs-lookup"><span data-stu-id="c1190-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="c1190-111">Det här kommandot får alla certifikat som är aktiva med hjälp av Get-AzureBatchCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1190-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="c1190-112">Kommandot skickar de aktiva certifikaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c1190-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c1190-113">Varje certifikat tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1190-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="c1190-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="c1190-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c1190-115">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c1190-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c1190-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1190-116">PARAMETERS</span></span>

### <span data-ttu-id="c1190-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c1190-117">-BatchContext</span></span>
<span data-ttu-id="c1190-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1190-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c1190-119">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1190-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c1190-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c1190-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c1190-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c1190-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c1190-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c1190-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c1190-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1190-123">-DefaultProfile</span></span>
<span data-ttu-id="c1190-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1190-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1190-125">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c1190-125">-Thumbprint</span></span>
<span data-ttu-id="c1190-126">Anger tumavtrycket för det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c1190-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c1190-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c1190-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c1190-128">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="c1190-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="c1190-129">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="c1190-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="c1190-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1190-130">-Confirm</span></span>
<span data-ttu-id="c1190-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1190-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1190-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1190-132">-WhatIf</span></span>
<span data-ttu-id="c1190-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1190-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1190-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1190-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1190-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1190-135">CommonParameters</span></span>
<span data-ttu-id="c1190-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1190-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1190-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1190-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1190-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1190-138">INPUTS</span></span>

### <span data-ttu-id="c1190-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c1190-139">System.String</span></span>

### <span data-ttu-id="c1190-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1190-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c1190-141">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1190-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c1190-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1190-142">OUTPUTS</span></span>

### <span data-ttu-id="c1190-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="c1190-143">System.Void</span></span>

## <span data-ttu-id="c1190-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1190-144">NOTES</span></span>

## <span data-ttu-id="c1190-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1190-145">RELATED LINKS</span></span>

[<span data-ttu-id="c1190-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c1190-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="c1190-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c1190-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c1190-148">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c1190-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="c1190-149">Stopp-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="c1190-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="c1190-150">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c1190-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


