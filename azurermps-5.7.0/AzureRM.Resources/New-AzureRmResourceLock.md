---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: 0b3498ba3107e2312b596143820036286b925b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755590"
---
# <span data-ttu-id="c54d1-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c54d1-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="c54d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c54d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c54d1-103">Skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="c54d1-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c54d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c54d1-104">SYNTAX</span></span>

### <span data-ttu-id="c54d1-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="c54d1-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c54d1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c54d1-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c54d1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c54d1-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c54d1-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c54d1-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c54d1-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c54d1-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c54d1-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c54d1-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c54d1-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c54d1-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c54d1-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c54d1-112">DESCRIPTION</span></span>
<span data-ttu-id="c54d1-113">Cmdleten **New-AzureRmResourceLock** skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="c54d1-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="c54d1-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c54d1-114">EXAMPLES</span></span>

### <span data-ttu-id="c54d1-115">Exempel 1: skapa ett resurs lås på en webbplats</span><span class="sxs-lookup"><span data-stu-id="c54d1-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="c54d1-116">Det här kommandot skapar ett resurs lås på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="c54d1-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="c54d1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c54d1-117">PARAMETERS</span></span>

### <span data-ttu-id="c54d1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c54d1-118">-ApiVersion</span></span>
<span data-ttu-id="c54d1-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c54d1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c54d1-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="c54d1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c54d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54d1-121">-DefaultProfile</span></span>
<span data-ttu-id="c54d1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c54d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c54d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c54d1-123">-Force</span></span>
<span data-ttu-id="c54d1-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c54d1-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c54d1-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c54d1-125">-InformationAction</span></span>
<span data-ttu-id="c54d1-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c54d1-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c54d1-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c54d1-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c54d1-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="c54d1-128">Continue</span></span>
- <span data-ttu-id="c54d1-129">Över</span><span class="sxs-lookup"><span data-stu-id="c54d1-129">Ignore</span></span>
- <span data-ttu-id="c54d1-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="c54d1-130">Inquire</span></span>
- <span data-ttu-id="c54d1-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c54d1-131">SilentlyContinue</span></span>
- <span data-ttu-id="c54d1-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="c54d1-132">Stop</span></span>
- <span data-ttu-id="c54d1-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c54d1-133">Suspend</span></span>

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

### <span data-ttu-id="c54d1-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c54d1-134">-InformationVariable</span></span>
<span data-ttu-id="c54d1-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c54d1-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c54d1-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="c54d1-136">-LockId</span></span>
<span data-ttu-id="c54d1-137">Anger låsets ID.</span><span class="sxs-lookup"><span data-stu-id="c54d1-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="c54d1-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c54d1-138">-LockLevel</span></span>
<span data-ttu-id="c54d1-139">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="c54d1-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="c54d1-140">För närvarande är giltiga värden CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="c54d1-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="c54d1-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="c54d1-141">-LockName</span></span>
<span data-ttu-id="c54d1-142">Anger namnet på låset.</span><span class="sxs-lookup"><span data-stu-id="c54d1-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="c54d1-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c54d1-143">-LockNotes</span></span>
<span data-ttu-id="c54d1-144">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="c54d1-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c54d1-145">-För</span><span class="sxs-lookup"><span data-stu-id="c54d1-145">-Pre</span></span>
<span data-ttu-id="c54d1-146">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c54d1-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c54d1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54d1-147">-ResourceGroupName</span></span>
<span data-ttu-id="c54d1-148">Anger namnet på en resurs grupp som låset gäller för eller som innehåller den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="c54d1-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="c54d1-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c54d1-149">-ResourceName</span></span>
<span data-ttu-id="c54d1-150">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="c54d1-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c54d1-151">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="c54d1-151">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="c54d1-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c54d1-152">-ResourceType</span></span>
<span data-ttu-id="c54d1-153">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="c54d1-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="c54d1-154">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c54d1-154">-Scope</span></span>
<span data-ttu-id="c54d1-155">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="c54d1-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c54d1-156">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="c54d1-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c54d1-157">`/subscriptions/`abonnemang ID `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn</span><span class="sxs-lookup"><span data-stu-id="c54d1-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="c54d1-158">Använd följande format för att ange en resurs grupp:</span><span class="sxs-lookup"><span data-stu-id="c54d1-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="c54d1-159">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="c54d1-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="c54d1-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c54d1-160">-TenantLevel</span></span>
<span data-ttu-id="c54d1-161">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="c54d1-161">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c54d1-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c54d1-162">-Confirm</span></span>
<span data-ttu-id="c54d1-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c54d1-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c54d1-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c54d1-164">-WhatIf</span></span>
<span data-ttu-id="c54d1-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c54d1-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c54d1-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c54d1-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c54d1-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54d1-167">CommonParameters</span></span>
<span data-ttu-id="c54d1-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c54d1-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54d1-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54d1-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54d1-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c54d1-170">INPUTS</span></span>

### <span data-ttu-id="c54d1-171">Ingen</span><span class="sxs-lookup"><span data-stu-id="c54d1-171">None</span></span>
<span data-ttu-id="c54d1-172">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c54d1-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c54d1-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c54d1-173">OUTPUTS</span></span>

### <span data-ttu-id="c54d1-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c54d1-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c54d1-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c54d1-175">NOTES</span></span>

## <span data-ttu-id="c54d1-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c54d1-176">RELATED LINKS</span></span>

[<span data-ttu-id="c54d1-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c54d1-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="c54d1-178">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c54d1-178">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="c54d1-179">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c54d1-179">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


