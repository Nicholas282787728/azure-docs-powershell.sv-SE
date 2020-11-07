---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758296"
---
# <span data-ttu-id="3a2a1-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2a1-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="3a2a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a2a1-103">Lägger till ett certifikat till det angivna batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a2a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a2a1-104">SYNTAX</span></span>

### <span data-ttu-id="3a2a1-105">Fil (standard)</span><span class="sxs-lookup"><span data-stu-id="3a2a1-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a2a1-106">RawData</span><span class="sxs-lookup"><span data-stu-id="3a2a1-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a2a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a2a1-107">DESCRIPTION</span></span>
<span data-ttu-id="3a2a1-108">Cmdleten **New-AzureBatchCertificate** lägger till ett certifikat till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="3a2a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a2a1-109">EXAMPLES</span></span>

### <span data-ttu-id="3a2a1-110">Exempel 1: lägga till ett certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="3a2a1-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="3a2a1-111">Det här kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av filen E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="3a2a1-112">Exempel 2: lägga till ett certifikat från rå data</span><span class="sxs-lookup"><span data-stu-id="3a2a1-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="3a2a1-113">Det första kommandot läser in data från filen med namnet "cert. pfx" i $RawData variabel.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="3a2a1-114">Det andra kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av rå data som lagras i $RawData.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="3a2a1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a2a1-115">PARAMETERS</span></span>

### <span data-ttu-id="3a2a1-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3a2a1-116">-BatchContext</span></span>
<span data-ttu-id="3a2a1-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3a2a1-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3a2a1-119">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="3a2a1-119">-FilePath</span></span>
<span data-ttu-id="3a2a1-120">Anger sökvägen till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="3a2a1-121">Certifikat filen måste vara i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-121">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2a1-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="3a2a1-122">-Password</span></span>
<span data-ttu-id="3a2a1-123">Anger lösen ordet för att komma åt certifikatets privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="3a2a1-124">Du måste ange den här parametern om du anger ett certifikat i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a2a1-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="3a2a1-125">-RawData</span></span>
<span data-ttu-id="3a2a1-126">Anger rå data för certifikat i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a2a1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a2a1-127">-DefaultProfile</span></span>
<span data-ttu-id="3a2a1-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a2a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a2a1-129">CommonParameters</span></span>
<span data-ttu-id="3a2a1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a2a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a2a1-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a2a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a2a1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a2a1-132">INPUTS</span></span>

### <span data-ttu-id="3a2a1-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3a2a1-133">BatchAccountContext</span></span>
<span data-ttu-id="3a2a1-134">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3a2a1-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3a2a1-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="3a2a1-135">Byte[]</span></span>
<span data-ttu-id="3a2a1-136">Parametern ' RawData ' godkänner värdet av typen ' byte [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3a2a1-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="3a2a1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a2a1-137">OUTPUTS</span></span>

## <span data-ttu-id="3a2a1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a2a1-138">NOTES</span></span>

## <span data-ttu-id="3a2a1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a2a1-139">RELATED LINKS</span></span>

[<span data-ttu-id="3a2a1-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2a1-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="3a2a1-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3a2a1-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3a2a1-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2a1-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="3a2a1-143">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="3a2a1-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


