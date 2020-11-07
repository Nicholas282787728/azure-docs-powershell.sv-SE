---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928817"
---
# <span data-ttu-id="5f5f3-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5f5f3-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5f5f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5f3-103">Tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f5f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f5f3-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f5f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="5f5f3-106">Cmdleten **Remove-AzureKeyVaultCertificateContact** tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="5f5f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f5f3-107">EXAMPLES</span></span>

### <span data-ttu-id="5f5f3-108">Exempel 1: ta bort en certifikat kontakt</span><span class="sxs-lookup"><span data-stu-id="5f5f3-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="5f5f3-109">Det här kommandot tar bort Patti Nilsson som en certifikat kontakt för Contoso01-.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="5f5f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f5f3-110">PARAMETERS</span></span>

### <span data-ttu-id="5f5f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5f3-111">-DefaultProfile</span></span>
<span data-ttu-id="5f5f3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5f5f3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f5f3-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5f5f3-113">-EmailAddress</span></span>
<span data-ttu-id="5f5f3-114">Anger e-postadressen till den kontakt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="5f5f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f5f3-115">-PassThru</span></span>
<span data-ttu-id="5f5f3-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5f5f3-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5f5f3-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5f5f3-118">-VaultName</span></span>
<span data-ttu-id="5f5f3-119">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5f5f3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f5f3-120">-Confirm</span></span>
<span data-ttu-id="5f5f3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f5f3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f5f3-122">-WhatIf</span></span>
<span data-ttu-id="5f5f3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f5f3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f5f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5f3-125">CommonParameters</span></span>
<span data-ttu-id="5f5f3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5f3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5f3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5f3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f5f3-128">INPUTS</span></span>

## <span data-ttu-id="5f5f3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f5f3-129">OUTPUTS</span></span>

### <span data-ttu-id="5f5f3-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="5f5f3-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="5f5f3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f5f3-131">NOTES</span></span>

## <span data-ttu-id="5f5f3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f5f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f5f3-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5f5f3-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="5f5f3-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5f5f3-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

