---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929869"
---
# <span data-ttu-id="30921-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="30921-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="30921-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30921-102">SYNOPSIS</span></span>
<span data-ttu-id="30921-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="30921-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30921-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30921-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30921-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30921-105">DESCRIPTION</span></span>
<span data-ttu-id="30921-106">Med cmdleten **Undo-AzureKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="30921-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="30921-107">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="30921-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="30921-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="30921-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="30921-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30921-109">EXAMPLES</span></span>

### <span data-ttu-id="30921-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30921-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="30921-111">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="30921-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="30921-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30921-112">PARAMETERS</span></span>

### <span data-ttu-id="30921-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30921-113">-DefaultProfile</span></span>
<span data-ttu-id="30921-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="30921-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30921-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="30921-115">-Name</span></span>
<span data-ttu-id="30921-116">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="30921-116">Certificate name.</span></span>
<span data-ttu-id="30921-117">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="30921-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30921-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30921-118">-VaultName</span></span>
<span data-ttu-id="30921-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="30921-119">Vault name.</span></span>
<span data-ttu-id="30921-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="30921-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30921-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30921-121">-Confirm</span></span>
<span data-ttu-id="30921-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30921-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30921-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30921-123">-WhatIf</span></span>
<span data-ttu-id="30921-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30921-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30921-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30921-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30921-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30921-126">CommonParameters</span></span>
<span data-ttu-id="30921-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30921-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30921-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30921-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30921-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30921-129">INPUTS</span></span>

### <span data-ttu-id="30921-130">System. String</span><span class="sxs-lookup"><span data-stu-id="30921-130">System.String</span></span>

## <span data-ttu-id="30921-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30921-131">OUTPUTS</span></span>

### <span data-ttu-id="30921-132">Microsoft. Azure. commands. Vault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="30921-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="30921-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30921-133">NOTES</span></span>

## <span data-ttu-id="30921-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30921-134">RELATED LINKS</span></span>

[<span data-ttu-id="30921-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="30921-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="30921-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="30921-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
