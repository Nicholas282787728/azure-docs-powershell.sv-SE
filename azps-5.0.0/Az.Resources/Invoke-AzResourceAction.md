---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322878"
---
# <span data-ttu-id="4a6f4-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="4a6f4-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="4a6f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6f4-103">Anropar en åtgärd för en resurs.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="4a6f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a6f4-104">SYNTAX</span></span>

### <span data-ttu-id="4a6f4-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="4a6f4-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a6f4-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4a6f4-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6f4-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4a6f4-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a6f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a6f4-108">DESCRIPTION</span></span>
<span data-ttu-id="4a6f4-109">Cmdleten **Invoke-AzResourceAction** anropar en åtgärd på en angiven Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="4a6f4-110">Använd Azure Resource Explorer-verktyget för att få en lista över vilka åtgärder som stöds.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="4a6f4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a6f4-111">EXAMPLES</span></span>

### <span data-ttu-id="4a6f4-112">Exempel 1: Invoke starta en virtuell dator med ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6f4-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4a6f4-113">Det här kommandot startar den virtuella datorn med {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="4a6f4-114">Exempel 2: anropa poweroffing en virtuell dator med ResourceName</span><span class="sxs-lookup"><span data-stu-id="4a6f4-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="4a6f4-115">Det här kommandot stoppar den virtuella datorn med {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="4a6f4-116">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4a6f4-117">Exempel 3: anropa registrering av en resurs leverantör med ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6f4-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="4a6f4-118">Det här kommandot registrerar en resurs leverantör "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="4a6f4-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="4a6f4-119">Kommandot anger parametern *Force* och ber därför inte dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4a6f4-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a6f4-120">PARAMETERS</span></span>

### <span data-ttu-id="4a6f4-121">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="4a6f4-121">-Action</span></span>
<span data-ttu-id="4a6f4-122">Anger namnet på den åtgärd som ska anropas.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4a6f4-123">-ApiVersion</span></span>
<span data-ttu-id="4a6f4-124">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4a6f4-125">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4a6f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6f4-126">-DefaultProfile</span></span>
<span data-ttu-id="4a6f4-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4a6f4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a6f4-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="4a6f4-128">-ExtensionResourceName</span></span>
<span data-ttu-id="4a6f4-129">Anger namnet på en tilläggs resurs för den resurs där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4a6f4-130">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="4a6f4-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="4a6f4-131">-ExtensionResourceType</span></span>
<span data-ttu-id="4a6f4-132">Anger typen för tilläggs resursen.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="4a6f4-133">Till exempel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4a6f4-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-134">-Force</span><span class="sxs-lookup"><span data-stu-id="4a6f4-134">-Force</span></span>
<span data-ttu-id="4a6f4-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a6f4-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4a6f4-136">-ODataQuery</span></span>
<span data-ttu-id="4a6f4-137">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4a6f4-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="4a6f4-138">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="4a6f4-139">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="4a6f4-139">-Parameters</span></span>
<span data-ttu-id="4a6f4-140">Anger parametrar som en hash-tabell för den åtgärd som denna cmdlet anropar.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-141">-För</span><span class="sxs-lookup"><span data-stu-id="4a6f4-141">-Pre</span></span>
<span data-ttu-id="4a6f4-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4a6f4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6f4-143">-ResourceGroupName</span></span>
<span data-ttu-id="4a6f4-144">Anger namnet på en resurs grupp där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6f4-145">-ResourceId</span></span>
<span data-ttu-id="4a6f4-146">Anger det fullständiga resurs-ID: t för resursen som denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4a6f4-147">Detta ID inkluderar abonnemanget, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4a6f4-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4a6f4-148">-ResourceName</span></span>
<span data-ttu-id="4a6f4-149">Anger namnet på resursen för resursen där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4a6f4-150">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4a6f4-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4a6f4-151">-ResourceType</span></span>
<span data-ttu-id="4a6f4-152">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="4a6f4-153">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4a6f4-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6f4-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4a6f4-154">-TenantLevel</span></span>
<span data-ttu-id="4a6f4-155">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4a6f4-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a6f4-156">-Confirm</span></span>
<span data-ttu-id="4a6f4-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a6f4-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6f4-158">-WhatIf</span></span>
<span data-ttu-id="4a6f4-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a6f4-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a6f4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6f4-161">CommonParameters</span></span>
<span data-ttu-id="4a6f4-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6f4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6f4-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a6f4-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6f4-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a6f4-164">INPUTS</span></span>

### <span data-ttu-id="4a6f4-165">System. String</span><span class="sxs-lookup"><span data-stu-id="4a6f4-165">System.String</span></span>

## <span data-ttu-id="4a6f4-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a6f4-166">OUTPUTS</span></span>

### <span data-ttu-id="4a6f4-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4a6f4-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4a6f4-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a6f4-168">NOTES</span></span>

## <span data-ttu-id="4a6f4-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a6f4-169">RELATED LINKS</span></span>
