---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924442"
---
# <span data-ttu-id="73a09-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="73a09-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="73a09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73a09-102">SYNOPSIS</span></span>
<span data-ttu-id="73a09-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="73a09-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="73a09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73a09-104">SYNTAX</span></span>

### <span data-ttu-id="73a09-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="73a09-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a09-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="73a09-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a09-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73a09-107">DESCRIPTION</span></span>
<span data-ttu-id="73a09-108">Set-AzKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="73a09-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="73a09-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73a09-109">EXAMPLES</span></span>

### <span data-ttu-id="73a09-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="73a09-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="73a09-111">Det här kommandot anger egenskaperna för en certifikat utfärdare och lagrar dem sedan i $Issuer variabel.</span><span class="sxs-lookup"><span data-stu-id="73a09-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="73a09-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73a09-112">PARAMETERS</span></span>

### <span data-ttu-id="73a09-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="73a09-113">-AccountId</span></span>
<span data-ttu-id="73a09-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="73a09-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="73a09-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="73a09-115">-ApiKey</span></span>
<span data-ttu-id="73a09-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="73a09-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="73a09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a09-117">-DefaultProfile</span></span>
<span data-ttu-id="73a09-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="73a09-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73a09-119">-Utgivare</span><span class="sxs-lookup"><span data-stu-id="73a09-119">-Issuer</span></span>
<span data-ttu-id="73a09-120">Anger vilken certifikat utfärdare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="73a09-120">Specifies the certificate issuer to update.</span></span>

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

### <span data-ttu-id="73a09-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="73a09-121">-IssuerProvider</span></span>
<span data-ttu-id="73a09-122">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="73a09-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="73a09-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="73a09-123">-Name</span></span>
<span data-ttu-id="73a09-124">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="73a09-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="73a09-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="73a09-125">-OrganizationDetails</span></span>
<span data-ttu-id="73a09-126">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="73a09-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="73a09-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73a09-127">-PassThru</span></span>
<span data-ttu-id="73a09-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="73a09-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="73a09-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="73a09-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="73a09-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="73a09-130">-VaultName</span></span>
<span data-ttu-id="73a09-131">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="73a09-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="73a09-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73a09-132">-Confirm</span></span>
<span data-ttu-id="73a09-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73a09-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a09-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a09-134">-WhatIf</span></span>
<span data-ttu-id="73a09-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73a09-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a09-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73a09-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a09-137">CommonParameters</span></span>
<span data-ttu-id="73a09-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a09-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a09-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a09-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73a09-140">INPUTS</span></span>

### <span data-ttu-id="73a09-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="73a09-141">None</span></span>
<span data-ttu-id="73a09-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="73a09-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73a09-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73a09-143">OUTPUTS</span></span>

### <span data-ttu-id="73a09-144">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="73a09-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="73a09-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73a09-145">NOTES</span></span>

## <span data-ttu-id="73a09-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73a09-146">RELATED LINKS</span></span>

[<span data-ttu-id="73a09-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="73a09-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="73a09-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="73a09-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

