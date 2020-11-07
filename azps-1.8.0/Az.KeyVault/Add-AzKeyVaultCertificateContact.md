---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ff363ae1bf6581baaeb177edd4e215494c82f85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916382"
---
# <span data-ttu-id="fab01-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fab01-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fab01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fab01-102">SYNOPSIS</span></span>
<span data-ttu-id="fab01-103">Lägger till en kontakt för certifikat meddelanden.</span><span class="sxs-lookup"><span data-stu-id="fab01-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="fab01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fab01-104">SYNTAX</span></span>

### <span data-ttu-id="fab01-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="fab01-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab01-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="fab01-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab01-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fab01-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab01-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fab01-108">DESCRIPTION</span></span>
<span data-ttu-id="fab01-109">Cmdleten **Add-AzKeyVaultCertificateContact** lägger till en kontakt för ett nyckelords valv för certifikat meddelanden i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fab01-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="fab01-110">Kontakten får uppdateringar om händelser som certifikat nära förfallo dag, certifikat förnyas och så vidare.</span><span class="sxs-lookup"><span data-stu-id="fab01-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="fab01-111">Dessa händelser bestäms av certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="fab01-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="fab01-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fab01-112">EXAMPLES</span></span>

### <span data-ttu-id="fab01-113">Exempel 1: lägga till en kontakt för ett nyckelord för en viktig valv</span><span class="sxs-lookup"><span data-stu-id="fab01-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="fab01-114">Det här kommandot lägger till Patti Nilsson som en certifikat kontakt för ContosoKV01-valv och returnerar listan med kontakter för "ContosoKV01"-valvet.</span><span class="sxs-lookup"><span data-stu-id="fab01-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="fab01-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fab01-115">PARAMETERS</span></span>

### <span data-ttu-id="fab01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab01-116">-DefaultProfile</span></span>
<span data-ttu-id="fab01-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fab01-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fab01-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="fab01-118">-EmailAddress</span></span>
<span data-ttu-id="fab01-119">Anger kontaktens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="fab01-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab01-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab01-120">-InputObject</span></span>
<span data-ttu-id="fab01-121">Valv objekt.</span><span class="sxs-lookup"><span data-stu-id="fab01-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fab01-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab01-122">-PassThru</span></span>
<span data-ttu-id="fab01-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fab01-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fab01-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fab01-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab01-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fab01-125">-ResourceId</span></span>
<span data-ttu-id="fab01-126">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="fab01-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab01-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fab01-127">-VaultName</span></span>
<span data-ttu-id="fab01-128">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="fab01-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab01-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fab01-129">-Confirm</span></span>
<span data-ttu-id="fab01-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fab01-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab01-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab01-131">-WhatIf</span></span>
<span data-ttu-id="fab01-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fab01-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab01-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fab01-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab01-134">CommonParameters</span></span>
<span data-ttu-id="fab01-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab01-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab01-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab01-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fab01-137">INPUTS</span></span>

### <span data-ttu-id="fab01-138">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fab01-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fab01-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fab01-139">System.String</span></span>

## <span data-ttu-id="fab01-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fab01-140">OUTPUTS</span></span>

### <span data-ttu-id="fab01-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fab01-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fab01-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fab01-142">NOTES</span></span>

## <span data-ttu-id="fab01-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fab01-143">RELATED LINKS</span></span>

[<span data-ttu-id="fab01-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fab01-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="fab01-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fab01-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

