---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584991"
---
# <span data-ttu-id="4ade2-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="4ade2-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="4ade2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ade2-102">SYNOPSIS</span></span>
<span data-ttu-id="4ade2-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="4ade2-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ade2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ade2-104">SYNTAX</span></span>

### <span data-ttu-id="4ade2-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="4ade2-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ade2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ade2-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ade2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ade2-107">DESCRIPTION</span></span>
<span data-ttu-id="4ade2-108">Med cmdleten **Undo-AzureKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="4ade2-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="4ade2-109">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="4ade2-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="4ade2-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4ade2-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4ade2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ade2-111">EXAMPLES</span></span>

### <span data-ttu-id="4ade2-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ade2-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="4ade2-113">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="4ade2-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4ade2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ade2-114">PARAMETERS</span></span>

### <span data-ttu-id="4ade2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ade2-115">-DefaultProfile</span></span>
<span data-ttu-id="4ade2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ade2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ade2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ade2-117">-InputObject</span></span>
<span data-ttu-id="4ade2-118">Borttaget certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="4ade2-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="4ade2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ade2-119">-Name</span></span>
<span data-ttu-id="4ade2-120">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="4ade2-120">Certificate name.</span></span>
<span data-ttu-id="4ade2-121">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="4ade2-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="4ade2-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ade2-122">-VaultName</span></span>
<span data-ttu-id="4ade2-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="4ade2-123">Vault name.</span></span>
<span data-ttu-id="4ade2-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="4ade2-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4ade2-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ade2-125">-Confirm</span></span>
<span data-ttu-id="4ade2-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ade2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ade2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ade2-127">-WhatIf</span></span>
<span data-ttu-id="4ade2-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ade2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ade2-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ade2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ade2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ade2-130">CommonParameters</span></span>
<span data-ttu-id="4ade2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ade2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ade2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ade2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ade2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ade2-133">INPUTS</span></span>

### <span data-ttu-id="4ade2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4ade2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="4ade2-135">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ade2-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4ade2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ade2-136">OUTPUTS</span></span>

### <span data-ttu-id="4ade2-137">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4ade2-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="4ade2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ade2-138">NOTES</span></span>

## <span data-ttu-id="4ade2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ade2-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ade2-140">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4ade2-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4ade2-141">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4ade2-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
