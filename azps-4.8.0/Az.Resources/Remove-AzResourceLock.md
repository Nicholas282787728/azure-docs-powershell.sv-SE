---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 8ad1a2ace4978b12210e568fb944568f5a2fec77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258669"
---
# <span data-ttu-id="77153-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77153-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="77153-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77153-102">SYNOPSIS</span></span>
<span data-ttu-id="77153-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="77153-103">Removes a resource lock.</span></span>

## <span data-ttu-id="77153-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77153-104">SYNTAX</span></span>

### <span data-ttu-id="77153-105">ByLockId (standard)</span><span class="sxs-lookup"><span data-stu-id="77153-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77153-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77153-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77153-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="77153-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77153-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="77153-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77153-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="77153-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77153-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="77153-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77153-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77153-111">DESCRIPTION</span></span>
<span data-ttu-id="77153-112">Cmdleten **Remove-AzResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="77153-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="77153-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77153-113">EXAMPLES</span></span>

### <span data-ttu-id="77153-114">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="77153-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="77153-115">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="77153-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="77153-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="77153-116">Example 2</span></span>

<span data-ttu-id="77153-117">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="77153-117">Removes a resource lock.</span></span> <span data-ttu-id="77153-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="77153-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="77153-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77153-119">PARAMETERS</span></span>

### <span data-ttu-id="77153-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="77153-120">-ApiVersion</span></span>
<span data-ttu-id="77153-121">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="77153-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="77153-122">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="77153-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77153-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77153-123">-DefaultProfile</span></span>
<span data-ttu-id="77153-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="77153-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77153-125">-Force</span><span class="sxs-lookup"><span data-stu-id="77153-125">-Force</span></span>
<span data-ttu-id="77153-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="77153-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77153-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="77153-127">-LockId</span></span>
<span data-ttu-id="77153-128">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77153-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="77153-129">-LockName</span></span>
<span data-ttu-id="77153-130">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="77153-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-131">-För</span><span class="sxs-lookup"><span data-stu-id="77153-131">-Pre</span></span>
<span data-ttu-id="77153-132">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="77153-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="77153-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77153-133">-ResourceGroupName</span></span>
<span data-ttu-id="77153-134">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="77153-134">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="77153-135">-ResourceName</span></span>
<span data-ttu-id="77153-136">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="77153-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="77153-137">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="77153-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="77153-138">-ResourceType</span></span>
<span data-ttu-id="77153-139">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="77153-139">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-140">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="77153-140">-Scope</span></span>
<span data-ttu-id="77153-141">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="77153-141">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77153-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77153-142">-Confirm</span></span>
<span data-ttu-id="77153-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77153-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77153-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77153-144">-WhatIf</span></span>
<span data-ttu-id="77153-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77153-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77153-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77153-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77153-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77153-147">CommonParameters</span></span>
<span data-ttu-id="77153-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77153-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77153-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77153-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77153-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77153-150">INPUTS</span></span>

### <span data-ttu-id="77153-151">System. String</span><span class="sxs-lookup"><span data-stu-id="77153-151">System.String</span></span>

## <span data-ttu-id="77153-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77153-152">OUTPUTS</span></span>

### <span data-ttu-id="77153-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="77153-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="77153-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77153-154">NOTES</span></span>

## <span data-ttu-id="77153-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77153-155">RELATED LINKS</span></span>

[<span data-ttu-id="77153-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77153-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="77153-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77153-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="77153-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="77153-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)

