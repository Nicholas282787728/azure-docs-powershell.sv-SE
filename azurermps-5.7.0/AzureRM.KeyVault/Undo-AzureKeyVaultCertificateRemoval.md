---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757678"
---
# <span data-ttu-id="90ef5-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="90ef5-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="90ef5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="90ef5-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="90ef5-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90ef5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90ef5-104">SYNTAX</span></span>

### <span data-ttu-id="90ef5-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="90ef5-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ef5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="90ef5-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ef5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90ef5-107">DESCRIPTION</span></span>
<span data-ttu-id="90ef5-108">Med cmdleten **Undo-AzureKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="90ef5-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="90ef5-109">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="90ef5-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="90ef5-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="90ef5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="90ef5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90ef5-111">EXAMPLES</span></span>

### <span data-ttu-id="90ef5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90ef5-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="90ef5-113">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="90ef5-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="90ef5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90ef5-114">PARAMETERS</span></span>

### <span data-ttu-id="90ef5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ef5-115">-DefaultProfile</span></span>
<span data-ttu-id="90ef5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="90ef5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90ef5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ef5-117">-InputObject</span></span>
<span data-ttu-id="90ef5-118">Borttaget certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="90ef5-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ef5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="90ef5-119">-Name</span></span>
<span data-ttu-id="90ef5-120">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="90ef5-120">Certificate name.</span></span>
<span data-ttu-id="90ef5-121">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="90ef5-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ef5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="90ef5-122">-VaultName</span></span>
<span data-ttu-id="90ef5-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="90ef5-123">Vault name.</span></span>
<span data-ttu-id="90ef5-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="90ef5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ef5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90ef5-125">-Confirm</span></span>
<span data-ttu-id="90ef5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90ef5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ef5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ef5-127">-WhatIf</span></span>
<span data-ttu-id="90ef5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90ef5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ef5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90ef5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ef5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ef5-130">CommonParameters</span></span>
<span data-ttu-id="90ef5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ef5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ef5-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ef5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ef5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90ef5-133">INPUTS</span></span>

### <span data-ttu-id="90ef5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="90ef5-134">System.String</span></span>

## <span data-ttu-id="90ef5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90ef5-135">OUTPUTS</span></span>

### <span data-ttu-id="90ef5-136">Microsoft. Azure. commands. valv. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="90ef5-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="90ef5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90ef5-137">NOTES</span></span>

## <span data-ttu-id="90ef5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90ef5-138">RELATED LINKS</span></span>

[<span data-ttu-id="90ef5-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90ef5-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="90ef5-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="90ef5-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
