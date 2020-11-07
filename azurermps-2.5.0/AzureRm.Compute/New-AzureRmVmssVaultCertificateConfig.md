---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930685"
---
# <span data-ttu-id="01276-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="01276-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="01276-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01276-102">SYNOPSIS</span></span>
<span data-ttu-id="01276-103">Skapar en konfiguration för ett nyckelord för valv.</span><span class="sxs-lookup"><span data-stu-id="01276-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01276-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01276-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01276-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01276-105">DESCRIPTION</span></span>
<span data-ttu-id="01276-106">Cmdleten **New-AzureRmVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="01276-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="01276-107">Utdata från denna cmdlet är avsedda att användas med Add-AzureRmVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01276-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="01276-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01276-108">EXAMPLES</span></span>

### <span data-ttu-id="01276-109">Exempel 1: skapa en konfiguration för ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="01276-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="01276-110">Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.</span><span class="sxs-lookup"><span data-stu-id="01276-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="01276-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01276-111">PARAMETERS</span></span>

### <span data-ttu-id="01276-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="01276-112">-CertificateStore</span></span>
<span data-ttu-id="01276-113">Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="01276-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="01276-114">Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01276-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="01276-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="01276-115">-CertificateUrl</span></span>
<span data-ttu-id="01276-116">Anger URI för ett certifikat som är lagrat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="01276-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="01276-117">Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8:</span><span class="sxs-lookup"><span data-stu-id="01276-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="01276-118">{"data": " \<Base64-encoded-certificate\> ", "datatyp": "PFX", "lösen ord": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="01276-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="01276-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01276-119">-DefaultProfile</span></span>
<span data-ttu-id="01276-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01276-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01276-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01276-121">-Confirm</span></span>
<span data-ttu-id="01276-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01276-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01276-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01276-123">-WhatIf</span></span>
<span data-ttu-id="01276-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01276-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01276-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01276-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01276-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01276-126">CommonParameters</span></span>
<span data-ttu-id="01276-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01276-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01276-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01276-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01276-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01276-129">INPUTS</span></span>

### <span data-ttu-id="01276-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="01276-130">None</span></span>
<span data-ttu-id="01276-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="01276-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01276-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01276-132">OUTPUTS</span></span>

###  
<span data-ttu-id="01276-133">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="01276-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="01276-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01276-134">NOTES</span></span>

## <span data-ttu-id="01276-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01276-135">RELATED LINKS</span></span>

[<span data-ttu-id="01276-136">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="01276-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
