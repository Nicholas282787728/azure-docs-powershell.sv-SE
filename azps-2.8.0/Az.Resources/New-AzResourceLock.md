---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920068"
---
# <span data-ttu-id="474cc-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="474cc-101">New-AzResourceLock</span></span>

## <span data-ttu-id="474cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="474cc-102">SYNOPSIS</span></span>
<span data-ttu-id="474cc-103">Skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="474cc-103">Creates a resource lock.</span></span>

## <span data-ttu-id="474cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="474cc-104">SYNTAX</span></span>

### <span data-ttu-id="474cc-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="474cc-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="474cc-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="474cc-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474cc-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474cc-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="474cc-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="474cc-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474cc-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474cc-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="474cc-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="474cc-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="474cc-112">DESCRIPTION</span></span>
<span data-ttu-id="474cc-113">Cmdleten **New-AzResourceLock** skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="474cc-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="474cc-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="474cc-114">EXAMPLES</span></span>

### <span data-ttu-id="474cc-115">Exempel 1: skapa ett resurs lås på en webbplats</span><span class="sxs-lookup"><span data-stu-id="474cc-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="474cc-116">Det här kommandot skapar ett resurs lås på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="474cc-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="474cc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="474cc-117">PARAMETERS</span></span>

### <span data-ttu-id="474cc-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="474cc-118">-ApiVersion</span></span>
<span data-ttu-id="474cc-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="474cc-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="474cc-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="474cc-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="474cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474cc-121">-DefaultProfile</span></span>
<span data-ttu-id="474cc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="474cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="474cc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="474cc-123">-Force</span></span>
<span data-ttu-id="474cc-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="474cc-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="474cc-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="474cc-125">-LockId</span></span>
<span data-ttu-id="474cc-126">Anger låsets ID.</span><span class="sxs-lookup"><span data-stu-id="474cc-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="474cc-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-127">-LockLevel</span></span>
<span data-ttu-id="474cc-128">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="474cc-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="474cc-129">För närvarande är giltiga värden CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="474cc-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="474cc-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="474cc-130">-LockName</span></span>
<span data-ttu-id="474cc-131">Anger namnet på låset.</span><span class="sxs-lookup"><span data-stu-id="474cc-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="474cc-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="474cc-132">-LockNotes</span></span>
<span data-ttu-id="474cc-133">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="474cc-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="474cc-134">-För</span><span class="sxs-lookup"><span data-stu-id="474cc-134">-Pre</span></span>
<span data-ttu-id="474cc-135">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="474cc-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="474cc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474cc-136">-ResourceGroupName</span></span>
<span data-ttu-id="474cc-137">Anger namnet på en resurs grupp som låset gäller för eller som innehåller den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="474cc-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="474cc-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="474cc-138">-ResourceName</span></span>
<span data-ttu-id="474cc-139">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="474cc-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="474cc-140">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="474cc-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="474cc-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="474cc-141">-ResourceType</span></span>
<span data-ttu-id="474cc-142">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="474cc-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="474cc-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="474cc-143">-Scope</span></span>
<span data-ttu-id="474cc-144">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="474cc-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="474cc-145">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="474cc-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="474cc-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-146">-TenantLevel</span></span>
<span data-ttu-id="474cc-147">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="474cc-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="474cc-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="474cc-148">-Confirm</span></span>
<span data-ttu-id="474cc-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="474cc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="474cc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="474cc-150">-WhatIf</span></span>
<span data-ttu-id="474cc-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="474cc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="474cc-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="474cc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="474cc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474cc-153">CommonParameters</span></span>
<span data-ttu-id="474cc-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474cc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474cc-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474cc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474cc-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="474cc-156">INPUTS</span></span>

### <span data-ttu-id="474cc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="474cc-157">System.String</span></span>

### <span data-ttu-id="474cc-158">Microsoft. Azure. commands. ResourceManager. cmdlets. entities. LockLevel</span><span class="sxs-lookup"><span data-stu-id="474cc-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="474cc-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="474cc-159">OUTPUTS</span></span>

### <span data-ttu-id="474cc-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="474cc-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="474cc-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="474cc-161">NOTES</span></span>

## <span data-ttu-id="474cc-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="474cc-162">RELATED LINKS</span></span>

[<span data-ttu-id="474cc-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="474cc-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="474cc-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="474cc-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="474cc-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="474cc-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


