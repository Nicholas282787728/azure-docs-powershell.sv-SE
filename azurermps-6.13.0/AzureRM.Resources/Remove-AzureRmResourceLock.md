---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c719eee4800b404d691d478a989fdfdb3e7be09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583991"
---
# <span data-ttu-id="bc427-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc427-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="bc427-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc427-102">SYNOPSIS</span></span>
<span data-ttu-id="bc427-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="bc427-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc427-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc427-104">SYNTAX</span></span>

### <span data-ttu-id="bc427-105">ByLockId (standard)</span><span class="sxs-lookup"><span data-stu-id="bc427-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc427-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc427-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc427-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bc427-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc427-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bc427-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc427-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bc427-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc427-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bc427-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc427-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc427-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc427-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc427-112">DESCRIPTION</span></span>
<span data-ttu-id="bc427-113">Cmdleten **Remove-AzureRmResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="bc427-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="bc427-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc427-114">EXAMPLES</span></span>

### <span data-ttu-id="bc427-115">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="bc427-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="bc427-116">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="bc427-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bc427-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc427-117">PARAMETERS</span></span>

### <span data-ttu-id="bc427-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc427-118">-ApiVersion</span></span>
<span data-ttu-id="bc427-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bc427-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bc427-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="bc427-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bc427-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc427-121">-DefaultProfile</span></span>
<span data-ttu-id="bc427-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bc427-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc427-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bc427-123">-Force</span></span>
<span data-ttu-id="bc427-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bc427-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc427-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bc427-125">-InformationAction</span></span>
<span data-ttu-id="bc427-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="bc427-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bc427-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bc427-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc427-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="bc427-128">Continue</span></span>
- <span data-ttu-id="bc427-129">Över</span><span class="sxs-lookup"><span data-stu-id="bc427-129">Ignore</span></span>
- <span data-ttu-id="bc427-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="bc427-130">Inquire</span></span>
- <span data-ttu-id="bc427-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc427-131">SilentlyContinue</span></span>
- <span data-ttu-id="bc427-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="bc427-132">Stop</span></span>
- <span data-ttu-id="bc427-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="bc427-133">Suspend</span></span>

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

### <span data-ttu-id="bc427-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc427-134">-InformationVariable</span></span>
<span data-ttu-id="bc427-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="bc427-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc427-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="bc427-136">-LockId</span></span>
<span data-ttu-id="bc427-137">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc427-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc427-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="bc427-138">-LockName</span></span>
<span data-ttu-id="bc427-139">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="bc427-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc427-140">-För</span><span class="sxs-lookup"><span data-stu-id="bc427-140">-Pre</span></span>
<span data-ttu-id="bc427-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bc427-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bc427-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc427-142">-ResourceGroupName</span></span>
<span data-ttu-id="bc427-143">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bc427-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="bc427-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bc427-144">-ResourceName</span></span>
<span data-ttu-id="bc427-145">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bc427-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bc427-146">Om du till exempel vill ange en databas använder du följande format: Server `/` databas</span><span class="sxs-lookup"><span data-stu-id="bc427-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="bc427-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bc427-147">-ResourceType</span></span>
<span data-ttu-id="bc427-148">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bc427-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="bc427-149">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="bc427-149">-Scope</span></span>
<span data-ttu-id="bc427-150">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="bc427-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="bc427-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc427-151">-TenantLevel</span></span>
<span data-ttu-id="bc427-152">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="bc427-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="bc427-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc427-153">-Confirm</span></span>
<span data-ttu-id="bc427-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc427-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc427-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc427-155">-WhatIf</span></span>
<span data-ttu-id="bc427-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc427-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc427-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc427-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc427-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc427-158">CommonParameters</span></span>
<span data-ttu-id="bc427-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc427-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc427-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc427-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc427-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc427-161">INPUTS</span></span>

## <span data-ttu-id="bc427-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc427-162">OUTPUTS</span></span>

## <span data-ttu-id="bc427-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc427-163">NOTES</span></span>

## <span data-ttu-id="bc427-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc427-164">RELATED LINKS</span></span>

[<span data-ttu-id="bc427-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc427-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="bc427-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc427-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="bc427-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc427-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)

