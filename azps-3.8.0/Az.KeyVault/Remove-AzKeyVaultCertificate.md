---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092605"
---
# <span data-ttu-id="a4fa9-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4fa9-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a4fa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fa9-103">Tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="a4fa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4fa9-104">SYNTAX</span></span>

### <span data-ttu-id="a4fa9-105">ByVaultNameAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="a4fa9-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4fa9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a4fa9-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4fa9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="a4fa9-108">Cmdleten **Remove-AzKeyVaultCertificate** tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="a4fa9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4fa9-109">EXAMPLES</span></span>

### <span data-ttu-id="a4fa9-110">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="a4fa9-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="a4fa9-111">Det här kommandot tar bort certifikatet som heter SelfSigned01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="a4fa9-112">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="a4fa9-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a4fa9-113">Därför behöver du inte bekräfta en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a4fa9-114">Exempel 2: ta bort det borttagna certifikatet från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="a4fa9-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="a4fa9-115">Det här kommandot tar permanent bort certifikatet med namnet ' mitt certifikat ' från huvud valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="a4fa9-116">För att köra denna cmdlet krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren i det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="a4fa9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4fa9-117">PARAMETERS</span></span>

### <span data-ttu-id="a4fa9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fa9-118">-DefaultProfile</span></span>
<span data-ttu-id="a4fa9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4fa9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4fa9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a4fa9-120">-Force</span></span>
<span data-ttu-id="a4fa9-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4fa9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4fa9-122">-InputObject</span></span>
<span data-ttu-id="a4fa9-123">Certifikat objekt.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fa9-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a4fa9-124">-InRemovedState</span></span>
<span data-ttu-id="a4fa9-125">Om det finns någon tar bort det tidigare borttagna certifikatet permanent</span><span class="sxs-lookup"><span data-stu-id="a4fa9-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="a4fa9-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4fa9-126">-Name</span></span>
<span data-ttu-id="a4fa9-127">Anger namnet på det certifikat som denna cmdlet tar bort från ett valv.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="a4fa9-128">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fa9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4fa9-129">-PassThru</span></span>
<span data-ttu-id="a4fa9-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4fa9-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4fa9-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a4fa9-132">-VaultName</span></span>
<span data-ttu-id="a4fa9-133">Anger namnet på det huvud valv som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="a4fa9-134">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fa9-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4fa9-135">-Confirm</span></span>
<span data-ttu-id="a4fa9-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4fa9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4fa9-137">-WhatIf</span></span>
<span data-ttu-id="a4fa9-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fa9-139">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4fa9-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4fa9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fa9-141">CommonParameters</span></span>
<span data-ttu-id="a4fa9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fa9-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4fa9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fa9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4fa9-144">INPUTS</span></span>

### <span data-ttu-id="a4fa9-145">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a4fa9-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a4fa9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4fa9-146">OUTPUTS</span></span>

### <span data-ttu-id="a4fa9-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4fa9-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="a4fa9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4fa9-148">NOTES</span></span>

## <span data-ttu-id="a4fa9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4fa9-149">RELATED LINKS</span></span>

[<span data-ttu-id="a4fa9-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4fa9-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4fa9-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4fa9-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4fa9-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4fa9-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="a4fa9-153">Ångra-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="a4fa9-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)