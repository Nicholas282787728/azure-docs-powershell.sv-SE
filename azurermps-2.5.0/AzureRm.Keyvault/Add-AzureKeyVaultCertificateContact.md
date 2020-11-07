---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9f52889f044ba6bf497b57a53f3e2daaea0dbf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928837"
---
# <span data-ttu-id="88910-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="88910-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="88910-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88910-102">SYNOPSIS</span></span>
<span data-ttu-id="88910-103">Lägger till en kontakt för certifikat meddelanden.</span><span class="sxs-lookup"><span data-stu-id="88910-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88910-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88910-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88910-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88910-105">DESCRIPTION</span></span>
<span data-ttu-id="88910-106">Cmdleten **Add-AzureKeyVaultCertificateContact** lägger till en kontakt för ett nyckelords valv för certifikat meddelanden i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="88910-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="88910-107">Kontakten får uppdateringar om händelser som certifikat nära förfallo dag, certifikat förnyas och så vidare.</span><span class="sxs-lookup"><span data-stu-id="88910-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="88910-108">Dessa händelser bestäms av certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="88910-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="88910-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88910-109">EXAMPLES</span></span>

### <span data-ttu-id="88910-110">Exempel 1: lägga till en kontakt för ett nyckelord för en viktig valv</span><span class="sxs-lookup"><span data-stu-id="88910-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="88910-111">Det här kommandot lägger till Patti Nilsson som en certifikat kontakt för ContosoKV01-nyckelvärdet och returnerar **KeyVaultCertificateContact** -objektet.</span><span class="sxs-lookup"><span data-stu-id="88910-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="88910-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88910-112">PARAMETERS</span></span>

### <span data-ttu-id="88910-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88910-113">-DefaultProfile</span></span>
<span data-ttu-id="88910-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="88910-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88910-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="88910-115">-EmailAddress</span></span>
<span data-ttu-id="88910-116">Anger kontaktens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="88910-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="88910-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88910-117">-PassThru</span></span>
<span data-ttu-id="88910-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="88910-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88910-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="88910-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88910-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="88910-120">-VaultName</span></span>
<span data-ttu-id="88910-121">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="88910-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="88910-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88910-122">-Confirm</span></span>
<span data-ttu-id="88910-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88910-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88910-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88910-124">-WhatIf</span></span>
<span data-ttu-id="88910-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88910-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88910-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88910-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88910-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88910-127">CommonParameters</span></span>
<span data-ttu-id="88910-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88910-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88910-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88910-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88910-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88910-130">INPUTS</span></span>

## <span data-ttu-id="88910-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88910-131">OUTPUTS</span></span>

### <span data-ttu-id="88910-132">List<Microsoft. Azure.-kommandon. valv. KeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="88910-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="88910-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88910-133">NOTES</span></span>

## <span data-ttu-id="88910-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88910-134">RELATED LINKS</span></span>

[<span data-ttu-id="88910-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="88910-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="88910-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="88910-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

