---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584327"
---
# <span data-ttu-id="1c2ee-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c2ee-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1c2ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2ee-103">Lägger till en kontakt för certifikat meddelanden.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c2ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c2ee-104">SYNTAX</span></span>

### <span data-ttu-id="1c2ee-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="1c2ee-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2ee-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1c2ee-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c2ee-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c2ee-107">DESCRIPTION</span></span>
<span data-ttu-id="1c2ee-108">Cmdleten **Add-AzureKeyVaultCertificateContact** lägger till en kontakt för ett nyckelords valv för certifikat meddelanden i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="1c2ee-109">Kontakten får uppdateringar om händelser som certifikat nära förfallo dag, certifikat förnyas och så vidare.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="1c2ee-110">Dessa händelser bestäms av certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="1c2ee-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c2ee-111">EXAMPLES</span></span>

### <span data-ttu-id="1c2ee-112">Exempel 1: lägga till en kontakt för ett nyckelord för en viktig valv</span><span class="sxs-lookup"><span data-stu-id="1c2ee-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="1c2ee-113">Det här kommandot lägger till Patti Nilsson som en certifikat kontakt för ContosoKV01-nyckelvärdet och returnerar **KeyVaultCertificateContact** -objektet.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="1c2ee-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c2ee-114">PARAMETERS</span></span>

### <span data-ttu-id="1c2ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2ee-115">-DefaultProfile</span></span>
<span data-ttu-id="1c2ee-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c2ee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c2ee-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1c2ee-117">-EmailAddress</span></span>
<span data-ttu-id="1c2ee-118">Anger kontaktens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c2ee-119">-InputObject</span></span>
<span data-ttu-id="1c2ee-120">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c2ee-121">-PassThru</span></span>
<span data-ttu-id="1c2ee-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c2ee-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c2ee-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1c2ee-124">-VaultName</span></span>
<span data-ttu-id="1c2ee-125">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ee-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c2ee-126">-Confirm</span></span>
<span data-ttu-id="1c2ee-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2ee-128">-WhatIf</span></span>
<span data-ttu-id="1c2ee-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c2ee-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2ee-131">CommonParameters</span></span>
<span data-ttu-id="1c2ee-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2ee-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2ee-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2ee-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c2ee-134">INPUTS</span></span>

### <span data-ttu-id="1c2ee-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c2ee-135">None</span></span>
<span data-ttu-id="1c2ee-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1c2ee-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c2ee-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c2ee-137">OUTPUTS</span></span>

### <span data-ttu-id="1c2ee-138">List<Microsoft. Azure.-kommandon. valv. PSKeyVaultCertificateContact-></span><span class="sxs-lookup"><span data-stu-id="1c2ee-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="1c2ee-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c2ee-139">NOTES</span></span>

## <span data-ttu-id="1c2ee-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c2ee-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c2ee-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c2ee-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="1c2ee-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c2ee-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

