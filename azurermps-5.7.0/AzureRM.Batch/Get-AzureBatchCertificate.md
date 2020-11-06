---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
ms.openlocfilehash: d33d18c5025a5374849c9ef5770968b4e34b9930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579651"
---
# <span data-ttu-id="4039e-101">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4039e-101">Get-AzureBatchCertificate</span></span>

## <span data-ttu-id="4039e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4039e-102">SYNOPSIS</span></span>
<span data-ttu-id="4039e-103">Hämtar certifikaten i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4039e-103">Gets the certificates in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4039e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4039e-104">SYNTAX</span></span>

### <span data-ttu-id="4039e-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="4039e-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4039e-106">#C1</span><span class="sxs-lookup"><span data-stu-id="4039e-106">Thumbprint</span></span>
```
Get-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4039e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4039e-107">DESCRIPTION</span></span>
<span data-ttu-id="4039e-108">Cmdleten **Get-AzureBatchCertificate** hämtar certifikaten i Azure Batch-kontot som parametern *BatchContext* anger.</span><span class="sxs-lookup"><span data-stu-id="4039e-108">The **Get-AzureBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="4039e-109">Om du vill skaffa ett visst certifikat anger du parametrarna för *ThumbprintAlgorithm* och *tumavtryck* .</span><span class="sxs-lookup"><span data-stu-id="4039e-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="4039e-110">Ange parametern *filter* för att hämta de certifikat som matchar ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4039e-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="4039e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4039e-111">EXAMPLES</span></span>

### <span data-ttu-id="4039e-112">Exempel 1: Hämta ett certifikat via tumavtryck</span><span class="sxs-lookup"><span data-stu-id="4039e-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzureBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="4039e-113">Det här kommandot får ett enskilt certifikat som har det angivna tumavtrycket.</span><span class="sxs-lookup"><span data-stu-id="4039e-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="4039e-114">Tumavtrycket för tumavtryck är SHA1.</span><span class="sxs-lookup"><span data-stu-id="4039e-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="4039e-115">Exempel 2: hämta filtrerade certifikat</span><span class="sxs-lookup"><span data-stu-id="4039e-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="4039e-116">Det här kommandot får alla certifikat i tillståndet aktiv från batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="4039e-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="4039e-117">Parametern *filter* anger tillståndet.</span><span class="sxs-lookup"><span data-stu-id="4039e-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="4039e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4039e-118">PARAMETERS</span></span>

### <span data-ttu-id="4039e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4039e-119">-BatchContext</span></span>
<span data-ttu-id="4039e-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4039e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4039e-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4039e-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4039e-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="4039e-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4039e-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="4039e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4039e-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4039e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4039e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4039e-125">-DefaultProfile</span></span>
<span data-ttu-id="4039e-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4039e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4039e-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="4039e-127">-Filter</span></span>
<span data-ttu-id="4039e-128">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="4039e-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="4039e-129">Om du anger den här parametern får denna cmdlet de certifikat som matchar filtret.</span><span class="sxs-lookup"><span data-stu-id="4039e-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039e-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4039e-130">-MaxCount</span></span>
<span data-ttu-id="4039e-131">Anger det högsta antalet certifikat som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="4039e-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="4039e-132">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4039e-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="4039e-133">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="4039e-133">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039e-134">-Välj</span><span class="sxs-lookup"><span data-stu-id="4039e-134">-Select</span></span>
<span data-ttu-id="4039e-135">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="4039e-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="4039e-136">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4039e-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039e-137">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="4039e-137">-Thumbprint</span></span>
<span data-ttu-id="4039e-138">Anger tumavtrycket för det certifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="4039e-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4039e-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4039e-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4039e-140">Anger den algoritm som används för att härleda *tumavtrycket* .</span><span class="sxs-lookup"><span data-stu-id="4039e-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="4039e-141">För närvarande är det enda giltiga värdet SHA1.</span><span class="sxs-lookup"><span data-stu-id="4039e-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4039e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4039e-142">CommonParameters</span></span>
<span data-ttu-id="4039e-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4039e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4039e-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4039e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4039e-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4039e-145">INPUTS</span></span>

### <span data-ttu-id="4039e-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4039e-146">BatchAccountContext</span></span>
<span data-ttu-id="4039e-147">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4039e-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4039e-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4039e-148">OUTPUTS</span></span>

### <span data-ttu-id="4039e-149">Microsoft.Azure.Commands.BatCH. Modeller. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="4039e-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="4039e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4039e-150">NOTES</span></span>

## <span data-ttu-id="4039e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4039e-151">RELATED LINKS</span></span>

[<span data-ttu-id="4039e-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4039e-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4039e-153">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4039e-153">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="4039e-154">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4039e-154">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="4039e-155">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4039e-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


