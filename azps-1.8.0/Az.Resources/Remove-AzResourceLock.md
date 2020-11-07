---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747057"
---
# <span data-ttu-id="bf908-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bf908-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="bf908-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf908-102">SYNOPSIS</span></span>
<span data-ttu-id="bf908-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="bf908-103">Removes a resource lock.</span></span>

## <span data-ttu-id="bf908-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf908-104">SYNTAX</span></span>

### <span data-ttu-id="bf908-105">ByLockId (standard)</span><span class="sxs-lookup"><span data-stu-id="bf908-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf908-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf908-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf908-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bf908-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf908-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bf908-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf908-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bf908-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf908-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bf908-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf908-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bf908-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf908-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf908-112">DESCRIPTION</span></span>
<span data-ttu-id="bf908-113">Cmdleten **Remove-AzResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="bf908-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="bf908-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf908-114">EXAMPLES</span></span>

### <span data-ttu-id="bf908-115">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="bf908-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="bf908-116">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="bf908-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bf908-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf908-117">PARAMETERS</span></span>

### <span data-ttu-id="bf908-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bf908-118">-ApiVersion</span></span>
<span data-ttu-id="bf908-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bf908-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bf908-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="bf908-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bf908-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf908-121">-DefaultProfile</span></span>
<span data-ttu-id="bf908-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf908-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf908-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bf908-123">-Force</span></span>
<span data-ttu-id="bf908-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bf908-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf908-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="bf908-125">-LockId</span></span>
<span data-ttu-id="bf908-126">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf908-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf908-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="bf908-127">-LockName</span></span>
<span data-ttu-id="bf908-128">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="bf908-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf908-129">-För</span><span class="sxs-lookup"><span data-stu-id="bf908-129">-Pre</span></span>
<span data-ttu-id="bf908-130">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bf908-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bf908-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf908-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf908-132">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bf908-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="bf908-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bf908-133">-ResourceName</span></span>
<span data-ttu-id="bf908-134">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bf908-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bf908-135">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="bf908-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="bf908-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bf908-136">-ResourceType</span></span>
<span data-ttu-id="bf908-137">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bf908-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="bf908-138">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="bf908-138">-Scope</span></span>
<span data-ttu-id="bf908-139">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bf908-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="bf908-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bf908-140">-TenantLevel</span></span>
<span data-ttu-id="bf908-141">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="bf908-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="bf908-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf908-142">-Confirm</span></span>
<span data-ttu-id="bf908-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf908-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf908-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf908-144">-WhatIf</span></span>
<span data-ttu-id="bf908-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf908-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf908-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf908-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf908-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf908-147">CommonParameters</span></span>
<span data-ttu-id="bf908-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf908-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf908-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf908-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf908-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf908-150">INPUTS</span></span>

### <span data-ttu-id="bf908-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bf908-151">System.String</span></span>

## <span data-ttu-id="bf908-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf908-152">OUTPUTS</span></span>

### <span data-ttu-id="bf908-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bf908-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bf908-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf908-154">NOTES</span></span>

## <span data-ttu-id="bf908-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf908-155">RELATED LINKS</span></span>

[<span data-ttu-id="bf908-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bf908-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="bf908-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bf908-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="bf908-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bf908-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


