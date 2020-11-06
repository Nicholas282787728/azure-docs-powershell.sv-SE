---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581291"
---
# <span data-ttu-id="57af3-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="57af3-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="57af3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57af3-102">SYNOPSIS</span></span>
<span data-ttu-id="57af3-103">Tar bort ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="57af3-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57af3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57af3-104">SYNTAX</span></span>

### <span data-ttu-id="57af3-105">Ett lås, efter ID. (standard)</span><span class="sxs-lookup"><span data-stu-id="57af3-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57af3-106">Ett lås i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="57af3-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57af3-107">Ett lås i resurs gruppens resurs omfång.</span><span class="sxs-lookup"><span data-stu-id="57af3-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57af3-108">Ett lås vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="57af3-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57af3-109">Ett lås i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="57af3-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57af3-110">Ett lås i resurs omfattningen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="57af3-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57af3-111">Ett lås hos klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="57af3-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57af3-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57af3-112">DESCRIPTION</span></span>
<span data-ttu-id="57af3-113">Cmdleten **Remove-AzureRmResourceLock** tar bort ett Azure-resurs lås.</span><span class="sxs-lookup"><span data-stu-id="57af3-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="57af3-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57af3-114">EXAMPLES</span></span>

### <span data-ttu-id="57af3-115">Exempel 1: ta bort ett lås</span><span class="sxs-lookup"><span data-stu-id="57af3-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="57af3-116">Det här kommandot tar bort låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="57af3-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="57af3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57af3-117">PARAMETERS</span></span>

### <span data-ttu-id="57af3-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="57af3-118">-ApiVersion</span></span>
<span data-ttu-id="57af3-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="57af3-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="57af3-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="57af3-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="57af3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="57af3-121">-Force</span></span>
<span data-ttu-id="57af3-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="57af3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57af3-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="57af3-123">-InformationAction</span></span>
<span data-ttu-id="57af3-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="57af3-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="57af3-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="57af3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57af3-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="57af3-126">Continue</span></span>
- <span data-ttu-id="57af3-127">Över</span><span class="sxs-lookup"><span data-stu-id="57af3-127">Ignore</span></span>
- <span data-ttu-id="57af3-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="57af3-128">Inquire</span></span>
- <span data-ttu-id="57af3-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="57af3-129">SilentlyContinue</span></span>
- <span data-ttu-id="57af3-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="57af3-130">Stop</span></span>
- <span data-ttu-id="57af3-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="57af3-131">Suspend</span></span>

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

### <span data-ttu-id="57af3-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="57af3-132">-InformationVariable</span></span>
<span data-ttu-id="57af3-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="57af3-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="57af3-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="57af3-134">-LockId</span></span>
<span data-ttu-id="57af3-135">Anger ID för låset som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57af3-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="57af3-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="57af3-136">-LockName</span></span>
<span data-ttu-id="57af3-137">Anger namnet på det lås som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="57af3-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57af3-138">-För</span><span class="sxs-lookup"><span data-stu-id="57af3-138">-Pre</span></span>
<span data-ttu-id="57af3-139">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="57af3-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="57af3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57af3-140">-ResourceGroupName</span></span>
<span data-ttu-id="57af3-141">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="57af3-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="57af3-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="57af3-142">-ResourceName</span></span>
<span data-ttu-id="57af3-143">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="57af3-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="57af3-144">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="57af3-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="57af3-145">Server- `/` databas</span><span class="sxs-lookup"><span data-stu-id="57af3-145">Server`/`Database</span></span>

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

### <span data-ttu-id="57af3-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="57af3-146">-ResourceType</span></span>
<span data-ttu-id="57af3-147">Anger resurs typen för resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="57af3-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="57af3-148">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="57af3-148">-Scope</span></span>
<span data-ttu-id="57af3-149">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="57af3-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="57af3-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="57af3-150">-TenantLevel</span></span>
<span data-ttu-id="57af3-151">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="57af3-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="57af3-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57af3-152">-Confirm</span></span>
<span data-ttu-id="57af3-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57af3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57af3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57af3-154">-WhatIf</span></span>
<span data-ttu-id="57af3-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57af3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57af3-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57af3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57af3-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57af3-157">-DefaultProfile</span></span>
<span data-ttu-id="57af3-158">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57af3-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57af3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57af3-159">CommonParameters</span></span>
<span data-ttu-id="57af3-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57af3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57af3-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57af3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57af3-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57af3-162">INPUTS</span></span>

## <span data-ttu-id="57af3-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57af3-163">OUTPUTS</span></span>

### <span data-ttu-id="57af3-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="57af3-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="57af3-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57af3-165">NOTES</span></span>

## <span data-ttu-id="57af3-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57af3-166">RELATED LINKS</span></span>

[<span data-ttu-id="57af3-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="57af3-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="57af3-168">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="57af3-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="57af3-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="57af3-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


