---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089359"
---
# <span data-ttu-id="1ce7a-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ce7a-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="1ce7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ce7a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce7a-103">Tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="1ce7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ce7a-104">SYNTAX</span></span>

### <span data-ttu-id="1ce7a-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="1ce7a-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce7a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ce7a-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce7a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ce7a-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce7a-108">Remove-AzKeyVaultSecret-cmdleten tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="1ce7a-109">Om hemligheten togs bort av misstag kan hemligheten återställas med Undo-AzKeyVaultSecretRemoval av en användare med särskilda "återställnings behörighet".</span><span class="sxs-lookup"><span data-stu-id="1ce7a-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="1ce7a-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="1ce7a-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="1ce7a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ce7a-111">EXAMPLES</span></span>

### <span data-ttu-id="1ce7a-112">Exempel 1: ta bort en hemlighet från ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="1ce7a-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="1ce7a-113">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="1ce7a-114">Exempel 2: ta bort en hemlighet från ett nyckel valv utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="1ce7a-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="1ce7a-115">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="1ce7a-116">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="1ce7a-117">Exempel 3: rensa bort hemliga hemlighet från nyckel valvet permanent</span><span class="sxs-lookup"><span data-stu-id="1ce7a-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="1ce7a-118">Det här kommandot förflyttar den hemliga hemligheten med namnet FinanceSecret från nyckel valvet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="1ce7a-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="1ce7a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ce7a-120">PARAMETERS</span></span>

### <span data-ttu-id="1ce7a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce7a-121">-DefaultProfile</span></span>
<span data-ttu-id="1ce7a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1ce7a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ce7a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1ce7a-123">-Force</span></span>
<span data-ttu-id="1ce7a-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ce7a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce7a-125">-InputObject</span></span>
<span data-ttu-id="1ce7a-126">Hemliga nyckel valv objekt</span><span class="sxs-lookup"><span data-stu-id="1ce7a-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce7a-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1ce7a-127">-InRemovedState</span></span>
<span data-ttu-id="1ce7a-128">Om den visas tar du bort den hemliga hemligheten permanent.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="1ce7a-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ce7a-129">-Name</span></span>
<span data-ttu-id="1ce7a-130">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="1ce7a-131">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce7a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ce7a-132">-PassThru</span></span>
<span data-ttu-id="1ce7a-133">Anger att den här cmdleten returnerar ett **Microsoft. Azure.-kommandon. nyckel valv.** rebärare-objekt.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="1ce7a-134">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ce7a-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1ce7a-135">-VaultName</span></span>
<span data-ttu-id="1ce7a-136">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="1ce7a-137">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce7a-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ce7a-138">-Confirm</span></span>
<span data-ttu-id="1ce7a-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce7a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce7a-140">-WhatIf</span></span>
<span data-ttu-id="1ce7a-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce7a-142">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce7a-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce7a-144">CommonParameters</span></span>
<span data-ttu-id="1ce7a-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce7a-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ce7a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce7a-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ce7a-147">INPUTS</span></span>

### <span data-ttu-id="1ce7a-148">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1ce7a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="1ce7a-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ce7a-149">OUTPUTS</span></span>

### <span data-ttu-id="1ce7a-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ce7a-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="1ce7a-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ce7a-151">NOTES</span></span>

## <span data-ttu-id="1ce7a-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ce7a-152">RELATED LINKS</span></span>

[<span data-ttu-id="1ce7a-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ce7a-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="1ce7a-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1ce7a-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="1ce7a-155">Ångra-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="1ce7a-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

