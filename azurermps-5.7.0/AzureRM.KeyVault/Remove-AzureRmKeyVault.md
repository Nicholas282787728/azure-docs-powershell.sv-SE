---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756085"
---
# <span data-ttu-id="b90e9-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="b90e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b90e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b90e9-103">Tar bort ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b90e9-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b90e9-104">SYNTAX</span></span>

### <span data-ttu-id="b90e9-105">ByAvailableVault (standard)</span><span class="sxs-lookup"><span data-stu-id="b90e9-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90e9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b90e9-109">DESCRIPTION</span></span>
<span data-ttu-id="b90e9-110">Cmdleten **Remove-AzureRmKeyVault** tar bort det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="b90e9-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="b90e9-111">Dessutom tas alla nycklar och hemligheter bort i den instansen.</span><span class="sxs-lookup"><span data-stu-id="b90e9-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="b90e9-112">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="b90e9-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="b90e9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b90e9-113">EXAMPLES</span></span>

### <span data-ttu-id="b90e9-114">Exempel 1: ta bort ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="b90e9-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="b90e9-115">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b90e9-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="b90e9-116">Exempel 2: ta bort ett nyckeltal från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b90e9-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="b90e9-117">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b90e9-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="b90e9-118">Om du inte anger namnet på resurs gruppen söker cmdleten efter det namngivna nyckelvärdet att ta bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b90e9-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="b90e9-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b90e9-119">PARAMETERS</span></span>

### <span data-ttu-id="b90e9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b90e9-120">-AsJob</span></span>
<span data-ttu-id="b90e9-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b90e9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b90e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90e9-122">-DefaultProfile</span></span>
<span data-ttu-id="b90e9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b90e9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b90e9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b90e9-124">-Force</span></span>
<span data-ttu-id="b90e9-125">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b90e9-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="b90e9-126">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="b90e9-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="b90e9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b90e9-127">-InputObject</span></span>
<span data-ttu-id="b90e9-128">Key valv-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b90e9-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b90e9-129">-InRemovedState</span></span>
<span data-ttu-id="b90e9-130">Ta bort det tidigare borttagna valvet permanent.</span><span class="sxs-lookup"><span data-stu-id="b90e9-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="b90e9-131">-Location</span></span>
<span data-ttu-id="b90e9-132">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="b90e9-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b90e9-133">-PassThru</span></span>
<span data-ttu-id="b90e9-134">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="b90e9-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b90e9-135">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="b90e9-135">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b90e9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90e9-136">-ResourceGroupName</span></span>
<span data-ttu-id="b90e9-137">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b90e9-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b90e9-138">-VaultName</span></span>
<span data-ttu-id="b90e9-139">Anger namnet på det Key-valv som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b90e9-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b90e9-140">-Confirm</span></span>
<span data-ttu-id="b90e9-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b90e9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90e9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90e9-142">-WhatIf</span></span>
<span data-ttu-id="b90e9-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b90e9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90e9-144">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b90e9-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90e9-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b90e9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90e9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90e9-146">CommonParameters</span></span>
<span data-ttu-id="b90e9-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90e9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90e9-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90e9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90e9-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b90e9-149">INPUTS</span></span>

### <span data-ttu-id="b90e9-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="b90e9-150">None</span></span>
<span data-ttu-id="b90e9-151">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b90e9-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b90e9-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b90e9-152">OUTPUTS</span></span>

### <span data-ttu-id="b90e9-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b90e9-153">System.Boolean</span></span>

## <span data-ttu-id="b90e9-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b90e9-154">NOTES</span></span>

## <span data-ttu-id="b90e9-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b90e9-155">RELATED LINKS</span></span>

[<span data-ttu-id="b90e9-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="b90e9-157">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b90e9-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
