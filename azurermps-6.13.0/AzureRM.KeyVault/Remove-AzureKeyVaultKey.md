---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: ff7e5a02899d806633e485f06f419a6f1f2082a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578008"
---
# <span data-ttu-id="98331-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98331-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="98331-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98331-102">SYNOPSIS</span></span>
<span data-ttu-id="98331-103">Tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="98331-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98331-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98331-104">SYNTAX</span></span>

### <span data-ttu-id="98331-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="98331-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98331-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98331-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98331-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98331-107">DESCRIPTION</span></span>
<span data-ttu-id="98331-108">Remove-AzureKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="98331-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="98331-109">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzureKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="98331-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="98331-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="98331-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="98331-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98331-111">EXAMPLES</span></span>

### <span data-ttu-id="98331-112">Exempel 1: ta bort en Key från ett nyckelord</span><span class="sxs-lookup"><span data-stu-id="98331-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

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

<span data-ttu-id="98331-113">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="98331-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="98331-114">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="98331-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="98331-115">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="98331-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="98331-116">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="98331-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="98331-117">Exempel 3: ta bort en borttagen Key från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="98331-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="98331-118">Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="98331-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="98331-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="98331-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="98331-120">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="98331-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="98331-121">Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="98331-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="98331-122">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98331-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="98331-123">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98331-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="98331-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98331-124">PARAMETERS</span></span>

### <span data-ttu-id="98331-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98331-125">-DefaultProfile</span></span>
<span data-ttu-id="98331-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="98331-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98331-127">-Force</span><span class="sxs-lookup"><span data-stu-id="98331-127">-Force</span></span>
<span data-ttu-id="98331-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="98331-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98331-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98331-129">-InputObject</span></span>
<span data-ttu-id="98331-130">Paket-objekt</span><span class="sxs-lookup"><span data-stu-id="98331-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="98331-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98331-131">-InRemovedState</span></span>
<span data-ttu-id="98331-132">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="98331-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="98331-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="98331-133">-Name</span></span>
<span data-ttu-id="98331-134">Anger namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="98331-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="98331-135">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="98331-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="98331-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98331-136">-PassThru</span></span>
<span data-ttu-id="98331-137">Anger att denna cmdlet returnerar ett **Microsoft. Azure.-kommandon. PSKeyVaultKey..** ..</span><span class="sxs-lookup"><span data-stu-id="98331-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="98331-138">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="98331-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98331-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98331-139">-VaultName</span></span>
<span data-ttu-id="98331-140">Anger namnet på det nyckelord som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="98331-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="98331-141">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="98331-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="98331-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98331-142">-Confirm</span></span>
<span data-ttu-id="98331-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98331-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98331-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98331-144">-WhatIf</span></span>
<span data-ttu-id="98331-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98331-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98331-146">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98331-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98331-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98331-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98331-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98331-148">CommonParameters</span></span>
<span data-ttu-id="98331-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98331-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98331-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98331-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98331-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98331-151">INPUTS</span></span>

### <span data-ttu-id="98331-152">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98331-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="98331-153">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98331-153">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="98331-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98331-154">OUTPUTS</span></span>

### <span data-ttu-id="98331-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98331-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="98331-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98331-156">NOTES</span></span>

## <span data-ttu-id="98331-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98331-157">RELATED LINKS</span></span>

[<span data-ttu-id="98331-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98331-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="98331-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98331-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="98331-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="98331-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="98331-161">Ångra-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="98331-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

