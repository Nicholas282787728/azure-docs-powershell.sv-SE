---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755948"
---
# <span data-ttu-id="9cf89-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9cf89-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9cf89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cf89-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf89-103">Tar bort en certifikat utfärdare från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="9cf89-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cf89-104">SYNTAX</span></span>

### <span data-ttu-id="9cf89-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="9cf89-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf89-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf89-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf89-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cf89-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf89-108">Cmdleten **Remove-AzureKeyVaultCertificateIssuer** tar bort en certifikat utfärdare från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="9cf89-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="9cf89-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cf89-109">EXAMPLES</span></span>

### <span data-ttu-id="9cf89-110">Exempel 1: ta bort en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="9cf89-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="9cf89-111">Det här kommandot tar bort certifikat utfärdaren som heter TestIssuer01 från ContosoKV01-.</span><span class="sxs-lookup"><span data-stu-id="9cf89-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9cf89-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cf89-112">PARAMETERS</span></span>

### <span data-ttu-id="9cf89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf89-113">-DefaultProfile</span></span>
<span data-ttu-id="9cf89-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9cf89-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cf89-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9cf89-115">-Force</span></span>
<span data-ttu-id="9cf89-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9cf89-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cf89-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf89-117">-InputObject</span></span>
<span data-ttu-id="9cf89-118">Objekt i certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="9cf89-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf89-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cf89-119">-Name</span></span>
<span data-ttu-id="9cf89-120">Anger namnet på den utfärdare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9cf89-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf89-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cf89-121">-PassThru</span></span>
<span data-ttu-id="9cf89-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9cf89-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cf89-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9cf89-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cf89-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9cf89-124">-VaultName</span></span>
<span data-ttu-id="9cf89-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="9cf89-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf89-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cf89-126">-Confirm</span></span>
<span data-ttu-id="9cf89-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cf89-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf89-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf89-128">-WhatIf</span></span>
<span data-ttu-id="9cf89-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cf89-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf89-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cf89-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf89-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cf89-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf89-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf89-132">CommonParameters</span></span>
<span data-ttu-id="9cf89-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf89-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf89-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf89-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf89-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cf89-135">INPUTS</span></span>

### <span data-ttu-id="9cf89-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9cf89-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="9cf89-137">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9cf89-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9cf89-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cf89-138">OUTPUTS</span></span>

### <span data-ttu-id="9cf89-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9cf89-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9cf89-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cf89-140">NOTES</span></span>

## <span data-ttu-id="9cf89-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cf89-141">RELATED LINKS</span></span>

[<span data-ttu-id="9cf89-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9cf89-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9cf89-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9cf89-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


