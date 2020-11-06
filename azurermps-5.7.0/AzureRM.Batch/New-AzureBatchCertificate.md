---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586123"
---
# <span data-ttu-id="e6117-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e6117-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="e6117-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6117-102">SYNOPSIS</span></span>
<span data-ttu-id="e6117-103">Lägger till ett certifikat till det angivna batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="e6117-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6117-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6117-104">SYNTAX</span></span>

### <span data-ttu-id="e6117-105">Fil (standard)</span><span class="sxs-lookup"><span data-stu-id="e6117-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6117-106">RawData</span><span class="sxs-lookup"><span data-stu-id="e6117-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6117-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6117-107">DESCRIPTION</span></span>
<span data-ttu-id="e6117-108">Cmdleten **New-AzureBatchCertificate** lägger till ett certifikat till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="e6117-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="e6117-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6117-109">EXAMPLES</span></span>

### <span data-ttu-id="e6117-110">Exempel 1: lägga till ett certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="e6117-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="e6117-111">Det här kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av filen E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="e6117-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="e6117-112">Exempel 2: lägga till ett certifikat från rå data</span><span class="sxs-lookup"><span data-stu-id="e6117-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="e6117-113">Det första kommandot läser in data från filen med namnet "cert. pfx" i $RawData variabel.</span><span class="sxs-lookup"><span data-stu-id="e6117-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="e6117-114">Det andra kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av rå data som lagras i $RawData.</span><span class="sxs-lookup"><span data-stu-id="e6117-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="e6117-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6117-115">PARAMETERS</span></span>

### <span data-ttu-id="e6117-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e6117-116">-BatchContext</span></span>
<span data-ttu-id="e6117-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e6117-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e6117-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e6117-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e6117-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e6117-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e6117-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e6117-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e6117-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e6117-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e6117-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6117-122">-DefaultProfile</span></span>
<span data-ttu-id="e6117-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6117-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6117-124">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="e6117-124">-FilePath</span></span>
<span data-ttu-id="e6117-125">Anger sökvägen till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="e6117-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="e6117-126">Certifikat filen måste vara i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="e6117-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6117-127">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="e6117-127">-Password</span></span>
<span data-ttu-id="e6117-128">Anger lösen ordet för att komma åt certifikatets privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="e6117-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="e6117-129">Du måste ange den här parametern om du anger ett certifikat i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="e6117-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6117-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="e6117-130">-RawData</span></span>
<span data-ttu-id="e6117-131">Anger rå data för certifikat i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="e6117-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6117-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6117-132">CommonParameters</span></span>
<span data-ttu-id="e6117-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6117-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6117-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6117-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6117-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6117-135">INPUTS</span></span>

### <span data-ttu-id="e6117-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e6117-136">BatchAccountContext</span></span>
<span data-ttu-id="e6117-137">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e6117-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e6117-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="e6117-138">Byte[]</span></span>
<span data-ttu-id="e6117-139">Parametern ' RawData ' godkänner värdet av typen ' byte [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e6117-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="e6117-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6117-140">OUTPUTS</span></span>

## <span data-ttu-id="e6117-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6117-141">NOTES</span></span>

## <span data-ttu-id="e6117-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6117-142">RELATED LINKS</span></span>

[<span data-ttu-id="e6117-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e6117-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="e6117-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6117-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e6117-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e6117-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="e6117-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e6117-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


