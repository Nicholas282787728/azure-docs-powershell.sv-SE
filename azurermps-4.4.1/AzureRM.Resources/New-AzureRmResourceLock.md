---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585331"
---
# <span data-ttu-id="04551-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="04551-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="04551-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04551-102">SYNOPSIS</span></span>
<span data-ttu-id="04551-103">Skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="04551-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04551-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04551-104">SYNTAX</span></span>

### <span data-ttu-id="04551-105">Ett lås vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="04551-105">A lock at the specified scope.</span></span> <span data-ttu-id="04551-106">Vis</span><span class="sxs-lookup"><span data-stu-id="04551-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04551-107">Ett lås i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="04551-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04551-108">Ett lås i resurs gruppens resurs omfång.</span><span class="sxs-lookup"><span data-stu-id="04551-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04551-109">Ett lås i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="04551-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04551-110">Ett lås i resurs omfattningen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="04551-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04551-111">Ett lås hos klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="04551-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04551-112">Ett lås, efter ID.</span><span class="sxs-lookup"><span data-stu-id="04551-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04551-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04551-113">DESCRIPTION</span></span>
<span data-ttu-id="04551-114">Cmdleten **New-AzureRmResourceLock** skapar ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="04551-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="04551-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04551-115">EXAMPLES</span></span>

### <span data-ttu-id="04551-116">Exempel 1: skapa ett resurs lås på en webbplats</span><span class="sxs-lookup"><span data-stu-id="04551-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="04551-117">Det här kommandot skapar ett resurs lås på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="04551-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="04551-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04551-118">PARAMETERS</span></span>

### <span data-ttu-id="04551-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="04551-119">-ApiVersion</span></span>
<span data-ttu-id="04551-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="04551-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="04551-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="04551-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="04551-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04551-122">-Force</span></span>
<span data-ttu-id="04551-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="04551-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04551-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04551-124">-InformationAction</span></span>
<span data-ttu-id="04551-125">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="04551-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04551-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="04551-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04551-127">Vidare</span><span class="sxs-lookup"><span data-stu-id="04551-127">Continue</span></span>
- <span data-ttu-id="04551-128">Över</span><span class="sxs-lookup"><span data-stu-id="04551-128">Ignore</span></span>
- <span data-ttu-id="04551-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="04551-129">Inquire</span></span>
- <span data-ttu-id="04551-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04551-130">SilentlyContinue</span></span>
- <span data-ttu-id="04551-131">Stanna</span><span class="sxs-lookup"><span data-stu-id="04551-131">Stop</span></span>
- <span data-ttu-id="04551-132">Avbryt</span><span class="sxs-lookup"><span data-stu-id="04551-132">Suspend</span></span>

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

### <span data-ttu-id="04551-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04551-133">-InformationVariable</span></span>
<span data-ttu-id="04551-134">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="04551-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="04551-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="04551-135">-LockId</span></span>
<span data-ttu-id="04551-136">Anger låsets ID.</span><span class="sxs-lookup"><span data-stu-id="04551-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="04551-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="04551-137">-LockLevel</span></span>
<span data-ttu-id="04551-138">Anger nivån för låset.</span><span class="sxs-lookup"><span data-stu-id="04551-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="04551-139">För närvarande är det enda giltiga värdet CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="04551-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="04551-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="04551-140">-LockName</span></span>
<span data-ttu-id="04551-141">Anger namnet på låset.</span><span class="sxs-lookup"><span data-stu-id="04551-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="04551-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="04551-142">-LockNotes</span></span>
<span data-ttu-id="04551-143">Anger låsets anteckningar.</span><span class="sxs-lookup"><span data-stu-id="04551-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="04551-144">-För</span><span class="sxs-lookup"><span data-stu-id="04551-144">-Pre</span></span>
<span data-ttu-id="04551-145">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="04551-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="04551-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04551-146">-ResourceGroupName</span></span>
<span data-ttu-id="04551-147">Anger namnet på en resurs grupp som låset gäller för eller som innehåller den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="04551-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="04551-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="04551-148">-ResourceName</span></span>
<span data-ttu-id="04551-149">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="04551-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="04551-150">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="04551-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="04551-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="04551-151">-ResourceType</span></span>
<span data-ttu-id="04551-152">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="04551-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="04551-153">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="04551-153">-Scope</span></span>
<span data-ttu-id="04551-154">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="04551-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="04551-155">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="04551-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="04551-156">`/subscriptions/`abonnemang ID `/resourceGroups/` resurs grupp namn `/providers/Microsoft.Sql/servers/` Server namn `/databases/` databas namn</span><span class="sxs-lookup"><span data-stu-id="04551-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="04551-157">Använd följande format för att ange en resurs grupp:</span><span class="sxs-lookup"><span data-stu-id="04551-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="04551-158">`/subscriptions/`resurs grupps namn för prenumerations-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="04551-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="04551-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="04551-159">-TenantLevel</span></span>
<span data-ttu-id="04551-160">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="04551-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="04551-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04551-161">-Confirm</span></span>
<span data-ttu-id="04551-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04551-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04551-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04551-163">-WhatIf</span></span>
<span data-ttu-id="04551-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04551-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04551-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04551-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04551-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04551-166">-DefaultProfile</span></span>
<span data-ttu-id="04551-167">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04551-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04551-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04551-168">CommonParameters</span></span>
<span data-ttu-id="04551-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04551-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04551-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04551-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04551-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04551-171">INPUTS</span></span>

## <span data-ttu-id="04551-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04551-172">OUTPUTS</span></span>

### <span data-ttu-id="04551-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="04551-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="04551-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04551-174">NOTES</span></span>

## <span data-ttu-id="04551-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04551-175">RELATED LINKS</span></span>

[<span data-ttu-id="04551-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="04551-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="04551-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="04551-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="04551-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="04551-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


