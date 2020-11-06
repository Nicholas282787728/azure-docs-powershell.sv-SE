---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580595"
---
# <span data-ttu-id="0af00-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0af00-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0af00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0af00-102">SYNOPSIS</span></span>
<span data-ttu-id="0af00-103">Ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="0af00-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0af00-104">SYNTAX</span></span>

### <span data-ttu-id="0af00-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="0af00-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af00-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="0af00-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af00-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0af00-107">DESCRIPTION</span></span>
<span data-ttu-id="0af00-108">Set-AzureKeyVaultCertificateIssuer cmdleten ställer in en certifikat utfärdare i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="0af00-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="0af00-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0af00-109">EXAMPLES</span></span>

### <span data-ttu-id="0af00-110">Exempel 1: Ange en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="0af00-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="0af00-111">Det här kommandot anger egenskaperna för en certifikat utfärdare och lagrar dem sedan i $Issuer variabel.</span><span class="sxs-lookup"><span data-stu-id="0af00-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="0af00-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0af00-112">PARAMETERS</span></span>

### <span data-ttu-id="0af00-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="0af00-113">-AccountId</span></span>
<span data-ttu-id="0af00-114">Anger konto-ID för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="0af00-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="0af00-115">-ApiKey</span></span>
<span data-ttu-id="0af00-116">Anger API-tangenten för certifikat utfärdaren.</span><span class="sxs-lookup"><span data-stu-id="0af00-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-117">-Utgivare</span><span class="sxs-lookup"><span data-stu-id="0af00-117">-Issuer</span></span>
<span data-ttu-id="0af00-118">Anger vilken certifikat utfärdare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="0af00-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="0af00-119">-IssuerProvider</span></span>
<span data-ttu-id="0af00-120">Anger typen av certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="0af00-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0af00-121">-Name</span></span>
<span data-ttu-id="0af00-122">Anger namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0af00-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="0af00-123">-OrganizationDetails</span></span>
<span data-ttu-id="0af00-124">Organisationsinformation för organisationen.</span><span class="sxs-lookup"><span data-stu-id="0af00-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0af00-125">-PassThru</span></span>
<span data-ttu-id="0af00-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0af00-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0af00-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0af00-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0af00-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0af00-128">-VaultName</span></span>
<span data-ttu-id="0af00-129">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="0af00-129">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af00-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0af00-130">-Confirm</span></span>
<span data-ttu-id="0af00-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0af00-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af00-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af00-132">-WhatIf</span></span>
<span data-ttu-id="0af00-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0af00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0af00-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0af00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af00-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af00-135">-DefaultProfile</span></span>
<span data-ttu-id="0af00-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0af00-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af00-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af00-137">CommonParameters</span></span>
<span data-ttu-id="0af00-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af00-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af00-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af00-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af00-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0af00-140">INPUTS</span></span>

## <span data-ttu-id="0af00-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0af00-141">OUTPUTS</span></span>

### <span data-ttu-id="0af00-142">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0af00-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0af00-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0af00-143">NOTES</span></span>

## <span data-ttu-id="0af00-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0af00-144">RELATED LINKS</span></span>

[<span data-ttu-id="0af00-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0af00-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0af00-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0af00-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

