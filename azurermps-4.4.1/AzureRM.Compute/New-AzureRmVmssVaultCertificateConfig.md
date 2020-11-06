---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584788"
---
# <span data-ttu-id="522ba-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="522ba-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="522ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="522ba-102">SYNOPSIS</span></span>
<span data-ttu-id="522ba-103">Skapar en konfiguration för ett nyckelord för valv.</span><span class="sxs-lookup"><span data-stu-id="522ba-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="522ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="522ba-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="522ba-105">DESCRIPTION</span></span>
<span data-ttu-id="522ba-106">Cmdleten **New-AzureRmVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="522ba-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="522ba-107">Utdata från denna cmdlet är avsedda att användas med Add-AzureRmVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="522ba-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="522ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="522ba-108">EXAMPLES</span></span>

### <span data-ttu-id="522ba-109">Exempel 1: skapa en konfiguration för ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="522ba-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="522ba-110">Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.</span><span class="sxs-lookup"><span data-stu-id="522ba-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="522ba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="522ba-111">PARAMETERS</span></span>

### <span data-ttu-id="522ba-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="522ba-112">-CertificateStore</span></span>
<span data-ttu-id="522ba-113">Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="522ba-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="522ba-114">Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="522ba-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ba-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="522ba-115">-CertificateUrl</span></span>
<span data-ttu-id="522ba-116">Anger URI för ett certifikat som är lagrat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="522ba-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="522ba-117">Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8:</span><span class="sxs-lookup"><span data-stu-id="522ba-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="522ba-118">{"data": " \<Base64-encoded-certificate\> ", "datatyp": "PFX", "lösen ord": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="522ba-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522ba-119">-DefaultProfile</span></span>
<span data-ttu-id="522ba-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="522ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="522ba-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="522ba-121">-Confirm</span></span>
<span data-ttu-id="522ba-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="522ba-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522ba-123">-WhatIf</span></span>
<span data-ttu-id="522ba-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="522ba-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="522ba-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="522ba-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522ba-126">CommonParameters</span></span>
<span data-ttu-id="522ba-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522ba-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522ba-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="522ba-129">INPUTS</span></span>

## <span data-ttu-id="522ba-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="522ba-130">OUTPUTS</span></span>

###  
<span data-ttu-id="522ba-131">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="522ba-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="522ba-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="522ba-132">NOTES</span></span>

## <span data-ttu-id="522ba-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="522ba-133">RELATED LINKS</span></span>

[<span data-ttu-id="522ba-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="522ba-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
