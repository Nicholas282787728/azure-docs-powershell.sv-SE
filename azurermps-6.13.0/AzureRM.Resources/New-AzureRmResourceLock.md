---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: cf1f245b06e607bc96a8e23429d15954ce7b69f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573912"
---
# <span data-ttu-id="386df-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="386df-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="386df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="386df-102">SYNOPSIS</span></span>
<span data-ttu-id="386df-103">Skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="386df-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="386df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="386df-104">SYNTAX</span></span>

### <span data-ttu-id="386df-105">BySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="386df-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="386df-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="386df-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="386df-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="386df-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386df-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="386df-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="386df-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="386df-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386df-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="386df-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386df-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="386df-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="386df-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="386df-112">DESCRIPTION</span></span>
<span data-ttu-id="386df-113">Cmdleten **New-AzureRmResourceLock** skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="386df-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="386df-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="386df-114">EXAMPLES</span></span>

### <span data-ttu-id="386df-115">Exempel 1: skapa ett resurs lås på en webbplats</span><span class="sxs-lookup"><span data-stu-id="386df-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="386df-116">Det här kommandot skapar ett resurs lås på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="386df-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="386df-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="386df-117">PARAMETERS</span></span>

### <span data-ttu-id="386df-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="386df-118">-ApiVersion</span></span>
<span data-ttu-id="386df-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="386df-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="386df-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="386df-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="386df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386df-121">-DefaultProfile</span></span>
<span data-ttu-id="386df-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="386df-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386df-123">-Force</span><span class="sxs-lookup"><span data-stu-id="386df-123">-Force</span></span>
<span data-ttu-id="386df-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="386df-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="386df-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="386df-125">-InformationAction</span></span>
<span data-ttu-id="386df-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="386df-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="386df-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="386df-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="386df-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="386df-128">Continue</span></span>
- <span data-ttu-id="386df-129">Över</span><span class="sxs-lookup"><span data-stu-id="386df-129">Ignore</span></span>
- <span data-ttu-id="386df-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="386df-130">Inquire</span></span>
- <span data-ttu-id="386df-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="386df-131">SilentlyContinue</span></span>
- <span data-ttu-id="386df-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="386df-132">Stop</span></span>
- <span data-ttu-id="386df-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="386df-133">Suspend</span></span>

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

### <span data-ttu-id="386df-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="386df-134">-InformationVariable</span></span>
<span data-ttu-id="386df-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="386df-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="386df-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="386df-136">-LockId</span></span>
<span data-ttu-id="386df-137">Anger låsets ID.</span><span class="sxs-lookup"><span data-stu-id="386df-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="386df-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="386df-138">-LockLevel</span></span>
<span data-ttu-id="386df-139">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="386df-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="386df-140">För närvarande är giltiga värden CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="386df-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="386df-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="386df-141">-LockName</span></span>
<span data-ttu-id="386df-142">Anger namnet på låset.</span><span class="sxs-lookup"><span data-stu-id="386df-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="386df-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="386df-143">-LockNotes</span></span>
<span data-ttu-id="386df-144">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="386df-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="386df-145">-För</span><span class="sxs-lookup"><span data-stu-id="386df-145">-Pre</span></span>
<span data-ttu-id="386df-146">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="386df-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="386df-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386df-147">-ResourceGroupName</span></span>
<span data-ttu-id="386df-148">Anger namnet på en resurs grupp som låset gäller för eller som innehåller den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="386df-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="386df-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="386df-149">-ResourceName</span></span>
<span data-ttu-id="386df-150">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="386df-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="386df-151">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="386df-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="386df-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="386df-152">-ResourceType</span></span>
<span data-ttu-id="386df-153">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="386df-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="386df-154">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="386df-154">-Scope</span></span>
<span data-ttu-id="386df-155">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="386df-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="386df-156">Om du till exempel vill ange en databas använder du följande format: `/subscriptions/` ID för `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn för att ange en resurs grupp, Använd följande format: `/subscriptions/` `/resourceGroups/` resurs GRUPPS namn för prenumerations-ID</span><span class="sxs-lookup"><span data-stu-id="386df-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="386df-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="386df-157">-TenantLevel</span></span>
<span data-ttu-id="386df-158">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="386df-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="386df-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="386df-159">-Confirm</span></span>
<span data-ttu-id="386df-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="386df-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386df-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386df-161">-WhatIf</span></span>
<span data-ttu-id="386df-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="386df-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386df-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="386df-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386df-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386df-164">CommonParameters</span></span>
<span data-ttu-id="386df-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386df-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386df-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386df-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386df-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="386df-167">INPUTS</span></span>

## <span data-ttu-id="386df-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="386df-168">OUTPUTS</span></span>

## <span data-ttu-id="386df-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="386df-169">NOTES</span></span>

## <span data-ttu-id="386df-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="386df-170">RELATED LINKS</span></span>

[<span data-ttu-id="386df-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="386df-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="386df-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="386df-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="386df-173">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="386df-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


