---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928261"
---
# <span data-ttu-id="35537-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="35537-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="35537-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35537-102">SYNOPSIS</span></span>
<span data-ttu-id="35537-103">Skapar en konfiguration för ett nyckelord för valv.</span><span class="sxs-lookup"><span data-stu-id="35537-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="35537-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35537-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35537-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35537-105">DESCRIPTION</span></span>
<span data-ttu-id="35537-106">Cmdleten **New-AzVmssVaultCertificateConfig** anger den hemlighet som måste placeras på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="35537-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="35537-107">Utdata från denna cmdlet är avsedda att användas med Add-AzVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35537-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="35537-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35537-108">EXAMPLES</span></span>

### <span data-ttu-id="35537-109">Exempel 1: skapa en konfiguration för ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="35537-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="35537-110">Det här kommandot skapar en konfiguration för ett valv certifikat som använder certifikat arkivet som heter mina certifikat på den angivna certifikat-URL: en.</span><span class="sxs-lookup"><span data-stu-id="35537-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="35537-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35537-111">PARAMETERS</span></span>

### <span data-ttu-id="35537-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="35537-112">-CertificateStore</span></span>
<span data-ttu-id="35537-113">Anger certifikat arkivet på de virtuella datorerna i den skal uppsättning där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="35537-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="35537-114">Det här gäller endast för skalnings uppsättningar i Windows virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="35537-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="35537-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="35537-115">-CertificateUrl</span></span>
<span data-ttu-id="35537-116">Anger URI för ett certifikat som är lagrat i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="35537-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="35537-117">Det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8: {"data": " \< Base64-kodat \> ", "datatyp": "PFX", "lösen ord": " \< PFX-File-Password \> "}</span><span class="sxs-lookup"><span data-stu-id="35537-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="35537-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35537-118">-DefaultProfile</span></span>
<span data-ttu-id="35537-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35537-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35537-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35537-120">-Confirm</span></span>
<span data-ttu-id="35537-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35537-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35537-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35537-122">-WhatIf</span></span>
<span data-ttu-id="35537-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35537-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35537-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35537-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35537-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35537-125">CommonParameters</span></span>
<span data-ttu-id="35537-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35537-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35537-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35537-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35537-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35537-128">INPUTS</span></span>

### <span data-ttu-id="35537-129">System. String</span><span class="sxs-lookup"><span data-stu-id="35537-129">System.String</span></span>

## <span data-ttu-id="35537-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35537-130">OUTPUTS</span></span>

### <span data-ttu-id="35537-131">Microsoft. Azure. Management. Compute. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="35537-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="35537-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35537-132">NOTES</span></span>

## <span data-ttu-id="35537-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35537-133">RELATED LINKS</span></span>

[<span data-ttu-id="35537-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="35537-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
