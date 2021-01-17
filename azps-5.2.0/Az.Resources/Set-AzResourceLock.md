---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405587"
---
# <span data-ttu-id="26cb2-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26cb2-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="26cb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="26cb2-103">Ändrar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="26cb2-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="26cb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26cb2-104">SYNTAX</span></span>

### <span data-ttu-id="26cb2-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="26cb2-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26cb2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26cb2-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26cb2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="26cb2-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26cb2-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="26cb2-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26cb2-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="26cb2-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26cb2-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="26cb2-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26cb2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26cb2-111">DESCRIPTION</span></span>
<span data-ttu-id="26cb2-112">Cmdleten **set-AzResourceLock** ändrar resurs låset.</span><span class="sxs-lookup"><span data-stu-id="26cb2-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="26cb2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26cb2-113">EXAMPLES</span></span>

### <span data-ttu-id="26cb2-114">Exempel 1: uppdatera anteckningar för ett lås</span><span class="sxs-lookup"><span data-stu-id="26cb2-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="26cb2-115">Det här kommandot uppdaterar anteckningen för ett lås med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="26cb2-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="26cb2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26cb2-116">PARAMETERS</span></span>

### <span data-ttu-id="26cb2-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26cb2-117">-ApiVersion</span></span>
<span data-ttu-id="26cb2-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="26cb2-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="26cb2-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="26cb2-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="26cb2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cb2-120">-DefaultProfile</span></span>
<span data-ttu-id="26cb2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26cb2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26cb2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="26cb2-122">-Force</span></span>
<span data-ttu-id="26cb2-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="26cb2-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26cb2-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="26cb2-124">-LockId</span></span>
<span data-ttu-id="26cb2-125">Anger det lås som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="26cb2-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="26cb2-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="26cb2-126">-LockLevel</span></span>
<span data-ttu-id="26cb2-127">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="26cb2-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="26cb2-128">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="26cb2-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="26cb2-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="26cb2-129">-LockName</span></span>
<span data-ttu-id="26cb2-130">Anger namnet på det lås som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="26cb2-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cb2-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="26cb2-131">-LockNotes</span></span>
<span data-ttu-id="26cb2-132">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="26cb2-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="26cb2-133">-För</span><span class="sxs-lookup"><span data-stu-id="26cb2-133">-Pre</span></span>
<span data-ttu-id="26cb2-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="26cb2-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26cb2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26cb2-135">-ResourceGroupName</span></span>
<span data-ttu-id="26cb2-136">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="26cb2-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="26cb2-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="26cb2-137">-ResourceName</span></span>
<span data-ttu-id="26cb2-138">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="26cb2-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="26cb2-139">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="26cb2-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="26cb2-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="26cb2-140">-ResourceType</span></span>
<span data-ttu-id="26cb2-141">Anger den resurs typ som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="26cb2-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="26cb2-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="26cb2-142">-Scope</span></span>
<span data-ttu-id="26cb2-143">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="26cb2-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="26cb2-144">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="26cb2-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="26cb2-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26cb2-145">-Confirm</span></span>
<span data-ttu-id="26cb2-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26cb2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26cb2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26cb2-147">-WhatIf</span></span>
<span data-ttu-id="26cb2-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26cb2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26cb2-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26cb2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26cb2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cb2-150">CommonParameters</span></span>
<span data-ttu-id="26cb2-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26cb2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cb2-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26cb2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26cb2-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26cb2-153">INPUTS</span></span>

### <span data-ttu-id="26cb2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="26cb2-154">System.String</span></span>

### <span data-ttu-id="26cb2-155">Microsoft. Azure. commands. ResourceManager. cmdlets. entities. LockLevel</span><span class="sxs-lookup"><span data-stu-id="26cb2-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="26cb2-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26cb2-156">OUTPUTS</span></span>

### <span data-ttu-id="26cb2-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="26cb2-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="26cb2-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26cb2-158">NOTES</span></span>

## <span data-ttu-id="26cb2-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26cb2-159">RELATED LINKS</span></span>

[<span data-ttu-id="26cb2-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26cb2-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="26cb2-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26cb2-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="26cb2-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="26cb2-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


