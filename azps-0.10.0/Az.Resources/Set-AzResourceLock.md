---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923761"
---
# <span data-ttu-id="53a99-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53a99-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="53a99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53a99-102">SYNOPSIS</span></span>
<span data-ttu-id="53a99-103">Ändrar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="53a99-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="53a99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53a99-104">SYNTAX</span></span>

### <span data-ttu-id="53a99-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="53a99-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53a99-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53a99-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53a99-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="53a99-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a99-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="53a99-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53a99-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="53a99-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a99-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="53a99-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a99-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="53a99-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53a99-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53a99-112">DESCRIPTION</span></span>
<span data-ttu-id="53a99-113">Cmdleten **set-AzResourceLock** ändrar resurs låset.</span><span class="sxs-lookup"><span data-stu-id="53a99-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="53a99-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53a99-114">EXAMPLES</span></span>

### <span data-ttu-id="53a99-115">Exempel 1: uppdatera anteckningar för ett lås</span><span class="sxs-lookup"><span data-stu-id="53a99-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="53a99-116">Det här kommandot uppdaterar anteckningen för ett lås med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="53a99-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="53a99-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53a99-117">PARAMETERS</span></span>

### <span data-ttu-id="53a99-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53a99-118">-ApiVersion</span></span>
<span data-ttu-id="53a99-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="53a99-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="53a99-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="53a99-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="53a99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a99-121">-DefaultProfile</span></span>
<span data-ttu-id="53a99-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="53a99-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a99-123">-Force</span><span class="sxs-lookup"><span data-stu-id="53a99-123">-Force</span></span>
<span data-ttu-id="53a99-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="53a99-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53a99-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="53a99-125">-InformationAction</span></span>
<span data-ttu-id="53a99-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="53a99-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="53a99-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53a99-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53a99-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="53a99-128">Continue</span></span>
- <span data-ttu-id="53a99-129">Över</span><span class="sxs-lookup"><span data-stu-id="53a99-129">Ignore</span></span>
- <span data-ttu-id="53a99-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="53a99-130">Inquire</span></span>
- <span data-ttu-id="53a99-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="53a99-131">SilentlyContinue</span></span>
- <span data-ttu-id="53a99-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="53a99-132">Stop</span></span>
- <span data-ttu-id="53a99-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="53a99-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a99-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="53a99-134">-InformationVariable</span></span>
<span data-ttu-id="53a99-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="53a99-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a99-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="53a99-136">-LockId</span></span>
<span data-ttu-id="53a99-137">Anger det lås som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="53a99-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53a99-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="53a99-138">-LockLevel</span></span>
<span data-ttu-id="53a99-139">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="53a99-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="53a99-140">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="53a99-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a99-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="53a99-141">-LockName</span></span>
<span data-ttu-id="53a99-142">Anger namnet på det lås som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="53a99-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53a99-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="53a99-143">-LockNotes</span></span>
<span data-ttu-id="53a99-144">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="53a99-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="53a99-145">-För</span><span class="sxs-lookup"><span data-stu-id="53a99-145">-Pre</span></span>
<span data-ttu-id="53a99-146">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="53a99-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53a99-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a99-147">-ResourceGroupName</span></span>
<span data-ttu-id="53a99-148">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="53a99-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="53a99-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="53a99-149">-ResourceName</span></span>
<span data-ttu-id="53a99-150">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="53a99-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="53a99-151">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="53a99-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="53a99-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="53a99-152">-ResourceType</span></span>
<span data-ttu-id="53a99-153">Anger den resurs typ som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="53a99-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="53a99-154">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="53a99-154">-Scope</span></span>
<span data-ttu-id="53a99-155">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="53a99-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="53a99-156">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="53a99-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="53a99-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="53a99-157">-TenantLevel</span></span>
<span data-ttu-id="53a99-158">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="53a99-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="53a99-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53a99-159">-Confirm</span></span>
<span data-ttu-id="53a99-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53a99-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a99-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a99-161">-WhatIf</span></span>
<span data-ttu-id="53a99-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53a99-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a99-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53a99-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a99-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a99-164">CommonParameters</span></span>
<span data-ttu-id="53a99-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a99-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a99-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a99-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a99-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53a99-167">INPUTS</span></span>

## <span data-ttu-id="53a99-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53a99-168">OUTPUTS</span></span>

## <span data-ttu-id="53a99-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53a99-169">NOTES</span></span>

## <span data-ttu-id="53a99-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53a99-170">RELATED LINKS</span></span>

[<span data-ttu-id="53a99-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53a99-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="53a99-172">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53a99-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="53a99-173">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53a99-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


