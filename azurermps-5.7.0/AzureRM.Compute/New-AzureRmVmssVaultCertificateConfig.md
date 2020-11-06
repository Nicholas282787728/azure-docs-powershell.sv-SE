---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579612"
---
# <span data-ttu-id="ea277-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="ea277-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="ea277-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea277-102">SYNOPSIS</span></span>
<span data-ttu-id="ea277-103">Skapar en konfiguration för ett nyckelord för valv.</span><span class="sxs-lookup"><span data-stu-id="ea277-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea277-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea277-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea277-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea277-105">DESCRIPTION</span></span>
<span data-ttu-id="ea277-106">Cmdleten **New-AzureRmVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ea277-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="ea277-107">Utdata från denna cmdlet är avsedda att användas med Add-AzureRmVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea277-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="ea277-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea277-108">EXAMPLES</span></span>

### <span data-ttu-id="ea277-109">Exempel 1: skapa en konfiguration för ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="ea277-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="ea277-110">Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.</span><span class="sxs-lookup"><span data-stu-id="ea277-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="ea277-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea277-111">PARAMETERS</span></span>

### <span data-ttu-id="ea277-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="ea277-112">-CertificateStore</span></span>
<span data-ttu-id="ea277-113">Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="ea277-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="ea277-114">Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ea277-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea277-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ea277-115">-CertificateUrl</span></span>
<span data-ttu-id="ea277-116">Anger URI för ett certifikat som är lagrat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ea277-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="ea277-117">Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8:</span><span class="sxs-lookup"><span data-stu-id="ea277-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="ea277-118">{"data": " \<Base64-encoded-certificate\> ", "datatyp": "PFX", "lösen ord": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="ea277-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea277-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea277-119">-Confirm</span></span>
<span data-ttu-id="ea277-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea277-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea277-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea277-121">-WhatIf</span></span>
<span data-ttu-id="ea277-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea277-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea277-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea277-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea277-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea277-124">CommonParameters</span></span>
<span data-ttu-id="ea277-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea277-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea277-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea277-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea277-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea277-127">INPUTS</span></span>

### <span data-ttu-id="ea277-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="ea277-128">None</span></span>
<span data-ttu-id="ea277-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ea277-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea277-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea277-130">OUTPUTS</span></span>

###  
<span data-ttu-id="ea277-131">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ea277-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ea277-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea277-132">NOTES</span></span>

## <span data-ttu-id="ea277-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea277-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea277-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ea277-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
