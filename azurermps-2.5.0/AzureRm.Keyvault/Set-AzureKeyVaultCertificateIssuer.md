---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 430a909e76c08ba0c19c18072fdf019cd2fa7b29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930230"
---
# <span data-ttu-id="4a88e-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4a88e-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4a88e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a88e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a88e-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="4a88e-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a88e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a88e-104">SYNTAX</span></span>

### <span data-ttu-id="4a88e-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="4a88e-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a88e-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="4a88e-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a88e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a88e-107">DESCRIPTION</span></span>
<span data-ttu-id="4a88e-108">Set-AzureKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="4a88e-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="4a88e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a88e-109">EXAMPLES</span></span>

### <span data-ttu-id="4a88e-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="4a88e-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="4a88e-111">Det här kommandot anger egenskaperna för en certifikat utfärdare och lagrar dem sedan i $Issuer variabel.</span><span class="sxs-lookup"><span data-stu-id="4a88e-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="4a88e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a88e-112">PARAMETERS</span></span>

### <span data-ttu-id="4a88e-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="4a88e-113">-AccountId</span></span>
<span data-ttu-id="4a88e-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="4a88e-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="4a88e-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="4a88e-115">-ApiKey</span></span>
<span data-ttu-id="4a88e-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="4a88e-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="4a88e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a88e-117">-DefaultProfile</span></span>
<span data-ttu-id="4a88e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4a88e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a88e-119">-Utgivare</span><span class="sxs-lookup"><span data-stu-id="4a88e-119">-Issuer</span></span>
<span data-ttu-id="4a88e-120">Anger vilken certifikat utfärdare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4a88e-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a88e-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="4a88e-121">-IssuerProvider</span></span>
<span data-ttu-id="4a88e-122">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="4a88e-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="4a88e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a88e-123">-Name</span></span>
<span data-ttu-id="4a88e-124">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="4a88e-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="4a88e-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="4a88e-125">-OrganizationDetails</span></span>
<span data-ttu-id="4a88e-126">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="4a88e-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a88e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a88e-127">-PassThru</span></span>
<span data-ttu-id="4a88e-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4a88e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a88e-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4a88e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a88e-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4a88e-130">-VaultName</span></span>
<span data-ttu-id="4a88e-131">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="4a88e-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="4a88e-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a88e-132">-Confirm</span></span>
<span data-ttu-id="4a88e-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a88e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a88e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a88e-134">-WhatIf</span></span>
<span data-ttu-id="4a88e-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a88e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a88e-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a88e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a88e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a88e-137">CommonParameters</span></span>
<span data-ttu-id="4a88e-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a88e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a88e-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a88e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a88e-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a88e-140">INPUTS</span></span>

## <span data-ttu-id="4a88e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a88e-141">OUTPUTS</span></span>

### <span data-ttu-id="4a88e-142">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4a88e-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4a88e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a88e-143">NOTES</span></span>

## <span data-ttu-id="4a88e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a88e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a88e-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4a88e-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4a88e-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4a88e-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

