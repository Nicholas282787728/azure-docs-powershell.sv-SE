---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263015"
---
# <span data-ttu-id="83f4c-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="83f4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="83f4c-103">Tar bort en nycklar i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="83f4c-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="83f4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83f4c-104">SYNTAX</span></span>

### <span data-ttu-id="83f4c-105">RemoveByKeyNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83f4c-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f4c-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f4c-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f4c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="83f4c-108">Remove-AzManagedHsmKey-cmdleten tar bort en nycklar i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="83f4c-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="83f4c-109">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzManagedHsmKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="83f4c-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="83f4c-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="83f4c-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="83f4c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83f4c-111">EXAMPLES</span></span>

### <span data-ttu-id="83f4c-112">Exempel 1: ta bort en Key från en hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="83f4c-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="83f4c-113">Det här kommandot tar bort den nycklar som heter testkey från den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="83f4c-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="83f4c-114">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="83f4c-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="83f4c-115">Det här kommandot tar bort den nycklar som heter testkey från den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="83f4c-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="83f4c-116">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="83f4c-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="83f4c-117">Exempel 3: ta bort en borttagen från hanterad HSM permanent</span><span class="sxs-lookup"><span data-stu-id="83f4c-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="83f4c-118">Det här kommandot tar bort den nycklar som heter testkey från den hanterade HSM som heter testmhsm permanent.</span><span class="sxs-lookup"><span data-stu-id="83f4c-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="83f4c-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen beviljas användaren för den här hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="83f4c-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="83f4c-120">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="83f4c-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="83f4c-121">Det här kommandot får alla nycklar i den hanterade HSM som heter testmhsm och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="83f4c-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83f4c-122">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83f4c-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="83f4c-123">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83f4c-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="83f4c-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83f4c-124">PARAMETERS</span></span>

### <span data-ttu-id="83f4c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f4c-125">-DefaultProfile</span></span>
<span data-ttu-id="83f4c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83f4c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f4c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="83f4c-127">-Force</span></span>
<span data-ttu-id="83f4c-128">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="83f4c-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="83f4c-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="83f4c-129">-HsmName</span></span>
<span data-ttu-id="83f4c-130">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="83f4c-130">HSM name.</span></span> <span data-ttu-id="83f4c-131">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="83f4c-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f4c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f4c-132">-InputObject</span></span>
<span data-ttu-id="83f4c-133">Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="83f4c-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83f4c-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="83f4c-134">-InRemovedState</span></span>
<span data-ttu-id="83f4c-135">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="83f4c-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="83f4c-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="83f4c-136">-Name</span></span>
<span data-ttu-id="83f4c-137">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="83f4c-137">Key name.</span></span>
<span data-ttu-id="83f4c-138">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="83f4c-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f4c-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83f4c-139">-PassThru</span></span>
<span data-ttu-id="83f4c-140">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="83f4c-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="83f4c-141">Om den här växeln anges returnerar cmdleten det nyckelattribut som togs bort.</span><span class="sxs-lookup"><span data-stu-id="83f4c-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="83f4c-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83f4c-142">-Confirm</span></span>
<span data-ttu-id="83f4c-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83f4c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f4c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f4c-144">-WhatIf</span></span>
<span data-ttu-id="83f4c-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83f4c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f4c-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83f4c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f4c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f4c-147">CommonParameters</span></span>
<span data-ttu-id="83f4c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f4c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f4c-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83f4c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f4c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83f4c-150">INPUTS</span></span>

### <span data-ttu-id="83f4c-151">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="83f4c-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="83f4c-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83f4c-152">OUTPUTS</span></span>

### <span data-ttu-id="83f4c-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="83f4c-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83f4c-154">NOTES</span></span>

## <span data-ttu-id="83f4c-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83f4c-155">RELATED LINKS</span></span>

[<span data-ttu-id="83f4c-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="83f4c-157">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="83f4c-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="83f4c-159">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="83f4c-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="83f4c-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="83f4c-161">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="83f4c-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)