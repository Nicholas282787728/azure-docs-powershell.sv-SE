---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394883"
---
# <span data-ttu-id="1ab18-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1ab18-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="1ab18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ab18-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab18-103">Tar bort en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="1ab18-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="1ab18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ab18-104">SYNTAX</span></span>

### <span data-ttu-id="1ab18-105">RemoveManagedHsmByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1ab18-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab18-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ab18-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab18-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab18-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ab18-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ab18-108">DESCRIPTION</span></span>
<span data-ttu-id="1ab18-109">Cmdleten **Remove-AzKeyVaultManagedHsm** tar bort den angivna hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="1ab18-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="1ab18-110">Alla knappar i den instansen tas bort.</span><span class="sxs-lookup"><span data-stu-id="1ab18-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="1ab18-111">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="1ab18-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="1ab18-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ab18-112">EXAMPLES</span></span>

### <span data-ttu-id="1ab18-113">Exempel 1: ta bort en hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="1ab18-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="1ab18-114">Det här kommandot tar bort den hanterade HSM som heter myhsm från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1ab18-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="1ab18-115">Exempel 2: ta bort en hanterad HSM från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="1ab18-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="1ab18-116">Det här kommandot tar bort den hanterade HSM som heter myhsm från resurs gruppen med namnet myrg1.</span><span class="sxs-lookup"><span data-stu-id="1ab18-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="1ab18-117">Om du inte anger namnet på resurs gruppen söker cmdleten efter den namngivna hanterade HSM som ska tas bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1ab18-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="1ab18-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ab18-118">PARAMETERS</span></span>

### <span data-ttu-id="1ab18-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ab18-119">-AsJob</span></span>
<span data-ttu-id="1ab18-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1ab18-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ab18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab18-121">-DefaultProfile</span></span>
<span data-ttu-id="1ab18-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab18-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ab18-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1ab18-123">-Force</span></span>
<span data-ttu-id="1ab18-124">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1ab18-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="1ab18-125">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort den hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="1ab18-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="1ab18-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ab18-126">-InputObject</span></span>
<span data-ttu-id="1ab18-127">Hanterat HSM-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1ab18-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab18-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ab18-128">-Name</span></span>
<span data-ttu-id="1ab18-129">Anger namnet på den hanterade HSM som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1ab18-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab18-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ab18-130">-PassThru</span></span>
<span data-ttu-id="1ab18-131">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="1ab18-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1ab18-132">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="1ab18-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1ab18-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab18-133">-ResourceGroupName</span></span>
<span data-ttu-id="1ab18-134">Anger namnet på den resurs grupp för Azure Managed HSM som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1ab18-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab18-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab18-135">-ResourceId</span></span>
<span data-ttu-id="1ab18-136">ManagedHsm resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1ab18-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab18-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ab18-137">-Confirm</span></span>
<span data-ttu-id="1ab18-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ab18-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab18-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab18-139">-WhatIf</span></span>
<span data-ttu-id="1ab18-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ab18-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab18-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ab18-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab18-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab18-142">CommonParameters</span></span>
<span data-ttu-id="1ab18-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab18-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab18-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ab18-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab18-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ab18-145">INPUTS</span></span>

### <span data-ttu-id="1ab18-146">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1ab18-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="1ab18-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1ab18-147">System.String</span></span>

## <span data-ttu-id="1ab18-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ab18-148">OUTPUTS</span></span>

### <span data-ttu-id="1ab18-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ab18-149">System.Boolean</span></span>

## <span data-ttu-id="1ab18-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ab18-150">NOTES</span></span>

## <span data-ttu-id="1ab18-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ab18-151">RELATED LINKS</span></span>

[<span data-ttu-id="1ab18-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1ab18-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1ab18-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1ab18-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1ab18-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1ab18-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)