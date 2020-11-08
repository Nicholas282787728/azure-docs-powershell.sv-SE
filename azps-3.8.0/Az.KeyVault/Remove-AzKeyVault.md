---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 32060f2d9d468669f963f653f335729ca6c25761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092606"
---
# <span data-ttu-id="50fae-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="50fae-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="50fae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50fae-102">SYNOPSIS</span></span>
<span data-ttu-id="50fae-103">Tar bort ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="50fae-103">Deletes a key vault.</span></span>

## <span data-ttu-id="50fae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50fae-104">SYNTAX</span></span>

### <span data-ttu-id="50fae-105">ByAvailableVault (standard)</span><span class="sxs-lookup"><span data-stu-id="50fae-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fae-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="50fae-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fae-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="50fae-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fae-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="50fae-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fae-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="50fae-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fae-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="50fae-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50fae-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50fae-111">DESCRIPTION</span></span>
<span data-ttu-id="50fae-112">Cmdleten **Remove-AzKeyVault** tar bort det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="50fae-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="50fae-113">Dessutom tas alla nycklar och hemligheter bort i den instansen.</span><span class="sxs-lookup"><span data-stu-id="50fae-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="50fae-114">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="50fae-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="50fae-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50fae-115">EXAMPLES</span></span>

### <span data-ttu-id="50fae-116">Exempel 1: ta bort ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="50fae-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="50fae-117">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="50fae-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="50fae-118">Exempel 2: ta bort ett nyckeltal från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="50fae-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="50fae-119">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="50fae-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="50fae-120">Om du inte anger namnet på resurs gruppen söker cmdleten efter det namngivna nyckelvärdet att ta bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="50fae-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="50fae-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50fae-121">PARAMETERS</span></span>

### <span data-ttu-id="50fae-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50fae-122">-AsJob</span></span>
<span data-ttu-id="50fae-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50fae-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50fae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fae-124">-DefaultProfile</span></span>
<span data-ttu-id="50fae-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50fae-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50fae-126">-Force</span><span class="sxs-lookup"><span data-stu-id="50fae-126">-Force</span></span>
<span data-ttu-id="50fae-127">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="50fae-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="50fae-128">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="50fae-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="50fae-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50fae-129">-InputObject</span></span>
<span data-ttu-id="50fae-130">Key valv-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="50fae-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="50fae-131">-InRemovedState</span></span>
<span data-ttu-id="50fae-132">Ta bort det tidigare borttagna valvet permanent.</span><span class="sxs-lookup"><span data-stu-id="50fae-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="50fae-133">-Location</span></span>
<span data-ttu-id="50fae-134">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="50fae-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50fae-135">-PassThru</span></span>
<span data-ttu-id="50fae-136">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="50fae-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="50fae-137">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="50fae-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="50fae-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50fae-138">-ResourceGroupName</span></span>
<span data-ttu-id="50fae-139">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="50fae-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50fae-140">-ResourceId</span></span>
<span data-ttu-id="50fae-141">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="50fae-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="50fae-142">-VaultName</span></span>
<span data-ttu-id="50fae-143">Anger namnet på det Key-valv som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="50fae-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50fae-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50fae-144">-Confirm</span></span>
<span data-ttu-id="50fae-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50fae-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fae-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fae-146">-WhatIf</span></span>
<span data-ttu-id="50fae-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50fae-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fae-148">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50fae-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fae-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50fae-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fae-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fae-150">CommonParameters</span></span>
<span data-ttu-id="50fae-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fae-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fae-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50fae-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fae-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50fae-153">INPUTS</span></span>

### <span data-ttu-id="50fae-154">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="50fae-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="50fae-155">System. String</span><span class="sxs-lookup"><span data-stu-id="50fae-155">System.String</span></span>

## <span data-ttu-id="50fae-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50fae-156">OUTPUTS</span></span>

### <span data-ttu-id="50fae-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50fae-157">System.Boolean</span></span>

## <span data-ttu-id="50fae-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50fae-158">NOTES</span></span>

## <span data-ttu-id="50fae-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50fae-159">RELATED LINKS</span></span>

[<span data-ttu-id="50fae-160">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="50fae-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="50fae-161">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="50fae-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
