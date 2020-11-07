---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 2989a3b50eaf4e7c8993a407823b5a1c42c3503b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916274"
---
# <span data-ttu-id="d88e6-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d88e6-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="d88e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d88e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d88e6-103">Tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="d88e6-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="d88e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d88e6-104">SYNTAX</span></span>

### <span data-ttu-id="d88e6-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="d88e6-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d88e6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d88e6-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d88e6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d88e6-107">DESCRIPTION</span></span>
<span data-ttu-id="d88e6-108">Remove-AzKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="d88e6-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="d88e6-109">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="d88e6-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="d88e6-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="d88e6-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="d88e6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d88e6-111">EXAMPLES</span></span>

### <span data-ttu-id="d88e6-112">Exempel 1: ta bort en Key från ett nyckelord</span><span class="sxs-lookup"><span data-stu-id="d88e6-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d88e6-113">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="d88e6-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="d88e6-114">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="d88e6-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="d88e6-115">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="d88e6-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="d88e6-116">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d88e6-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d88e6-117">Exempel 3: ta bort en borttagen Key från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="d88e6-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="d88e6-118">Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="d88e6-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="d88e6-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="d88e6-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="d88e6-120">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="d88e6-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="d88e6-121">Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d88e6-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d88e6-122">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d88e6-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="d88e6-123">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d88e6-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="d88e6-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d88e6-124">PARAMETERS</span></span>

### <span data-ttu-id="d88e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88e6-125">-DefaultProfile</span></span>
<span data-ttu-id="d88e6-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d88e6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d88e6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d88e6-127">-Force</span></span>
<span data-ttu-id="d88e6-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d88e6-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d88e6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d88e6-129">-InputObject</span></span>
<span data-ttu-id="d88e6-130">Paket-objekt</span><span class="sxs-lookup"><span data-stu-id="d88e6-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d88e6-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d88e6-131">-InRemovedState</span></span>
<span data-ttu-id="d88e6-132">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="d88e6-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="d88e6-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="d88e6-133">-Name</span></span>
<span data-ttu-id="d88e6-134">Anger namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d88e6-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="d88e6-135">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="d88e6-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88e6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d88e6-136">-PassThru</span></span>
<span data-ttu-id="d88e6-137">Anger att denna cmdlet returnerar ett **Microsoft. Azure.-kommandon. PSKeyVaultKey..** ..</span><span class="sxs-lookup"><span data-stu-id="d88e6-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="d88e6-138">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d88e6-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d88e6-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d88e6-139">-VaultName</span></span>
<span data-ttu-id="d88e6-140">Anger namnet på det nyckelord som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="d88e6-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="d88e6-141">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="d88e6-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d88e6-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d88e6-142">-Confirm</span></span>
<span data-ttu-id="d88e6-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d88e6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88e6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88e6-144">-WhatIf</span></span>
<span data-ttu-id="d88e6-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d88e6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88e6-146">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d88e6-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88e6-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d88e6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88e6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88e6-148">CommonParameters</span></span>
<span data-ttu-id="d88e6-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88e6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88e6-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88e6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88e6-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d88e6-151">INPUTS</span></span>

### <span data-ttu-id="d88e6-152">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d88e6-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="d88e6-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d88e6-153">OUTPUTS</span></span>

### <span data-ttu-id="d88e6-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d88e6-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d88e6-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d88e6-155">NOTES</span></span>

## <span data-ttu-id="d88e6-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d88e6-156">RELATED LINKS</span></span>

[<span data-ttu-id="d88e6-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d88e6-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d88e6-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d88e6-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="d88e6-159">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d88e6-159">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="d88e6-160">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d88e6-160">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

