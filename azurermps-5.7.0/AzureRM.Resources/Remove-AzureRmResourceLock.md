---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756072"
---
# <span data-ttu-id="0beca-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0beca-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="0beca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0beca-102">SYNOPSIS</span></span>
<span data-ttu-id="0beca-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="0beca-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0beca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0beca-104">SYNTAX</span></span>

### <span data-ttu-id="0beca-105">ByLockId (standard)</span><span class="sxs-lookup"><span data-stu-id="0beca-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0beca-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0beca-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0beca-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0beca-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0beca-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0beca-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0beca-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0beca-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0beca-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0beca-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0beca-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0beca-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0beca-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0beca-112">DESCRIPTION</span></span>
<span data-ttu-id="0beca-113">Cmdleten **Remove-AzureRmResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="0beca-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="0beca-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0beca-114">EXAMPLES</span></span>

### <span data-ttu-id="0beca-115">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="0beca-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="0beca-116">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="0beca-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0beca-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0beca-117">PARAMETERS</span></span>

### <span data-ttu-id="0beca-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0beca-118">-ApiVersion</span></span>
<span data-ttu-id="0beca-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0beca-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0beca-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="0beca-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0beca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0beca-121">-DefaultProfile</span></span>
<span data-ttu-id="0beca-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0beca-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0beca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0beca-123">-Force</span></span>
<span data-ttu-id="0beca-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0beca-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0beca-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0beca-125">-InformationAction</span></span>
<span data-ttu-id="0beca-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="0beca-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0beca-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0beca-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0beca-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="0beca-128">Continue</span></span>
- <span data-ttu-id="0beca-129">Över</span><span class="sxs-lookup"><span data-stu-id="0beca-129">Ignore</span></span>
- <span data-ttu-id="0beca-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="0beca-130">Inquire</span></span>
- <span data-ttu-id="0beca-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0beca-131">SilentlyContinue</span></span>
- <span data-ttu-id="0beca-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="0beca-132">Stop</span></span>
- <span data-ttu-id="0beca-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="0beca-133">Suspend</span></span>

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

### <span data-ttu-id="0beca-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0beca-134">-InformationVariable</span></span>
<span data-ttu-id="0beca-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="0beca-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0beca-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="0beca-136">-LockId</span></span>
<span data-ttu-id="0beca-137">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0beca-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0beca-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="0beca-138">-LockName</span></span>
<span data-ttu-id="0beca-139">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0beca-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0beca-140">-För</span><span class="sxs-lookup"><span data-stu-id="0beca-140">-Pre</span></span>
<span data-ttu-id="0beca-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0beca-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0beca-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0beca-142">-ResourceGroupName</span></span>
<span data-ttu-id="0beca-143">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0beca-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="0beca-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0beca-144">-ResourceName</span></span>
<span data-ttu-id="0beca-145">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0beca-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="0beca-146">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="0beca-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="0beca-147">Server- `/` databas</span><span class="sxs-lookup"><span data-stu-id="0beca-147">Server`/`Database</span></span>

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

### <span data-ttu-id="0beca-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0beca-148">-ResourceType</span></span>
<span data-ttu-id="0beca-149">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0beca-149">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="0beca-150">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0beca-150">-Scope</span></span>
<span data-ttu-id="0beca-151">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="0beca-151">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="0beca-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0beca-152">-TenantLevel</span></span>
<span data-ttu-id="0beca-153">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="0beca-153">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0beca-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0beca-154">-Confirm</span></span>
<span data-ttu-id="0beca-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0beca-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0beca-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0beca-156">-WhatIf</span></span>
<span data-ttu-id="0beca-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0beca-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0beca-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0beca-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0beca-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0beca-159">CommonParameters</span></span>
<span data-ttu-id="0beca-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0beca-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0beca-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0beca-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0beca-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0beca-162">INPUTS</span></span>

### <span data-ttu-id="0beca-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="0beca-163">None</span></span>
<span data-ttu-id="0beca-164">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0beca-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0beca-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0beca-165">OUTPUTS</span></span>

### <span data-ttu-id="0beca-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0beca-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0beca-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0beca-167">NOTES</span></span>

## <span data-ttu-id="0beca-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0beca-168">RELATED LINKS</span></span>

[<span data-ttu-id="0beca-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0beca-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="0beca-170">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0beca-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="0beca-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0beca-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


