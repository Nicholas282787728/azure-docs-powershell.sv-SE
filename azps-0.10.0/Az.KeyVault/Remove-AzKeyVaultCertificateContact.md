---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922697"
---
# <span data-ttu-id="5b285-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5b285-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5b285-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b285-102">SYNOPSIS</span></span>
<span data-ttu-id="5b285-103">Tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="5b285-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="5b285-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b285-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b285-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b285-105">DESCRIPTION</span></span>
<span data-ttu-id="5b285-106">Cmdleten **Remove-AzKeyVaultCertificateContact** tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="5b285-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="5b285-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b285-107">EXAMPLES</span></span>

### <span data-ttu-id="5b285-108">Exempel 1: ta bort en certifikat kontakt</span><span class="sxs-lookup"><span data-stu-id="5b285-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="5b285-109">Det här kommandot tar bort Patti Nilsson som en certifikat kontakt för Contoso01-.</span><span class="sxs-lookup"><span data-stu-id="5b285-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="5b285-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b285-110">PARAMETERS</span></span>

### <span data-ttu-id="5b285-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b285-111">-DefaultProfile</span></span>
<span data-ttu-id="5b285-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5b285-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b285-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5b285-113">-EmailAddress</span></span>
<span data-ttu-id="5b285-114">Anger e-postadressen till den kontakt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5b285-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b285-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b285-115">-PassThru</span></span>
<span data-ttu-id="5b285-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5b285-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b285-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5b285-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b285-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5b285-118">-VaultName</span></span>
<span data-ttu-id="5b285-119">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="5b285-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5b285-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b285-120">-Confirm</span></span>
<span data-ttu-id="5b285-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b285-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b285-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b285-122">-WhatIf</span></span>
<span data-ttu-id="5b285-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b285-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b285-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b285-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b285-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b285-125">CommonParameters</span></span>
<span data-ttu-id="5b285-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b285-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b285-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b285-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b285-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b285-128">INPUTS</span></span>

### <span data-ttu-id="5b285-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="5b285-129">None</span></span>
<span data-ttu-id="5b285-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5b285-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b285-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b285-131">OUTPUTS</span></span>

### <span data-ttu-id="5b285-132">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="5b285-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="5b285-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b285-133">NOTES</span></span>

## <span data-ttu-id="5b285-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b285-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b285-135">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5b285-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="5b285-136">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5b285-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

