---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919316"
---
# <span data-ttu-id="ff98b-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="ff98b-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="ff98b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff98b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff98b-103">Anropar en åtgärd för en resurs.</span><span class="sxs-lookup"><span data-stu-id="ff98b-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="ff98b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff98b-104">SYNTAX</span></span>

### <span data-ttu-id="ff98b-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="ff98b-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff98b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ff98b-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff98b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ff98b-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff98b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff98b-108">DESCRIPTION</span></span>
<span data-ttu-id="ff98b-109">Cmdleten **Invoke-AzResourceAction** anropar en åtgärd på en angiven Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="ff98b-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="ff98b-110">Använd Azure Resource Explorer-verktyget för att få en lista över vilka åtgärder som stöds.</span><span class="sxs-lookup"><span data-stu-id="ff98b-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="ff98b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff98b-111">EXAMPLES</span></span>

## <span data-ttu-id="ff98b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff98b-112">PARAMETERS</span></span>

### <span data-ttu-id="ff98b-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="ff98b-113">-Action</span></span>
<span data-ttu-id="ff98b-114">Anger namnet på den åtgärd som ska anropas.</span><span class="sxs-lookup"><span data-stu-id="ff98b-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="ff98b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ff98b-115">-ApiVersion</span></span>
<span data-ttu-id="ff98b-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ff98b-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ff98b-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ff98b-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ff98b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff98b-118">-DefaultProfile</span></span>
<span data-ttu-id="ff98b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff98b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff98b-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ff98b-120">-ExtensionResourceName</span></span>
<span data-ttu-id="ff98b-121">Anger namnet på en tilläggs resurs för den resurs där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ff98b-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ff98b-122">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="ff98b-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="ff98b-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ff98b-123">-ExtensionResourceType</span></span>
<span data-ttu-id="ff98b-124">Anger typen för tilläggs resursen.</span><span class="sxs-lookup"><span data-stu-id="ff98b-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="ff98b-125">Till exempel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ff98b-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ff98b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ff98b-126">-Force</span></span>
<span data-ttu-id="ff98b-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ff98b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff98b-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ff98b-128">-ODataQuery</span></span>
<span data-ttu-id="ff98b-129">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ff98b-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ff98b-130">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="ff98b-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ff98b-131">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="ff98b-131">-Parameters</span></span>
<span data-ttu-id="ff98b-132">Anger parametrar som en hash-tabell för den åtgärd som denna cmdlet anropar.</span><span class="sxs-lookup"><span data-stu-id="ff98b-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="ff98b-133">-För</span><span class="sxs-lookup"><span data-stu-id="ff98b-133">-Pre</span></span>
<span data-ttu-id="ff98b-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ff98b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ff98b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff98b-135">-ResourceGroupName</span></span>
<span data-ttu-id="ff98b-136">Anger namnet på en resurs grupp där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ff98b-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="ff98b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff98b-137">-ResourceId</span></span>
<span data-ttu-id="ff98b-138">Anger det fullständiga resurs-ID: t för resursen som denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ff98b-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ff98b-139">Detta ID inkluderar abonnemanget, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ff98b-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ff98b-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ff98b-140">-ResourceName</span></span>
<span data-ttu-id="ff98b-141">Anger namnet på resursen för resursen där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ff98b-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ff98b-142">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ff98b-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ff98b-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ff98b-143">-ResourceType</span></span>
<span data-ttu-id="ff98b-144">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="ff98b-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="ff98b-145">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ff98b-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ff98b-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ff98b-146">-TenantLevel</span></span>
<span data-ttu-id="ff98b-147">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="ff98b-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ff98b-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff98b-148">-Confirm</span></span>
<span data-ttu-id="ff98b-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff98b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff98b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff98b-150">-WhatIf</span></span>
<span data-ttu-id="ff98b-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff98b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff98b-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff98b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff98b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff98b-153">CommonParameters</span></span>
<span data-ttu-id="ff98b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff98b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff98b-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff98b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff98b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff98b-156">INPUTS</span></span>

### <span data-ttu-id="ff98b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ff98b-157">System.String</span></span>

## <span data-ttu-id="ff98b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff98b-158">OUTPUTS</span></span>

### <span data-ttu-id="ff98b-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ff98b-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ff98b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff98b-160">NOTES</span></span>

## <span data-ttu-id="ff98b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff98b-161">RELATED LINKS</span></span>
