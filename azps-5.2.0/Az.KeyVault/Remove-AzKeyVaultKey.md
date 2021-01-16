---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394888"
---
# <span data-ttu-id="54ceb-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="54ceb-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="54ceb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="54ceb-103">Tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="54ceb-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="54ceb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54ceb-104">SYNTAX</span></span>

### <span data-ttu-id="54ceb-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="54ceb-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ceb-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="54ceb-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ceb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="54ceb-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ceb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54ceb-108">DESCRIPTION</span></span>
<span data-ttu-id="54ceb-109">Remove-AzKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="54ceb-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="54ceb-110">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="54ceb-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="54ceb-111">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="54ceb-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="54ceb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54ceb-112">EXAMPLES</span></span>

### <span data-ttu-id="54ceb-113">Exempel 1: ta bort en Key från ett nyckelord</span><span class="sxs-lookup"><span data-stu-id="54ceb-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="54ceb-114">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="54ceb-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="54ceb-115">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="54ceb-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="54ceb-116">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="54ceb-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="54ceb-117">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="54ceb-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="54ceb-118">Exempel 3: ta bort en borttagen Key från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="54ceb-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="54ceb-119">Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="54ceb-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="54ceb-120">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="54ceb-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="54ceb-121">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="54ceb-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="54ceb-122">Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="54ceb-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54ceb-123">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54ceb-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="54ceb-124">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54ceb-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="54ceb-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54ceb-125">PARAMETERS</span></span>

### <span data-ttu-id="54ceb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ceb-126">-DefaultProfile</span></span>
<span data-ttu-id="54ceb-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54ceb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54ceb-128">-Force</span><span class="sxs-lookup"><span data-stu-id="54ceb-128">-Force</span></span>
<span data-ttu-id="54ceb-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="54ceb-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54ceb-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="54ceb-130">-HsmName</span></span>
<span data-ttu-id="54ceb-131">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="54ceb-131">HSM name.</span></span> <span data-ttu-id="54ceb-132">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="54ceb-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ceb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54ceb-133">-InputObject</span></span>
<span data-ttu-id="54ceb-134">Paket-objekt</span><span class="sxs-lookup"><span data-stu-id="54ceb-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="54ceb-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="54ceb-135">-InRemovedState</span></span>
<span data-ttu-id="54ceb-136">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="54ceb-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="54ceb-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="54ceb-137">-Name</span></span>
<span data-ttu-id="54ceb-138">Anger namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="54ceb-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="54ceb-139">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="54ceb-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ceb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54ceb-140">-PassThru</span></span>
<span data-ttu-id="54ceb-141">Anger att denna cmdlet returnerar ett **Microsoft. Azure.-kommandon. PSKeyVaultKey..** ..</span><span class="sxs-lookup"><span data-stu-id="54ceb-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="54ceb-142">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="54ceb-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54ceb-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54ceb-143">-VaultName</span></span>
<span data-ttu-id="54ceb-144">Anger namnet på det nyckelord som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="54ceb-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="54ceb-145">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="54ceb-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="54ceb-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54ceb-146">-Confirm</span></span>
<span data-ttu-id="54ceb-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54ceb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ceb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ceb-148">-WhatIf</span></span>
<span data-ttu-id="54ceb-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54ceb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ceb-150">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54ceb-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ceb-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54ceb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ceb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ceb-152">CommonParameters</span></span>
<span data-ttu-id="54ceb-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ceb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ceb-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54ceb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ceb-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54ceb-155">INPUTS</span></span>

### <span data-ttu-id="54ceb-156">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="54ceb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="54ceb-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54ceb-157">OUTPUTS</span></span>

### <span data-ttu-id="54ceb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="54ceb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="54ceb-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54ceb-159">NOTES</span></span>

## <span data-ttu-id="54ceb-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54ceb-160">RELATED LINKS</span></span>

[<span data-ttu-id="54ceb-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="54ceb-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="54ceb-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="54ceb-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="54ceb-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="54ceb-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="54ceb-164">Ångra-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="54ceb-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

