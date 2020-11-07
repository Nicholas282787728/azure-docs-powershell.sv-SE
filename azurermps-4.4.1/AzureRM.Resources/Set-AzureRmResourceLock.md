---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756853"
---
# <span data-ttu-id="19425-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="19425-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="19425-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19425-102">SYNOPSIS</span></span>
<span data-ttu-id="19425-103">Ändrar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="19425-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19425-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19425-104">SYNTAX</span></span>

### <span data-ttu-id="19425-105">Ett lås vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="19425-105">A lock at the specified scope.</span></span> <span data-ttu-id="19425-106">Vis</span><span class="sxs-lookup"><span data-stu-id="19425-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19425-107">Ett lås i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="19425-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19425-108">Ett lås i resurs gruppens resurs omfång.</span><span class="sxs-lookup"><span data-stu-id="19425-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19425-109">Ett lås i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="19425-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19425-110">Ett lås i resurs omfattningen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="19425-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19425-111">Ett lås hos klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="19425-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19425-112">Ett lås, efter ID.</span><span class="sxs-lookup"><span data-stu-id="19425-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19425-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19425-113">DESCRIPTION</span></span>
<span data-ttu-id="19425-114">Cmdleten **set-AzureRmResourceLock** ändrar resurs låset.</span><span class="sxs-lookup"><span data-stu-id="19425-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="19425-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19425-115">EXAMPLES</span></span>

### <span data-ttu-id="19425-116">Exempel 1: uppdatera anteckningar för ett lås</span><span class="sxs-lookup"><span data-stu-id="19425-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="19425-117">Det här kommandot uppdaterar anteckningen för ett lås med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="19425-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="19425-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19425-118">PARAMETERS</span></span>

### <span data-ttu-id="19425-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19425-119">-ApiVersion</span></span>
<span data-ttu-id="19425-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="19425-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19425-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="19425-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19425-122">-Force</span><span class="sxs-lookup"><span data-stu-id="19425-122">-Force</span></span>
<span data-ttu-id="19425-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="19425-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19425-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="19425-124">-InformationAction</span></span>
<span data-ttu-id="19425-125">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="19425-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19425-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="19425-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19425-127">Vidare</span><span class="sxs-lookup"><span data-stu-id="19425-127">Continue</span></span>
- <span data-ttu-id="19425-128">Över</span><span class="sxs-lookup"><span data-stu-id="19425-128">Ignore</span></span>
- <span data-ttu-id="19425-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="19425-129">Inquire</span></span>
- <span data-ttu-id="19425-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19425-130">SilentlyContinue</span></span>
- <span data-ttu-id="19425-131">Stanna</span><span class="sxs-lookup"><span data-stu-id="19425-131">Stop</span></span>
- <span data-ttu-id="19425-132">Avbryt</span><span class="sxs-lookup"><span data-stu-id="19425-132">Suspend</span></span>

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

### <span data-ttu-id="19425-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19425-133">-InformationVariable</span></span>
<span data-ttu-id="19425-134">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="19425-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19425-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="19425-135">-LockId</span></span>
<span data-ttu-id="19425-136">Anger det lås som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="19425-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="19425-137">-LockLevel</span></span>
<span data-ttu-id="19425-138">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="19425-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="19425-139">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="19425-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="19425-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="19425-140">-LockName</span></span>
<span data-ttu-id="19425-141">Anger namnet på det lås som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="19425-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="19425-142">-LockNotes</span></span>
<span data-ttu-id="19425-143">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="19425-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="19425-144">-För</span><span class="sxs-lookup"><span data-stu-id="19425-144">-Pre</span></span>
<span data-ttu-id="19425-145">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="19425-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19425-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19425-146">-ResourceGroupName</span></span>
<span data-ttu-id="19425-147">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="19425-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19425-148">-ResourceName</span></span>
<span data-ttu-id="19425-149">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="19425-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="19425-150">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="19425-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="19425-151">Server- `/` databas</span><span class="sxs-lookup"><span data-stu-id="19425-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="19425-152">-ResourceType</span></span>
<span data-ttu-id="19425-153">Anger den resurs typ som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="19425-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-154">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="19425-154">-Scope</span></span>
<span data-ttu-id="19425-155">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="19425-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="19425-156">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="19425-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="19425-157">`/subscriptions/`abonnemang ID `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn</span><span class="sxs-lookup"><span data-stu-id="19425-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="19425-158">Använd följande format för att ange en resurs grupp:</span><span class="sxs-lookup"><span data-stu-id="19425-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="19425-159">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="19425-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19425-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="19425-160">-TenantLevel</span></span>
<span data-ttu-id="19425-161">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="19425-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19425-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19425-162">-Confirm</span></span>
<span data-ttu-id="19425-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19425-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19425-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19425-164">-WhatIf</span></span>
<span data-ttu-id="19425-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19425-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19425-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19425-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19425-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19425-167">-DefaultProfile</span></span>
<span data-ttu-id="19425-168">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19425-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19425-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19425-169">CommonParameters</span></span>
<span data-ttu-id="19425-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19425-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19425-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19425-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19425-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19425-172">INPUTS</span></span>

## <span data-ttu-id="19425-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19425-173">OUTPUTS</span></span>

### <span data-ttu-id="19425-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19425-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19425-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19425-175">NOTES</span></span>

## <span data-ttu-id="19425-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19425-176">RELATED LINKS</span></span>

[<span data-ttu-id="19425-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="19425-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="19425-178">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="19425-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="19425-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="19425-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


