---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 12d1a696bd37cd6844a54f32f60bf70eaba6a0b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583035"
---
# <span data-ttu-id="af386-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="af386-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="af386-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af386-102">SYNOPSIS</span></span>
<span data-ttu-id="af386-103">Ändrar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="af386-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af386-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af386-104">SYNTAX</span></span>

### <span data-ttu-id="af386-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="af386-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af386-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="af386-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af386-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="af386-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af386-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="af386-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af386-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="af386-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af386-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="af386-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af386-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="af386-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af386-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af386-112">DESCRIPTION</span></span>
<span data-ttu-id="af386-113">Cmdleten **set-AzureRmResourceLock** ändrar resurs låset.</span><span class="sxs-lookup"><span data-stu-id="af386-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="af386-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af386-114">EXAMPLES</span></span>

### <span data-ttu-id="af386-115">Exempel 1: uppdatera anteckningar för ett lås</span><span class="sxs-lookup"><span data-stu-id="af386-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="af386-116">Det här kommandot uppdaterar anteckningen för ett lås med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="af386-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="af386-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af386-117">PARAMETERS</span></span>

### <span data-ttu-id="af386-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af386-118">-ApiVersion</span></span>
<span data-ttu-id="af386-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="af386-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="af386-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="af386-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af386-121">-DefaultProfile</span></span>
<span data-ttu-id="af386-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af386-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-123">-Force</span><span class="sxs-lookup"><span data-stu-id="af386-123">-Force</span></span>
<span data-ttu-id="af386-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af386-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="af386-125">-InformationAction</span></span>
<span data-ttu-id="af386-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="af386-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="af386-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="af386-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af386-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="af386-128">Continue</span></span>
- <span data-ttu-id="af386-129">Över</span><span class="sxs-lookup"><span data-stu-id="af386-129">Ignore</span></span>
- <span data-ttu-id="af386-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="af386-130">Inquire</span></span>
- <span data-ttu-id="af386-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="af386-131">SilentlyContinue</span></span>
- <span data-ttu-id="af386-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="af386-132">Stop</span></span>
- <span data-ttu-id="af386-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="af386-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="af386-134">-InformationVariable</span></span>
<span data-ttu-id="af386-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="af386-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="af386-136">-LockId</span></span>
<span data-ttu-id="af386-137">Anger det lås som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="af386-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="af386-138">-LockLevel</span></span>
<span data-ttu-id="af386-139">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="af386-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="af386-140">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="af386-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="af386-141">-LockName</span></span>
<span data-ttu-id="af386-142">Anger namnet på det lås som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="af386-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="af386-143">-LockNotes</span></span>
<span data-ttu-id="af386-144">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="af386-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-145">-För</span><span class="sxs-lookup"><span data-stu-id="af386-145">-Pre</span></span>
<span data-ttu-id="af386-146">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="af386-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af386-147">-ResourceGroupName</span></span>
<span data-ttu-id="af386-148">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af386-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="af386-149">-ResourceName</span></span>
<span data-ttu-id="af386-150">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af386-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="af386-151">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="af386-151">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="af386-152">Server- `/` databas</span><span class="sxs-lookup"><span data-stu-id="af386-152">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-153">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="af386-153">-ResourceType</span></span>
<span data-ttu-id="af386-154">Anger den resurs typ som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af386-154">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-155">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="af386-155">-Scope</span></span>
<span data-ttu-id="af386-156">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="af386-156">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="af386-157">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="af386-157">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="af386-158">`/subscriptions/`abonnemang ID `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn</span><span class="sxs-lookup"><span data-stu-id="af386-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="af386-159">Använd följande format för att ange en resurs grupp:</span><span class="sxs-lookup"><span data-stu-id="af386-159">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="af386-160">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="af386-160">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af386-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="af386-161">-TenantLevel</span></span>
<span data-ttu-id="af386-162">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="af386-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af386-163">-Confirm</span></span>
<span data-ttu-id="af386-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af386-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af386-165">-WhatIf</span></span>
<span data-ttu-id="af386-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af386-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af386-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af386-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af386-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af386-168">CommonParameters</span></span>
<span data-ttu-id="af386-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af386-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af386-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af386-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af386-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af386-171">INPUTS</span></span>

### <span data-ttu-id="af386-172">Ingen</span><span class="sxs-lookup"><span data-stu-id="af386-172">None</span></span>
<span data-ttu-id="af386-173">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="af386-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af386-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af386-174">OUTPUTS</span></span>

### <span data-ttu-id="af386-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="af386-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="af386-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af386-176">NOTES</span></span>

## <span data-ttu-id="af386-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af386-177">RELATED LINKS</span></span>

[<span data-ttu-id="af386-178">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="af386-178">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="af386-179">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="af386-179">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="af386-180">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="af386-180">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


