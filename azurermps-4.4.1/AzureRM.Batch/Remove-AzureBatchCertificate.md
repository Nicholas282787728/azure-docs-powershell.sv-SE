---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575013"
---
# <span data-ttu-id="02537-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="02537-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="02537-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02537-102">SYNOPSIS</span></span>
<span data-ttu-id="02537-103">Tar bort ett certifikat från ett konto.</span><span class="sxs-lookup"><span data-stu-id="02537-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02537-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02537-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02537-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02537-105">DESCRIPTION</span></span>
<span data-ttu-id="02537-106">Cmdleten **Remove-AzureBatchCertificate** tar bort ett certifikat från det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="02537-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="02537-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02537-107">EXAMPLES</span></span>

### <span data-ttu-id="02537-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="02537-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="02537-109">Det här kommandot tar bort certifikatet med angivet tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="02537-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="02537-110">Exempel 2: ta bort alla aktiva certifikat</span><span class="sxs-lookup"><span data-stu-id="02537-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="02537-111">Det här kommandot får alla certifikat som är aktiva med hjälp av Get-AzureBatchCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02537-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="02537-112">Kommandot skickar de aktiva certifikaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="02537-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02537-113">Varje certifikat tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02537-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="02537-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="02537-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="02537-115">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="02537-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="02537-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02537-116">PARAMETERS</span></span>

### <span data-ttu-id="02537-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02537-117">-BatchContext</span></span>
<span data-ttu-id="02537-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="02537-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02537-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="02537-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="02537-120">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="02537-120">-Thumbprint</span></span>
<span data-ttu-id="02537-121">Anger tumavtrycket för det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="02537-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="02537-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="02537-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="02537-123">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="02537-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="02537-124">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="02537-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="02537-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02537-125">-Confirm</span></span>
<span data-ttu-id="02537-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02537-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02537-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02537-127">-WhatIf</span></span>
<span data-ttu-id="02537-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02537-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02537-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02537-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02537-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02537-130">-DefaultProfile</span></span>
<span data-ttu-id="02537-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02537-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02537-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02537-132">CommonParameters</span></span>
<span data-ttu-id="02537-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02537-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02537-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02537-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02537-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02537-135">INPUTS</span></span>

### <span data-ttu-id="02537-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02537-136">BatchAccountContext</span></span>
<span data-ttu-id="02537-137">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="02537-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="02537-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02537-138">OUTPUTS</span></span>

## <span data-ttu-id="02537-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02537-139">NOTES</span></span>

## <span data-ttu-id="02537-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02537-140">RELATED LINKS</span></span>

[<span data-ttu-id="02537-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="02537-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="02537-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="02537-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="02537-143">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="02537-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="02537-144">Stopp-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="02537-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="02537-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="02537-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


