---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 56cc6b11c517379f1d13ebe2dbf2cee00f18211b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928790"
---
# <span data-ttu-id="5e09b-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5e09b-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="5e09b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e09b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e09b-103">Tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="5e09b-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e09b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e09b-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e09b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e09b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e09b-106">Remove-AzureKeyVaultSecret-cmdleten tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="5e09b-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="5e09b-107">Om hemligheten togs bort av misstag kan hemligheten återställas med Undo-AzureKeyVaultSecretRemoval av en användare med särskilda "återställnings behörighet".</span><span class="sxs-lookup"><span data-stu-id="5e09b-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="5e09b-108">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="5e09b-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="5e09b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e09b-109">EXAMPLES</span></span>

### <span data-ttu-id="5e09b-110">Exempel 1: ta bort en hemlighet från ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="5e09b-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="5e09b-111">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="5e09b-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="5e09b-112">Exempel 2: ta bort en hemlighet från ett nyckel valv utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="5e09b-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="5e09b-113">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="5e09b-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="5e09b-114">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e09b-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="5e09b-115">Exempel 3: rensa bort hemliga hemlighet från nyckel valvet permanent</span><span class="sxs-lookup"><span data-stu-id="5e09b-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="5e09b-116">Det här kommandot förflyttar den hemliga hemligheten med namnet FinanceSecret från nyckel valvet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="5e09b-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="5e09b-117">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="5e09b-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="5e09b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e09b-118">PARAMETERS</span></span>

### <span data-ttu-id="5e09b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e09b-119">-DefaultProfile</span></span>
<span data-ttu-id="5e09b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5e09b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e09b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5e09b-121">-Force</span></span>
<span data-ttu-id="5e09b-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5e09b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e09b-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5e09b-123">-InRemovedState</span></span>
<span data-ttu-id="5e09b-124">Om den visas tar du bort den hemliga hemligheten permanent.</span><span class="sxs-lookup"><span data-stu-id="5e09b-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="5e09b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e09b-125">-Name</span></span>
<span data-ttu-id="5e09b-126">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="5e09b-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="5e09b-127">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="5e09b-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e09b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e09b-128">-PassThru</span></span>
<span data-ttu-id="5e09b-129">Anger att den här cmdleten returnerar ett **Microsoft. Azure.-kommandon. nyckel valv.** rebärare-objekt.</span><span class="sxs-lookup"><span data-stu-id="5e09b-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="5e09b-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5e09b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e09b-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5e09b-131">-VaultName</span></span>
<span data-ttu-id="5e09b-132">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="5e09b-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="5e09b-133">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="5e09b-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5e09b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e09b-134">-Confirm</span></span>
<span data-ttu-id="5e09b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e09b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e09b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e09b-136">-WhatIf</span></span>
<span data-ttu-id="5e09b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e09b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e09b-138">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e09b-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e09b-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e09b-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e09b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e09b-140">CommonParameters</span></span>
<span data-ttu-id="5e09b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e09b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e09b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e09b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e09b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e09b-143">INPUTS</span></span>

### <span data-ttu-id="5e09b-144">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="5e09b-144">String</span></span>

## <span data-ttu-id="5e09b-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e09b-145">OUTPUTS</span></span>

### <span data-ttu-id="5e09b-146">Microsoft. Azure. commands. valv. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="5e09b-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="5e09b-147">Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .</span><span class="sxs-lookup"><span data-stu-id="5e09b-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="5e09b-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e09b-148">NOTES</span></span>

## <span data-ttu-id="5e09b-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e09b-149">RELATED LINKS</span></span>

[<span data-ttu-id="5e09b-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5e09b-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="5e09b-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5e09b-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="5e09b-152">Ångra-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="5e09b-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

