---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269651"
---
# <span data-ttu-id="4b069-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b069-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="4b069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b069-102">SYNOPSIS</span></span>
<span data-ttu-id="4b069-103">Lägger till ett certifikat till det angivna batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="4b069-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="4b069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b069-104">SYNTAX</span></span>

### <span data-ttu-id="4b069-105">Fil (standard)</span><span class="sxs-lookup"><span data-stu-id="4b069-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b069-106">RawData</span><span class="sxs-lookup"><span data-stu-id="4b069-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b069-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b069-107">DESCRIPTION</span></span>
<span data-ttu-id="4b069-108">Cmdleten **New-AzBatchCertificate** lägger till ett certifikat till det angivna Azure Batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="4b069-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="4b069-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b069-109">EXAMPLES</span></span>

### <span data-ttu-id="4b069-110">Exempel 1: lägga till ett certifikat från en fil</span><span class="sxs-lookup"><span data-stu-id="4b069-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="4b069-111">Det här kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av filen E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="4b069-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="4b069-112">Exempel 2: lägga till ett certifikat från rå data</span><span class="sxs-lookup"><span data-stu-id="4b069-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="4b069-113">Det första kommandot läser in data från filen med namnet "cert. pfx" i $RawData variabel.</span><span class="sxs-lookup"><span data-stu-id="4b069-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="4b069-114">Det andra kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av rå data som lagras i $RawData.</span><span class="sxs-lookup"><span data-stu-id="4b069-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="4b069-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b069-115">PARAMETERS</span></span>

### <span data-ttu-id="4b069-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4b069-116">-BatchContext</span></span>
<span data-ttu-id="4b069-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b069-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4b069-118">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b069-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4b069-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="4b069-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4b069-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="4b069-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4b069-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4b069-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4b069-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b069-122">-DefaultProfile</span></span>
<span data-ttu-id="4b069-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b069-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b069-124">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="4b069-124">-FilePath</span></span>
<span data-ttu-id="4b069-125">Anger sökvägen till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="4b069-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="4b069-126">Certifikat filen måste vara i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="4b069-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="4b069-127">-Sort</span><span class="sxs-lookup"><span data-stu-id="4b069-127">-Kind</span></span>
<span data-ttu-id="4b069-128">Den typ av certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4b069-128">The kind of certificate to create.</span></span> <span data-ttu-id="4b069-129">Om det inte anges antas det att alla certifikat utan lösen ord är CER och att alla certifikat med lösen ord är PFX.</span><span class="sxs-lookup"><span data-stu-id="4b069-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b069-130">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="4b069-130">-Password</span></span>
<span data-ttu-id="4b069-131">Anger lösen ordet för att komma åt certifikatets privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="4b069-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="4b069-132">Du måste ange den här parametern om du anger ett certifikat i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="4b069-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b069-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="4b069-133">-RawData</span></span>
<span data-ttu-id="4b069-134">Anger rå data för certifikat i. cer-eller. PFX-format.</span><span class="sxs-lookup"><span data-stu-id="4b069-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="4b069-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b069-135">CommonParameters</span></span>
<span data-ttu-id="4b069-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b069-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b069-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b069-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b069-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b069-138">INPUTS</span></span>

### <span data-ttu-id="4b069-139">System. byte []</span><span class="sxs-lookup"><span data-stu-id="4b069-139">System.Byte[]</span></span>

### <span data-ttu-id="4b069-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4b069-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4b069-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b069-141">OUTPUTS</span></span>

### <span data-ttu-id="4b069-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="4b069-142">System.Void</span></span>

## <span data-ttu-id="4b069-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b069-143">NOTES</span></span>

## <span data-ttu-id="4b069-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b069-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b069-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b069-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="4b069-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4b069-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4b069-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b069-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="4b069-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4b069-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)