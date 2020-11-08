---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: ff8404b3a437d27b84501ba56bc79daa09a9b8f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916210"
---
# <span data-ttu-id="f1e99-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="f1e99-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="f1e99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1e99-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e99-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f1e99-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="f1e99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1e99-104">SYNTAX</span></span>

### <span data-ttu-id="f1e99-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="f1e99-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e99-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e99-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e99-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1e99-107">DESCRIPTION</span></span>
<span data-ttu-id="f1e99-108">Med cmdleten **Undo-AzKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="f1e99-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="f1e99-109">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f1e99-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="f1e99-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f1e99-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f1e99-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1e99-111">EXAMPLES</span></span>

### <span data-ttu-id="f1e99-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1e99-112">Example 1</span></span>
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

<span data-ttu-id="f1e99-113">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f1e99-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f1e99-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1e99-114">PARAMETERS</span></span>

### <span data-ttu-id="f1e99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e99-115">-DefaultProfile</span></span>
<span data-ttu-id="f1e99-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f1e99-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e99-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e99-117">-InputObject</span></span>
<span data-ttu-id="f1e99-118">Borttaget certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="f1e99-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="f1e99-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1e99-119">-Name</span></span>
<span data-ttu-id="f1e99-120">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="f1e99-120">Certificate name.</span></span>
<span data-ttu-id="f1e99-121">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="f1e99-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="f1e99-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1e99-122">-VaultName</span></span>
<span data-ttu-id="f1e99-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="f1e99-123">Vault name.</span></span>
<span data-ttu-id="f1e99-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="f1e99-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f1e99-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1e99-125">-Confirm</span></span>
<span data-ttu-id="f1e99-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1e99-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e99-127">-WhatIf</span></span>
<span data-ttu-id="f1e99-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1e99-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e99-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1e99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e99-130">CommonParameters</span></span>
<span data-ttu-id="f1e99-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e99-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e99-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e99-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1e99-133">INPUTS</span></span>

### <span data-ttu-id="f1e99-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f1e99-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="f1e99-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1e99-135">OUTPUTS</span></span>

### <span data-ttu-id="f1e99-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1e99-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="f1e99-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1e99-137">NOTES</span></span>

## <span data-ttu-id="f1e99-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1e99-138">RELATED LINKS</span></span>

[<span data-ttu-id="f1e99-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1e99-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="f1e99-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1e99-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)