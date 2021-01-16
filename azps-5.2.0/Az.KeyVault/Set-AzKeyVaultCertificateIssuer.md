---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393880"
---
# <span data-ttu-id="645b6-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="645b6-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="645b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="645b6-102">SYNOPSIS</span></span>
<span data-ttu-id="645b6-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="645b6-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="645b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="645b6-104">SYNTAX</span></span>

### <span data-ttu-id="645b6-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="645b6-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="645b6-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="645b6-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="645b6-107">DESCRIPTION</span></span>
<span data-ttu-id="645b6-108">Set-AzKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="645b6-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="645b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="645b6-109">EXAMPLES</span></span>

### <span data-ttu-id="645b6-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="645b6-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="645b6-111">Det här kommandot anger egenskaperna för en certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="645b6-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="645b6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="645b6-112">PARAMETERS</span></span>

### <span data-ttu-id="645b6-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="645b6-113">-AccountId</span></span>
<span data-ttu-id="645b6-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="645b6-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="645b6-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="645b6-115">-ApiKey</span></span>
<span data-ttu-id="645b6-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="645b6-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="645b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645b6-117">-DefaultProfile</span></span>
<span data-ttu-id="645b6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="645b6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="645b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="645b6-119">-InputObject</span></span>
<span data-ttu-id="645b6-120">Anger vilken certifikat utfärdare som ska anges.</span><span class="sxs-lookup"><span data-stu-id="645b6-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="645b6-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="645b6-121">-IssuerProvider</span></span>
<span data-ttu-id="645b6-122">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="645b6-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="645b6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="645b6-123">-Name</span></span>
<span data-ttu-id="645b6-124">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="645b6-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="645b6-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="645b6-125">-OrganizationDetails</span></span>
<span data-ttu-id="645b6-126">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="645b6-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="645b6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="645b6-127">-PassThru</span></span>
<span data-ttu-id="645b6-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="645b6-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="645b6-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="645b6-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="645b6-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="645b6-130">-VaultName</span></span>
<span data-ttu-id="645b6-131">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="645b6-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="645b6-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="645b6-132">-Confirm</span></span>
<span data-ttu-id="645b6-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="645b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645b6-134">-WhatIf</span></span>
<span data-ttu-id="645b6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="645b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="645b6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="645b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645b6-137">CommonParameters</span></span>
<span data-ttu-id="645b6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645b6-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="645b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645b6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="645b6-140">INPUTS</span></span>

### <span data-ttu-id="645b6-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="645b6-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="645b6-142">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="645b6-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="645b6-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="645b6-143">OUTPUTS</span></span>

### <span data-ttu-id="645b6-144">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="645b6-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="645b6-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="645b6-145">NOTES</span></span>

## <span data-ttu-id="645b6-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="645b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="645b6-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="645b6-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="645b6-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="645b6-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

