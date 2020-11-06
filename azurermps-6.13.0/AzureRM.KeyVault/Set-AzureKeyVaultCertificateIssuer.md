---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574838"
---
# <span data-ttu-id="58c54-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="58c54-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="58c54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58c54-102">SYNOPSIS</span></span>
<span data-ttu-id="58c54-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="58c54-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58c54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58c54-104">SYNTAX</span></span>

### <span data-ttu-id="58c54-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="58c54-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c54-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="58c54-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c54-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58c54-107">DESCRIPTION</span></span>
<span data-ttu-id="58c54-108">Set-AzureKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="58c54-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="58c54-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58c54-109">EXAMPLES</span></span>

### <span data-ttu-id="58c54-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="58c54-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="58c54-111">Det här kommandot anger egenskaperna för en certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="58c54-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="58c54-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58c54-112">PARAMETERS</span></span>

### <span data-ttu-id="58c54-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="58c54-113">-AccountId</span></span>
<span data-ttu-id="58c54-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="58c54-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="58c54-115">-ApiKey</span></span>
<span data-ttu-id="58c54-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="58c54-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c54-117">-DefaultProfile</span></span>
<span data-ttu-id="58c54-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="58c54-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58c54-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58c54-119">-InputObject</span></span>
<span data-ttu-id="58c54-120">Anger vilken certifikat utfärdare som ska anges.</span><span class="sxs-lookup"><span data-stu-id="58c54-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="58c54-121">-IssuerProvider</span></span>
<span data-ttu-id="58c54-122">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="58c54-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="58c54-123">-Name</span></span>
<span data-ttu-id="58c54-124">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="58c54-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="58c54-125">-OrganizationDetails</span></span>
<span data-ttu-id="58c54-126">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="58c54-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58c54-127">-PassThru</span></span>
<span data-ttu-id="58c54-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="58c54-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58c54-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="58c54-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58c54-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58c54-130">-VaultName</span></span>
<span data-ttu-id="58c54-131">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="58c54-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c54-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58c54-132">-Confirm</span></span>
<span data-ttu-id="58c54-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58c54-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c54-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c54-134">-WhatIf</span></span>
<span data-ttu-id="58c54-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58c54-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c54-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58c54-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c54-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c54-137">CommonParameters</span></span>
<span data-ttu-id="58c54-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c54-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c54-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c54-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c54-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58c54-140">INPUTS</span></span>

### <span data-ttu-id="58c54-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="58c54-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="58c54-142">Parametrar: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58c54-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="58c54-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="58c54-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="58c54-144">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58c54-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="58c54-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58c54-145">OUTPUTS</span></span>

### <span data-ttu-id="58c54-146">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="58c54-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="58c54-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58c54-147">NOTES</span></span>

## <span data-ttu-id="58c54-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58c54-148">RELATED LINKS</span></span>

[<span data-ttu-id="58c54-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="58c54-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="58c54-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="58c54-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

