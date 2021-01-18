---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520415"
---
# <span data-ttu-id="93ccd-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="93ccd-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="93ccd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="93ccd-103">Tar bort en certifikat utfärdare från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="93ccd-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="93ccd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93ccd-104">SYNTAX</span></span>

### <span data-ttu-id="93ccd-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="93ccd-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ccd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="93ccd-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ccd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="93ccd-108">Cmdleten **Remove-AzKeyVaultCertificateIssuer** tar bort en certifikat utfärdare från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="93ccd-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="93ccd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="93ccd-110">Exempel 1: ta bort en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="93ccd-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="93ccd-111">Det här kommandot tar bort certifikat utfärdaren som heter TestIssuer01 från ContosoKV01-.</span><span class="sxs-lookup"><span data-stu-id="93ccd-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="93ccd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="93ccd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ccd-113">-DefaultProfile</span></span>
<span data-ttu-id="93ccd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="93ccd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93ccd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93ccd-115">-Force</span></span>
<span data-ttu-id="93ccd-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="93ccd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93ccd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ccd-117">-InputObject</span></span>
<span data-ttu-id="93ccd-118">Objekt i certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="93ccd-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="93ccd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="93ccd-119">-Name</span></span>
<span data-ttu-id="93ccd-120">Anger namnet på den utfärdare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="93ccd-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="93ccd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ccd-121">-PassThru</span></span>
<span data-ttu-id="93ccd-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="93ccd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93ccd-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="93ccd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93ccd-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="93ccd-124">-VaultName</span></span>
<span data-ttu-id="93ccd-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="93ccd-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="93ccd-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93ccd-126">-Confirm</span></span>
<span data-ttu-id="93ccd-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93ccd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ccd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ccd-128">-WhatIf</span></span>
<span data-ttu-id="93ccd-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93ccd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ccd-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93ccd-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ccd-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93ccd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ccd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ccd-132">CommonParameters</span></span>
<span data-ttu-id="93ccd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ccd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ccd-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93ccd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ccd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93ccd-135">INPUTS</span></span>

### <span data-ttu-id="93ccd-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="93ccd-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="93ccd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93ccd-137">OUTPUTS</span></span>

### <span data-ttu-id="93ccd-138">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="93ccd-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="93ccd-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93ccd-139">NOTES</span></span>

## <span data-ttu-id="93ccd-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93ccd-140">RELATED LINKS</span></span>

[<span data-ttu-id="93ccd-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="93ccd-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="93ccd-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="93ccd-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


