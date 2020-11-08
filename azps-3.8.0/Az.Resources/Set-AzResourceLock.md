---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: 7eea12813681153e6aaa39fba2c514e0b617f636
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089445"
---
# <span data-ttu-id="af5b6-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="af5b6-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="af5b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="af5b6-103">Ändrar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="af5b6-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="af5b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af5b6-104">SYNTAX</span></span>

### <span data-ttu-id="af5b6-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="af5b6-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af5b6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="af5b6-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5b6-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5b6-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="af5b6-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af5b6-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5b6-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5b6-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="af5b6-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af5b6-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af5b6-112">DESCRIPTION</span></span>
<span data-ttu-id="af5b6-113">Cmdleten **set-AzResourceLock** ändrar resurs låset.</span><span class="sxs-lookup"><span data-stu-id="af5b6-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="af5b6-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af5b6-114">EXAMPLES</span></span>

### <span data-ttu-id="af5b6-115">Exempel 1: uppdatera anteckningar för ett lås</span><span class="sxs-lookup"><span data-stu-id="af5b6-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="af5b6-116">Det här kommandot uppdaterar anteckningen för ett lås med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="af5b6-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="af5b6-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af5b6-117">PARAMETERS</span></span>

### <span data-ttu-id="af5b6-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af5b6-118">-ApiVersion</span></span>
<span data-ttu-id="af5b6-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="af5b6-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="af5b6-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="af5b6-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="af5b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5b6-121">-DefaultProfile</span></span>
<span data-ttu-id="af5b6-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af5b6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af5b6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="af5b6-123">-Force</span></span>
<span data-ttu-id="af5b6-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af5b6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af5b6-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="af5b6-125">-LockId</span></span>
<span data-ttu-id="af5b6-126">Anger det lås som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="af5b6-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="af5b6-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-127">-LockLevel</span></span>
<span data-ttu-id="af5b6-128">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="af5b6-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="af5b6-129">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="af5b6-129">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5b6-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="af5b6-130">-LockName</span></span>
<span data-ttu-id="af5b6-131">Anger namnet på det lås som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="af5b6-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5b6-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="af5b6-132">-LockNotes</span></span>
<span data-ttu-id="af5b6-133">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="af5b6-133">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5b6-134">-För</span><span class="sxs-lookup"><span data-stu-id="af5b6-134">-Pre</span></span>
<span data-ttu-id="af5b6-135">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="af5b6-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="af5b6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5b6-136">-ResourceGroupName</span></span>
<span data-ttu-id="af5b6-137">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af5b6-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="af5b6-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="af5b6-138">-ResourceName</span></span>
<span data-ttu-id="af5b6-139">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af5b6-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="af5b6-140">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="af5b6-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="af5b6-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="af5b6-141">-ResourceType</span></span>
<span data-ttu-id="af5b6-142">Anger den resurs typ som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af5b6-142">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="af5b6-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="af5b6-143">-Scope</span></span>
<span data-ttu-id="af5b6-144">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af5b6-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="af5b6-145">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="af5b6-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="af5b6-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-146">-TenantLevel</span></span>
<span data-ttu-id="af5b6-147">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="af5b6-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="af5b6-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af5b6-148">-Confirm</span></span>
<span data-ttu-id="af5b6-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af5b6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5b6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5b6-150">-WhatIf</span></span>
<span data-ttu-id="af5b6-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af5b6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af5b6-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af5b6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5b6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5b6-153">CommonParameters</span></span>
<span data-ttu-id="af5b6-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af5b6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5b6-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af5b6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5b6-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af5b6-156">INPUTS</span></span>

### <span data-ttu-id="af5b6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="af5b6-157">System.String</span></span>

### <span data-ttu-id="af5b6-158">Microsoft. Azure. commands. ResourceManager. cmdlets. entities. LockLevel</span><span class="sxs-lookup"><span data-stu-id="af5b6-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="af5b6-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af5b6-159">OUTPUTS</span></span>

### <span data-ttu-id="af5b6-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="af5b6-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="af5b6-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af5b6-161">NOTES</span></span>

## <span data-ttu-id="af5b6-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af5b6-162">RELATED LINKS</span></span>

[<span data-ttu-id="af5b6-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="af5b6-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="af5b6-164">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="af5b6-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="af5b6-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="af5b6-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


