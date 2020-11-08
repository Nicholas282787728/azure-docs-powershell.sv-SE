---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: ba740004f22eef1f574d861c44de7e26c7f4594b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089479"
---
# <span data-ttu-id="0f6fa-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0f6fa-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="0f6fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6fa-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-103">Removes a resource lock.</span></span>

## <span data-ttu-id="0f6fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f6fa-104">SYNTAX</span></span>

### <span data-ttu-id="0f6fa-105">ByLockId (standard)</span><span class="sxs-lookup"><span data-stu-id="0f6fa-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0f6fa-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0f6fa-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0f6fa-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0f6fa-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0f6fa-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f6fa-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0f6fa-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f6fa-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f6fa-112">DESCRIPTION</span></span>
<span data-ttu-id="0f6fa-113">Cmdleten **Remove-AzResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="0f6fa-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f6fa-114">EXAMPLES</span></span>

### <span data-ttu-id="0f6fa-115">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="0f6fa-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="0f6fa-116">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0f6fa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f6fa-117">PARAMETERS</span></span>

### <span data-ttu-id="0f6fa-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f6fa-118">-ApiVersion</span></span>
<span data-ttu-id="0f6fa-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0f6fa-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0f6fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6fa-121">-DefaultProfile</span></span>
<span data-ttu-id="0f6fa-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0f6fa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f6fa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0f6fa-123">-Force</span></span>
<span data-ttu-id="0f6fa-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f6fa-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="0f6fa-125">-LockId</span></span>
<span data-ttu-id="0f6fa-126">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f6fa-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="0f6fa-127">-LockName</span></span>
<span data-ttu-id="0f6fa-128">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fa-129">-För</span><span class="sxs-lookup"><span data-stu-id="0f6fa-129">-Pre</span></span>
<span data-ttu-id="0f6fa-130">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0f6fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f6fa-132">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="0f6fa-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0f6fa-133">-ResourceName</span></span>
<span data-ttu-id="0f6fa-134">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="0f6fa-135">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="0f6fa-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fa-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0f6fa-136">-ResourceType</span></span>
<span data-ttu-id="0f6fa-137">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-137">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fa-138">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0f6fa-138">-Scope</span></span>
<span data-ttu-id="0f6fa-139">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="0f6fa-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0f6fa-140">-TenantLevel</span></span>
<span data-ttu-id="0f6fa-141">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-141">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fa-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f6fa-142">-Confirm</span></span>
<span data-ttu-id="0f6fa-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6fa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6fa-144">-WhatIf</span></span>
<span data-ttu-id="0f6fa-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6fa-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6fa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6fa-147">CommonParameters</span></span>
<span data-ttu-id="0f6fa-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6fa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6fa-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f6fa-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6fa-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f6fa-150">INPUTS</span></span>

### <span data-ttu-id="0f6fa-151">System. String</span><span class="sxs-lookup"><span data-stu-id="0f6fa-151">System.String</span></span>

## <span data-ttu-id="0f6fa-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f6fa-152">OUTPUTS</span></span>

### <span data-ttu-id="0f6fa-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0f6fa-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0f6fa-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f6fa-154">NOTES</span></span>

## <span data-ttu-id="0f6fa-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f6fa-155">RELATED LINKS</span></span>

[<span data-ttu-id="0f6fa-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0f6fa-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="0f6fa-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0f6fa-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="0f6fa-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0f6fa-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


