---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583280"
---
# <span data-ttu-id="14a4f-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14a4f-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="14a4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="14a4f-103">Tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="14a4f-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14a4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14a4f-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="14a4f-106">Remove-AzureKeyVaultSecret-cmdleten tar bort en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="14a4f-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="14a4f-107">Om hemligheten togs bort av misstag kan hemligheten återställas med Undo-AzureKeyVaultSecretRemoval av en användare med särskilda "återställnings behörighet".</span><span class="sxs-lookup"><span data-stu-id="14a4f-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="14a4f-108">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="14a4f-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="14a4f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14a4f-109">EXAMPLES</span></span>

### <span data-ttu-id="14a4f-110">Exempel 1: ta bort en hemlighet från ett nyckel valv</span><span class="sxs-lookup"><span data-stu-id="14a4f-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="14a4f-111">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="14a4f-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="14a4f-112">Exempel 2: ta bort en hemlighet från ett nyckel valv utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="14a4f-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="14a4f-113">Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="14a4f-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="14a4f-114">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a4f-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="14a4f-115">Exempel 3: rensa bort hemliga hemlighet från nyckel valvet permanent</span><span class="sxs-lookup"><span data-stu-id="14a4f-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="14a4f-116">Det här kommandot förflyttar den hemliga hemligheten med namnet FinanceSecret från nyckel valvet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="14a4f-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="14a4f-117">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="14a4f-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="14a4f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14a4f-118">PARAMETERS</span></span>

### <span data-ttu-id="14a4f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="14a4f-119">-Force</span></span>
<span data-ttu-id="14a4f-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="14a4f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14a4f-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="14a4f-121">-InRemovedState</span></span>
<span data-ttu-id="14a4f-122">Om den visas tar du bort den hemliga hemligheten permanent.</span><span class="sxs-lookup"><span data-stu-id="14a4f-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="14a4f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="14a4f-123">-Name</span></span>
<span data-ttu-id="14a4f-124">Anger namnet på en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="14a4f-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="14a4f-125">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="14a4f-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a4f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14a4f-126">-PassThru</span></span>
<span data-ttu-id="14a4f-127">Anger att den här cmdleten returnerar ett **Microsoft. Azure.-kommandon. nyckel valv.** rebärare-objekt.</span><span class="sxs-lookup"><span data-stu-id="14a4f-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="14a4f-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="14a4f-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14a4f-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="14a4f-129">-VaultName</span></span>
<span data-ttu-id="14a4f-130">Anger namnet på det nyckel valv som hemligheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="14a4f-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="14a4f-131">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="14a4f-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="14a4f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14a4f-132">-Confirm</span></span>
<span data-ttu-id="14a4f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a4f-134">-WhatIf</span></span>
<span data-ttu-id="14a4f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14a4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a4f-136">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14a4f-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a4f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14a4f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a4f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a4f-138">-DefaultProfile</span></span>
<span data-ttu-id="14a4f-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14a4f-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a4f-140">CommonParameters</span></span>
<span data-ttu-id="14a4f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a4f-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a4f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a4f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14a4f-143">INPUTS</span></span>

### <span data-ttu-id="14a4f-144">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="14a4f-144">String</span></span>

## <span data-ttu-id="14a4f-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14a4f-145">OUTPUTS</span></span>

### <span data-ttu-id="14a4f-146">Microsoft. Azure. commands. valv. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="14a4f-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="14a4f-147">Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .</span><span class="sxs-lookup"><span data-stu-id="14a4f-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="14a4f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14a4f-148">NOTES</span></span>

## <span data-ttu-id="14a4f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14a4f-149">RELATED LINKS</span></span>

[<span data-ttu-id="14a4f-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14a4f-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="14a4f-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14a4f-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="14a4f-152">Ångra-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="14a4f-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

