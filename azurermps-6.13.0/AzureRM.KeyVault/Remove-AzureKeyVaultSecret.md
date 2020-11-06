---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576965"
---
# <span data-ttu-id="e2863-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e2863-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="e2863-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2863-102">SYNOPSIS</span></span>
<span data-ttu-id="e2863-103">Tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="e2863-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2863-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2863-104">SYNTAX</span></span>

### <span data-ttu-id="e2863-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="e2863-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2863-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2863-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2863-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2863-107">DESCRIPTION</span></span>
<span data-ttu-id="e2863-108">Remove-AzureKeyVaultSecret-cmdleten tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="e2863-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="e2863-109">Om hemligheten togs bort av misstag kan hemligheten återställas med Undo-AzureKeyVaultSecretRemoval av en användare med särskilda "återställnings behörighet".</span><span class="sxs-lookup"><span data-stu-id="e2863-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="e2863-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="e2863-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="e2863-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2863-111">EXAMPLES</span></span>

### <span data-ttu-id="e2863-112">Exempel 1: ta bort en hemlighet från ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="e2863-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="e2863-113">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="e2863-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="e2863-114">Exempel 2: ta bort en hemlighet från ett nyckel valv utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="e2863-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="e2863-115">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="e2863-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="e2863-116">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2863-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e2863-117">Exempel 3: rensa bort hemliga hemlighet från nyckel valvet permanent</span><span class="sxs-lookup"><span data-stu-id="e2863-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="e2863-118">Det här kommandot förflyttar den hemliga hemligheten med namnet FinanceSecret från nyckel valvet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="e2863-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="e2863-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="e2863-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="e2863-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2863-120">PARAMETERS</span></span>

### <span data-ttu-id="e2863-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2863-121">-DefaultProfile</span></span>
<span data-ttu-id="e2863-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2863-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2863-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e2863-123">-Force</span></span>
<span data-ttu-id="e2863-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2863-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2863-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2863-125">-InputObject</span></span>
<span data-ttu-id="e2863-126">Hemliga nyckel valv objekt</span><span class="sxs-lookup"><span data-stu-id="e2863-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="e2863-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e2863-127">-InRemovedState</span></span>
<span data-ttu-id="e2863-128">Om den visas tar du bort den hemliga hemligheten permanent.</span><span class="sxs-lookup"><span data-stu-id="e2863-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="e2863-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2863-129">-Name</span></span>
<span data-ttu-id="e2863-130">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="e2863-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="e2863-131">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="e2863-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="e2863-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2863-132">-PassThru</span></span>
<span data-ttu-id="e2863-133">Anger att den här cmdleten returnerar ett **Microsoft. Azure.-kommandon. nyckel valv.** rebärare-objekt.</span><span class="sxs-lookup"><span data-stu-id="e2863-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="e2863-134">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e2863-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2863-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e2863-135">-VaultName</span></span>
<span data-ttu-id="e2863-136">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2863-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="e2863-137">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="e2863-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e2863-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2863-138">-Confirm</span></span>
<span data-ttu-id="e2863-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2863-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2863-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2863-140">-WhatIf</span></span>
<span data-ttu-id="e2863-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2863-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2863-142">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2863-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2863-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2863-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2863-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2863-144">CommonParameters</span></span>
<span data-ttu-id="e2863-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2863-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2863-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2863-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2863-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2863-147">INPUTS</span></span>

### <span data-ttu-id="e2863-148">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e2863-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="e2863-149">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2863-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e2863-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2863-150">OUTPUTS</span></span>

### <span data-ttu-id="e2863-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e2863-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="e2863-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2863-152">NOTES</span></span>

## <span data-ttu-id="e2863-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2863-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2863-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e2863-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="e2863-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e2863-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="e2863-156">Ångra-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e2863-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

