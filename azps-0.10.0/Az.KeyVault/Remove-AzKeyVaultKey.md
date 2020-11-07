---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922682"
---
# <span data-ttu-id="99d8c-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99d8c-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="99d8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="99d8c-103">Tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="99d8c-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="99d8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99d8c-104">SYNTAX</span></span>

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="99d8c-106">Remove-AzKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="99d8c-106">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="99d8c-107">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="99d8c-107">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="99d8c-108">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="99d8c-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="99d8c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99d8c-109">EXAMPLES</span></span>

### <span data-ttu-id="99d8c-110">Exempel 1: ta bort en Key från ett nyckelord</span><span class="sxs-lookup"><span data-stu-id="99d8c-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="99d8c-111">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="99d8c-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="99d8c-112">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="99d8c-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="99d8c-113">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="99d8c-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="99d8c-114">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99d8c-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="99d8c-115">Exempel 3: ta bort en borttagen Key från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="99d8c-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="99d8c-116">Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="99d8c-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="99d8c-117">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="99d8c-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="99d8c-118">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="99d8c-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="99d8c-119">Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="99d8c-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="99d8c-120">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99d8c-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="99d8c-121">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d8c-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="99d8c-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99d8c-122">PARAMETERS</span></span>

### <span data-ttu-id="99d8c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d8c-123">-DefaultProfile</span></span>
<span data-ttu-id="99d8c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99d8c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d8c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="99d8c-125">-Force</span></span>
<span data-ttu-id="99d8c-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="99d8c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99d8c-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="99d8c-127">-InRemovedState</span></span>
<span data-ttu-id="99d8c-128">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="99d8c-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="99d8c-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="99d8c-129">-Name</span></span>
<span data-ttu-id="99d8c-130">Anger namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="99d8c-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="99d8c-131">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="99d8c-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d8c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99d8c-132">-PassThru</span></span>
<span data-ttu-id="99d8c-133">Anger att denna cmdlet returnerar ett **Microsoft. Azure. commands. valv** .-objekt för paket.</span><span class="sxs-lookup"><span data-stu-id="99d8c-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="99d8c-134">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="99d8c-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99d8c-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="99d8c-135">-VaultName</span></span>
<span data-ttu-id="99d8c-136">Anger namnet på det nyckelord som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="99d8c-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="99d8c-137">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="99d8c-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="99d8c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99d8c-138">-Confirm</span></span>
<span data-ttu-id="99d8c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99d8c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d8c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d8c-140">-WhatIf</span></span>
<span data-ttu-id="99d8c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99d8c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d8c-142">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99d8c-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d8c-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99d8c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d8c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d8c-144">CommonParameters</span></span>
<span data-ttu-id="99d8c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d8c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d8c-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d8c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d8c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99d8c-147">INPUTS</span></span>

### <span data-ttu-id="99d8c-148">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="99d8c-148">String</span></span>

## <span data-ttu-id="99d8c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99d8c-149">OUTPUTS</span></span>

### <span data-ttu-id="99d8c-150">Microsoft. Azure. commands. valv. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="99d8c-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="99d8c-151">Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .</span><span class="sxs-lookup"><span data-stu-id="99d8c-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="99d8c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99d8c-152">NOTES</span></span>

## <span data-ttu-id="99d8c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99d8c-153">RELATED LINKS</span></span>

[<span data-ttu-id="99d8c-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99d8c-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="99d8c-155">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99d8c-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="99d8c-156">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="99d8c-156">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="99d8c-157">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="99d8c-157">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

