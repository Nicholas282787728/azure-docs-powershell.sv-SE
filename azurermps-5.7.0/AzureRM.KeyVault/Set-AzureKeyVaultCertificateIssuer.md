---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585135"
---
# <span data-ttu-id="bf3b7-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="bf3b7-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="bf3b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3b7-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf3b7-104">SYNTAX</span></span>

### <span data-ttu-id="bf3b7-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="bf3b7-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf3b7-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="bf3b7-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf3b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="bf3b7-108">Set-AzureKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="bf3b7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf3b7-109">EXAMPLES</span></span>

### <span data-ttu-id="bf3b7-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="bf3b7-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="bf3b7-111">Det här kommandot anger egenskaperna för en certifikat utfärdare och lagrar dem sedan i $Issuer variabel.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="bf3b7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf3b7-112">PARAMETERS</span></span>

### <span data-ttu-id="bf3b7-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="bf3b7-113">-AccountId</span></span>
<span data-ttu-id="bf3b7-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="bf3b7-115">-ApiKey</span></span>
<span data-ttu-id="bf3b7-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3b7-117">-DefaultProfile</span></span>
<span data-ttu-id="bf3b7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf3b7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf3b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf3b7-119">-InputObject</span></span>
<span data-ttu-id="bf3b7-120">Anger vilken certifikat utfärdare som ska anges.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="bf3b7-121">-IssuerProvider</span></span>
<span data-ttu-id="bf3b7-122">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf3b7-123">-Name</span></span>
<span data-ttu-id="bf3b7-124">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="bf3b7-125">-OrganizationDetails</span></span>
<span data-ttu-id="bf3b7-126">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf3b7-127">-PassThru</span></span>
<span data-ttu-id="bf3b7-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf3b7-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf3b7-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bf3b7-130">-VaultName</span></span>
<span data-ttu-id="bf3b7-131">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="bf3b7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf3b7-132">-Confirm</span></span>
<span data-ttu-id="bf3b7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf3b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf3b7-134">-WhatIf</span></span>
<span data-ttu-id="bf3b7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf3b7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf3b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3b7-137">CommonParameters</span></span>
<span data-ttu-id="bf3b7-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3b7-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3b7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3b7-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf3b7-140">INPUTS</span></span>

### <span data-ttu-id="bf3b7-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="bf3b7-141">None</span></span>
<span data-ttu-id="bf3b7-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bf3b7-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf3b7-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf3b7-143">OUTPUTS</span></span>

### <span data-ttu-id="bf3b7-144">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf3b7-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bf3b7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf3b7-145">NOTES</span></span>

## <span data-ttu-id="bf3b7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf3b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf3b7-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="bf3b7-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="bf3b7-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="bf3b7-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

