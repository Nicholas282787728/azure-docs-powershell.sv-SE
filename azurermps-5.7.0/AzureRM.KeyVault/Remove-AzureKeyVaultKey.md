---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576500"
---
# <span data-ttu-id="575e2-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575e2-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="575e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="575e2-102">SYNOPSIS</span></span>
<span data-ttu-id="575e2-103">Tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="575e2-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="575e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="575e2-104">SYNTAX</span></span>

### <span data-ttu-id="575e2-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="575e2-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="575e2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="575e2-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="575e2-107">DESCRIPTION</span></span>
<span data-ttu-id="575e2-108">Remove-AzureKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="575e2-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="575e2-109">Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzureKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="575e2-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="575e2-110">Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="575e2-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="575e2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="575e2-111">EXAMPLES</span></span>

### <span data-ttu-id="575e2-112">Exempel 1: ta bort en Key från ett nyckelord</span><span class="sxs-lookup"><span data-stu-id="575e2-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="575e2-113">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="575e2-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="575e2-114">Exempel 2: ta bort en nycklar utan användar bekräftelse</span><span class="sxs-lookup"><span data-stu-id="575e2-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="575e2-115">Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.</span><span class="sxs-lookup"><span data-stu-id="575e2-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="575e2-116">Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="575e2-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="575e2-117">Exempel 3: ta bort en borttagen Key från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="575e2-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="575e2-118">Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.</span><span class="sxs-lookup"><span data-stu-id="575e2-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="575e2-119">För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="575e2-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="575e2-120">Exempel 4: ta bort tangenter med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="575e2-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="575e2-121">Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="575e2-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="575e2-122">Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="575e2-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="575e2-123">Dessa nycklar tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575e2-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="575e2-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="575e2-124">PARAMETERS</span></span>

### <span data-ttu-id="575e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575e2-125">-DefaultProfile</span></span>
<span data-ttu-id="575e2-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="575e2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="575e2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="575e2-127">-Force</span></span>
<span data-ttu-id="575e2-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="575e2-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="575e2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="575e2-129">-InputObject</span></span>
<span data-ttu-id="575e2-130">Paket-objekt</span><span class="sxs-lookup"><span data-stu-id="575e2-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="575e2-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="575e2-131">-InRemovedState</span></span>
<span data-ttu-id="575e2-132">Ta bort den tidigare borttagna knappen permanent.</span><span class="sxs-lookup"><span data-stu-id="575e2-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="575e2-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="575e2-133">-Name</span></span>
<span data-ttu-id="575e2-134">Anger namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="575e2-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="575e2-135">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="575e2-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575e2-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="575e2-136">-PassThru</span></span>
<span data-ttu-id="575e2-137">Anger att denna cmdlet returnerar ett **Microsoft. Azure. commands. valv** .-objekt för paket.</span><span class="sxs-lookup"><span data-stu-id="575e2-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="575e2-138">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="575e2-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="575e2-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="575e2-139">-VaultName</span></span>
<span data-ttu-id="575e2-140">Anger namnet på det nyckelord som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="575e2-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="575e2-141">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="575e2-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575e2-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="575e2-142">-Confirm</span></span>
<span data-ttu-id="575e2-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="575e2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="575e2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575e2-144">-WhatIf</span></span>
<span data-ttu-id="575e2-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="575e2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575e2-146">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="575e2-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575e2-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="575e2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="575e2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575e2-148">CommonParameters</span></span>
<span data-ttu-id="575e2-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575e2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575e2-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575e2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575e2-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="575e2-151">INPUTS</span></span>

### <span data-ttu-id="575e2-152">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="575e2-152">String</span></span>

## <span data-ttu-id="575e2-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="575e2-153">OUTPUTS</span></span>

### <span data-ttu-id="575e2-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575e2-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="575e2-155">Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .</span><span class="sxs-lookup"><span data-stu-id="575e2-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="575e2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="575e2-156">NOTES</span></span>

## <span data-ttu-id="575e2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="575e2-157">RELATED LINKS</span></span>

[<span data-ttu-id="575e2-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575e2-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="575e2-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575e2-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="575e2-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="575e2-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="575e2-161">Ångra-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="575e2-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

