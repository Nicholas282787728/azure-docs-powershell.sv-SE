---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584668"
---
# <span data-ttu-id="35a5d-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="35a5d-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="35a5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="35a5d-103">Återställer ett borttaget certifikat i ett nyckeltal till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="35a5d-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35a5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35a5d-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="35a5d-106">Med cmdleten **Undo-AzureKeyVaultCertificateRemoval** återställs ett tidigare borttaget certifikat.</span><span class="sxs-lookup"><span data-stu-id="35a5d-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="35a5d-107">Det återställda certifikatet kommer att vara aktivt och kan användas för alla åtgärder.</span><span class="sxs-lookup"><span data-stu-id="35a5d-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="35a5d-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="35a5d-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="35a5d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35a5d-109">EXAMPLES</span></span>

### <span data-ttu-id="35a5d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35a5d-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="35a5d-111">Det här kommandot återställer certifikatet "Mina certifikat" som tidigare tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="35a5d-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="35a5d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35a5d-112">PARAMETERS</span></span>

### <span data-ttu-id="35a5d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="35a5d-113">-Name</span></span>
<span data-ttu-id="35a5d-114">Certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="35a5d-114">Certificate name.</span></span>
<span data-ttu-id="35a5d-115">Cmdlet konstruerar FQDN för ett certifikat från valv namnet, för närvarande valda miljö-och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="35a5d-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35a5d-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="35a5d-116">-VaultName</span></span>
<span data-ttu-id="35a5d-117">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="35a5d-117">Vault name.</span></span>
<span data-ttu-id="35a5d-118">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="35a5d-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35a5d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35a5d-119">-Confirm</span></span>
<span data-ttu-id="35a5d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35a5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a5d-121">-WhatIf</span></span>
<span data-ttu-id="35a5d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35a5d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a5d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35a5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a5d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a5d-124">-DefaultProfile</span></span>
<span data-ttu-id="35a5d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35a5d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35a5d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a5d-126">CommonParameters</span></span>
<span data-ttu-id="35a5d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a5d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a5d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a5d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a5d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35a5d-129">INPUTS</span></span>

### <span data-ttu-id="35a5d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="35a5d-130">System.String</span></span>

## <span data-ttu-id="35a5d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35a5d-131">OUTPUTS</span></span>

### <span data-ttu-id="35a5d-132">Microsoft. Azure. commands. Vault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="35a5d-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="35a5d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35a5d-133">NOTES</span></span>

## <span data-ttu-id="35a5d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35a5d-134">RELATED LINKS</span></span>

[<span data-ttu-id="35a5d-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="35a5d-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="35a5d-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="35a5d-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
