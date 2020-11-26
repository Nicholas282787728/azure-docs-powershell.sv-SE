---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271433"
---
# <span data-ttu-id="4e626-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4e626-101">New-AzResourceLock</span></span>

## <span data-ttu-id="4e626-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e626-102">SYNOPSIS</span></span>
<span data-ttu-id="4e626-103">Skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="4e626-103">Creates a resource lock.</span></span>

## <span data-ttu-id="4e626-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e626-104">SYNTAX</span></span>

### <span data-ttu-id="4e626-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="4e626-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e626-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4e626-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e626-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="4e626-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e626-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="4e626-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e626-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4e626-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e626-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="4e626-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e626-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e626-111">DESCRIPTION</span></span>
<span data-ttu-id="4e626-112">Cmdleten **New-AzResourceLock** skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="4e626-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="4e626-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e626-113">EXAMPLES</span></span>

### <span data-ttu-id="4e626-114">Exempel 1: skapa ett resurs lås på en webbplats</span><span class="sxs-lookup"><span data-stu-id="4e626-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="4e626-115">Det här kommandot skapar ett resurs lås på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="4e626-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="4e626-116">Exempel 2: skapa ett resurs lås på en databas</span><span class="sxs-lookup"><span data-stu-id="4e626-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="4e626-117">Det här kommandot skapar ett resurs lås på en Azure-databas.</span><span class="sxs-lookup"><span data-stu-id="4e626-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="4e626-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e626-118">PARAMETERS</span></span>

### <span data-ttu-id="4e626-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e626-119">-ApiVersion</span></span>
<span data-ttu-id="4e626-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4e626-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4e626-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4e626-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4e626-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e626-122">-DefaultProfile</span></span>
<span data-ttu-id="4e626-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4e626-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e626-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4e626-124">-Force</span></span>
<span data-ttu-id="4e626-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4e626-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e626-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="4e626-126">-LockId</span></span>
<span data-ttu-id="4e626-127">Anger låsets ID.</span><span class="sxs-lookup"><span data-stu-id="4e626-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="4e626-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="4e626-128">-LockLevel</span></span>
<span data-ttu-id="4e626-129">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="4e626-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="4e626-130">För närvarande är giltiga värden CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="4e626-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="4e626-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="4e626-131">-LockName</span></span>
<span data-ttu-id="4e626-132">Anger namnet på låset.</span><span class="sxs-lookup"><span data-stu-id="4e626-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="4e626-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="4e626-133">-LockNotes</span></span>
<span data-ttu-id="4e626-134">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="4e626-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="4e626-135">-För</span><span class="sxs-lookup"><span data-stu-id="4e626-135">-Pre</span></span>
<span data-ttu-id="4e626-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4e626-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4e626-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e626-137">-ResourceGroupName</span></span>
<span data-ttu-id="4e626-138">Anger namnet på en resurs grupp som låset gäller för eller som innehåller den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="4e626-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="4e626-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4e626-139">-ResourceName</span></span>
<span data-ttu-id="4e626-140">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="4e626-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="4e626-141">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4e626-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4e626-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4e626-142">-ResourceType</span></span>
<span data-ttu-id="4e626-143">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="4e626-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="4e626-144">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4e626-144">-Scope</span></span>
<span data-ttu-id="4e626-145">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="4e626-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="4e626-146">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="4e626-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="4e626-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e626-147">-Confirm</span></span>
<span data-ttu-id="4e626-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e626-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e626-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e626-149">-WhatIf</span></span>
<span data-ttu-id="4e626-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e626-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e626-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e626-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e626-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e626-152">CommonParameters</span></span>
<span data-ttu-id="4e626-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e626-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e626-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e626-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e626-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e626-155">INPUTS</span></span>

### <span data-ttu-id="4e626-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4e626-156">System.String</span></span>

### <span data-ttu-id="4e626-157">Microsoft. Azure. commands. ResourceManager. cmdlets. entities. LockLevel</span><span class="sxs-lookup"><span data-stu-id="4e626-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="4e626-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e626-158">OUTPUTS</span></span>

### <span data-ttu-id="4e626-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4e626-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4e626-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e626-160">NOTES</span></span>

## <span data-ttu-id="4e626-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e626-161">RELATED LINKS</span></span>

[<span data-ttu-id="4e626-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4e626-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="4e626-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4e626-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="4e626-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4e626-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)

