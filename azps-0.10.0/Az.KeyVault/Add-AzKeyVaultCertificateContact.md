---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924494"
---
# <span data-ttu-id="62b49-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="62b49-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="62b49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62b49-102">SYNOPSIS</span></span>
<span data-ttu-id="62b49-103">Lägger till en kontakt för certifikat meddelanden.</span><span class="sxs-lookup"><span data-stu-id="62b49-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="62b49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62b49-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62b49-105">DESCRIPTION</span></span>
<span data-ttu-id="62b49-106">Cmdleten **Add-AzKeyVaultCertificateContact** lägger till en kontakt för ett nyckelords valv för certifikat meddelanden i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="62b49-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="62b49-107">Kontakten får uppdateringar om händelser som certifikat nära förfallo dag, certifikat förnyas och så vidare.</span><span class="sxs-lookup"><span data-stu-id="62b49-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="62b49-108">Dessa händelser bestäms av certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="62b49-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="62b49-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62b49-109">EXAMPLES</span></span>

### <span data-ttu-id="62b49-110">Exempel 1: lägga till en kontakt för ett nyckelord för en viktig valv</span><span class="sxs-lookup"><span data-stu-id="62b49-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="62b49-111">Det här kommandot lägger till Patti Nilsson som en certifikat kontakt för ContosoKV01-nyckelvärdet och returnerar **KeyVaultCertificateContact** -objektet.</span><span class="sxs-lookup"><span data-stu-id="62b49-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="62b49-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62b49-112">PARAMETERS</span></span>

### <span data-ttu-id="62b49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b49-113">-DefaultProfile</span></span>
<span data-ttu-id="62b49-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62b49-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62b49-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="62b49-115">-EmailAddress</span></span>
<span data-ttu-id="62b49-116">Anger kontaktens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="62b49-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="62b49-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b49-117">-PassThru</span></span>
<span data-ttu-id="62b49-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="62b49-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="62b49-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="62b49-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62b49-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="62b49-120">-VaultName</span></span>
<span data-ttu-id="62b49-121">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="62b49-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="62b49-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62b49-122">-Confirm</span></span>
<span data-ttu-id="62b49-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62b49-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b49-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b49-124">-WhatIf</span></span>
<span data-ttu-id="62b49-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62b49-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b49-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62b49-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b49-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b49-127">CommonParameters</span></span>
<span data-ttu-id="62b49-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b49-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b49-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b49-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b49-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62b49-130">INPUTS</span></span>

### <span data-ttu-id="62b49-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="62b49-131">None</span></span>
<span data-ttu-id="62b49-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="62b49-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62b49-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62b49-133">OUTPUTS</span></span>

### <span data-ttu-id="62b49-134">List<Microsoft. Azure.-kommandon. valv. KeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="62b49-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="62b49-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62b49-135">NOTES</span></span>

## <span data-ttu-id="62b49-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62b49-136">RELATED LINKS</span></span>

[<span data-ttu-id="62b49-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="62b49-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="62b49-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="62b49-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

