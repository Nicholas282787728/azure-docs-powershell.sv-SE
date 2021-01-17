---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411488"
---
# <span data-ttu-id="e53b8-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e53b8-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="e53b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e53b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e53b8-103">Tar bort ett certifikat från ett konto.</span><span class="sxs-lookup"><span data-stu-id="e53b8-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="e53b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e53b8-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e53b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e53b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e53b8-106">Cmdleten **Remove-AzBatchCertificate** tar bort ett certifikat från det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="e53b8-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="e53b8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e53b8-107">EXAMPLES</span></span>

### <span data-ttu-id="e53b8-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="e53b8-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="e53b8-109">Det här kommandot tar bort certifikatet med angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="e53b8-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="e53b8-110">Exempel 2: ta bort alla aktiva certifikat</span><span class="sxs-lookup"><span data-stu-id="e53b8-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="e53b8-111">Det här kommandot får alla certifikat som är aktiva med hjälp av Get-AzBatchCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53b8-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="e53b8-112">Kommandot skickar de aktiva certifikaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e53b8-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e53b8-113">Varje certifikat tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53b8-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="e53b8-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="e53b8-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e53b8-115">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e53b8-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e53b8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e53b8-116">PARAMETERS</span></span>

### <span data-ttu-id="e53b8-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e53b8-117">-BatchContext</span></span>
<span data-ttu-id="e53b8-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e53b8-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e53b8-119">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e53b8-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e53b8-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e53b8-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e53b8-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e53b8-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e53b8-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e53b8-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e53b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53b8-123">-DefaultProfile</span></span>
<span data-ttu-id="e53b8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e53b8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e53b8-125">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="e53b8-125">-Thumbprint</span></span>
<span data-ttu-id="e53b8-126">Anger tumavtrycket för det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e53b8-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e53b8-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e53b8-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e53b8-128">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="e53b8-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e53b8-129">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="e53b8-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e53b8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e53b8-130">-Confirm</span></span>
<span data-ttu-id="e53b8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e53b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53b8-132">-WhatIf</span></span>
<span data-ttu-id="e53b8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e53b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53b8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e53b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53b8-135">CommonParameters</span></span>
<span data-ttu-id="e53b8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53b8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e53b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53b8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e53b8-138">INPUTS</span></span>

### <span data-ttu-id="e53b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e53b8-139">System.String</span></span>

### <span data-ttu-id="e53b8-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e53b8-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e53b8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e53b8-141">OUTPUTS</span></span>

### <span data-ttu-id="e53b8-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="e53b8-142">System.Void</span></span>

## <span data-ttu-id="e53b8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e53b8-143">NOTES</span></span>

## <span data-ttu-id="e53b8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e53b8-144">RELATED LINKS</span></span>

[<span data-ttu-id="e53b8-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e53b8-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="e53b8-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e53b8-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e53b8-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e53b8-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="e53b8-148">Stopp-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="e53b8-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="e53b8-149">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e53b8-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
