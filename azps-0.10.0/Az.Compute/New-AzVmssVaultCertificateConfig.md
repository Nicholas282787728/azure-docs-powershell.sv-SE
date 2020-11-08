---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925022"
---
# <span data-ttu-id="479da-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="479da-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="479da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="479da-102">SYNOPSIS</span></span>
<span data-ttu-id="479da-103">Skapar en konfiguration för ett nyckelord för valv.</span><span class="sxs-lookup"><span data-stu-id="479da-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="479da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="479da-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="479da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="479da-105">DESCRIPTION</span></span>
<span data-ttu-id="479da-106">Cmdleten **New-AzVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="479da-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="479da-107">Utdata från denna cmdlet är avsedda att användas med Add-AzVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="479da-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="479da-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="479da-108">EXAMPLES</span></span>

### <span data-ttu-id="479da-109">Exempel 1: skapa en konfiguration för ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="479da-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="479da-110">Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.</span><span class="sxs-lookup"><span data-stu-id="479da-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="479da-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="479da-111">PARAMETERS</span></span>

### <span data-ttu-id="479da-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="479da-112">-CertificateStore</span></span>
<span data-ttu-id="479da-113">Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="479da-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="479da-114">Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="479da-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="479da-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="479da-115">-CertificateUrl</span></span>
<span data-ttu-id="479da-116">Anger URI för ett certifikat som är lagrat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="479da-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="479da-117">Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8:</span><span class="sxs-lookup"><span data-stu-id="479da-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="479da-118">{"data": " \< Base64-kodat-certifikat \> "," datatyp ":" PFX "," lösen ord ":" \< PFX-File-Password \> "}</span><span class="sxs-lookup"><span data-stu-id="479da-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="479da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479da-119">-DefaultProfile</span></span>
<span data-ttu-id="479da-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="479da-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="479da-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="479da-121">-Confirm</span></span>
<span data-ttu-id="479da-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="479da-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="479da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479da-123">-WhatIf</span></span>
<span data-ttu-id="479da-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="479da-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="479da-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="479da-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="479da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479da-126">CommonParameters</span></span>
<span data-ttu-id="479da-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479da-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479da-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479da-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="479da-129">INPUTS</span></span>

### <span data-ttu-id="479da-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="479da-130">None</span></span>
<span data-ttu-id="479da-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="479da-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="479da-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="479da-132">OUTPUTS</span></span>

###  
<span data-ttu-id="479da-133">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="479da-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="479da-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="479da-134">NOTES</span></span>

## <span data-ttu-id="479da-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="479da-135">RELATED LINKS</span></span>

[<span data-ttu-id="479da-136">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="479da-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)