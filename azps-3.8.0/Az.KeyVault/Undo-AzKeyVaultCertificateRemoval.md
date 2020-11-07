---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926630"
---
# <span data-ttu-id="0f44e-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="0f44e-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="0f44e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f44e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f44e-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="0f44e-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="0f44e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f44e-104">SYNTAX</span></span>

### <span data-ttu-id="0f44e-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="0f44e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f44e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0f44e-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f44e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f44e-107">DESCRIPTION</span></span>
<span data-ttu-id="0f44e-108">Med cmdleten **Undo-AzKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="0f44e-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="0f44e-109">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="0f44e-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="0f44e-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0f44e-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="0f44e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f44e-111">EXAMPLES</span></span>

### <span data-ttu-id="0f44e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f44e-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="0f44e-113">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="0f44e-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="0f44e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f44e-114">PARAMETERS</span></span>

### <span data-ttu-id="0f44e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f44e-115">-DefaultProfile</span></span>
<span data-ttu-id="0f44e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0f44e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f44e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f44e-117">-InputObject</span></span>
<span data-ttu-id="0f44e-118">Borttaget certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="0f44e-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f44e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f44e-119">-Name</span></span>
<span data-ttu-id="0f44e-120">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="0f44e-120">Certificate name.</span></span>
<span data-ttu-id="0f44e-121">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="0f44e-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f44e-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f44e-122">-VaultName</span></span>
<span data-ttu-id="0f44e-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="0f44e-123">Vault name.</span></span>
<span data-ttu-id="0f44e-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="0f44e-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f44e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f44e-125">-Confirm</span></span>
<span data-ttu-id="0f44e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f44e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f44e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f44e-127">-WhatIf</span></span>
<span data-ttu-id="0f44e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f44e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f44e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f44e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f44e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f44e-130">CommonParameters</span></span>
<span data-ttu-id="0f44e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f44e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f44e-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f44e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f44e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f44e-133">INPUTS</span></span>

### <span data-ttu-id="0f44e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f44e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0f44e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f44e-135">OUTPUTS</span></span>

### <span data-ttu-id="0f44e-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f44e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="0f44e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f44e-137">NOTES</span></span>

## <span data-ttu-id="0f44e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f44e-138">RELATED LINKS</span></span>

[<span data-ttu-id="0f44e-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f44e-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="0f44e-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0f44e-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
