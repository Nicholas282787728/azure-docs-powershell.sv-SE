---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: c91bc951ef06f2e591893f0959120cac3700b070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576961"
---
# <span data-ttu-id="0f174-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0f174-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="0f174-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f174-102">SYNOPSIS</span></span>
<span data-ttu-id="0f174-103">Tar bort ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="0f174-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f174-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f174-104">SYNTAX</span></span>

### <span data-ttu-id="0f174-105">ByAvailableVault (standard)</span><span class="sxs-lookup"><span data-stu-id="0f174-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f174-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="0f174-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f174-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="0f174-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f174-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="0f174-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f174-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="0f174-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f174-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="0f174-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f174-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f174-111">DESCRIPTION</span></span>
<span data-ttu-id="0f174-112">Cmdleten **Remove-AzureRmKeyVault** tar bort det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="0f174-112">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="0f174-113">Dessutom tas alla nycklar och hemligheter bort i den instansen.</span><span class="sxs-lookup"><span data-stu-id="0f174-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="0f174-114">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="0f174-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="0f174-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f174-115">EXAMPLES</span></span>

### <span data-ttu-id="0f174-116">Exempel 1: ta bort ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="0f174-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="0f174-117">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0f174-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="0f174-118">Exempel 2: ta bort ett nyckeltal från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0f174-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="0f174-119">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0f174-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="0f174-120">Om du inte anger namnet på resurs gruppen söker cmdleten efter det namngivna nyckelvärdet att ta bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0f174-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="0f174-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f174-121">PARAMETERS</span></span>

### <span data-ttu-id="0f174-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f174-122">-AsJob</span></span>
<span data-ttu-id="0f174-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0f174-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f174-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f174-124">-DefaultProfile</span></span>
<span data-ttu-id="0f174-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0f174-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f174-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0f174-126">-Force</span></span>
<span data-ttu-id="0f174-127">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0f174-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="0f174-128">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="0f174-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="0f174-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f174-129">-InputObject</span></span>
<span data-ttu-id="0f174-130">Key valv-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0f174-130">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="0f174-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0f174-131">-InRemovedState</span></span>
<span data-ttu-id="0f174-132">Ta bort det tidigare borttagna valvet permanent.</span><span class="sxs-lookup"><span data-stu-id="0f174-132">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="0f174-133">-Plats</span><span class="sxs-lookup"><span data-stu-id="0f174-133">-Location</span></span>
<span data-ttu-id="0f174-134">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="0f174-134">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="0f174-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f174-135">-PassThru</span></span>
<span data-ttu-id="0f174-136">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="0f174-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0f174-137">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="0f174-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0f174-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f174-138">-ResourceGroupName</span></span>
<span data-ttu-id="0f174-139">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0f174-139">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0f174-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f174-140">-ResourceId</span></span>
<span data-ttu-id="0f174-141">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="0f174-141">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0f174-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f174-142">-VaultName</span></span>
<span data-ttu-id="0f174-143">Anger namnet på det Key-valv som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0f174-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f174-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f174-144">-Confirm</span></span>
<span data-ttu-id="0f174-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f174-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f174-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f174-146">-WhatIf</span></span>
<span data-ttu-id="0f174-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f174-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f174-148">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f174-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f174-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f174-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f174-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f174-150">CommonParameters</span></span>
<span data-ttu-id="0f174-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f174-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f174-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f174-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f174-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f174-153">INPUTS</span></span>

### <span data-ttu-id="0f174-154">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0f174-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="0f174-155">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f174-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0f174-156">System. String</span><span class="sxs-lookup"><span data-stu-id="0f174-156">System.String</span></span>

## <span data-ttu-id="0f174-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f174-157">OUTPUTS</span></span>

### <span data-ttu-id="0f174-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f174-158">System.Boolean</span></span>

## <span data-ttu-id="0f174-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f174-159">NOTES</span></span>

## <span data-ttu-id="0f174-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f174-160">RELATED LINKS</span></span>

[<span data-ttu-id="0f174-161">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0f174-161">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="0f174-162">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0f174-162">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
