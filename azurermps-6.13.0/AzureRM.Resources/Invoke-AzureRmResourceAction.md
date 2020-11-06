---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 0a8fa9f13e77617a7f9efbd31909edfd64bf353a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576777"
---
# <span data-ttu-id="4dacc-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="4dacc-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="4dacc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dacc-102">SYNOPSIS</span></span>
<span data-ttu-id="4dacc-103">Anropar en åtgärd för en resurs.</span><span class="sxs-lookup"><span data-stu-id="4dacc-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dacc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dacc-104">SYNTAX</span></span>

### <span data-ttu-id="4dacc-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="4dacc-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dacc-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4dacc-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dacc-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4dacc-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dacc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dacc-108">DESCRIPTION</span></span>
<span data-ttu-id="4dacc-109">Cmdleten **Invoke-AzureRmResourceAction** anropar en åtgärd på en angiven Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="4dacc-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="4dacc-110">Använd Azure Resource Explorer-verktyget för att få en lista över vilka åtgärder som stöds.</span><span class="sxs-lookup"><span data-stu-id="4dacc-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="4dacc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dacc-111">EXAMPLES</span></span>

## <span data-ttu-id="4dacc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dacc-112">PARAMETERS</span></span>

### <span data-ttu-id="4dacc-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="4dacc-113">-Action</span></span>
<span data-ttu-id="4dacc-114">Anger namnet på den åtgärd som ska anropas.</span><span class="sxs-lookup"><span data-stu-id="4dacc-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="4dacc-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4dacc-115">-ApiVersion</span></span>
<span data-ttu-id="4dacc-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4dacc-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4dacc-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4dacc-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4dacc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dacc-118">-DefaultProfile</span></span>
<span data-ttu-id="4dacc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4dacc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dacc-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="4dacc-120">-ExtensionResourceName</span></span>
<span data-ttu-id="4dacc-121">Anger namnet på en tilläggs resurs för den resurs där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4dacc-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4dacc-122">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="4dacc-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="4dacc-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="4dacc-123">-ExtensionResourceType</span></span>
<span data-ttu-id="4dacc-124">Anger typen för tilläggs resursen.</span><span class="sxs-lookup"><span data-stu-id="4dacc-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="4dacc-125">Till exempel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4dacc-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4dacc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4dacc-126">-Force</span></span>
<span data-ttu-id="4dacc-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4dacc-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dacc-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4dacc-128">-InformationAction</span></span>
<span data-ttu-id="4dacc-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4dacc-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="4dacc-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4dacc-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dacc-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="4dacc-131">Continue</span></span>
- <span data-ttu-id="4dacc-132">Över</span><span class="sxs-lookup"><span data-stu-id="4dacc-132">Ignore</span></span>
- <span data-ttu-id="4dacc-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="4dacc-133">Inquire</span></span>
- <span data-ttu-id="4dacc-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4dacc-134">SilentlyContinue</span></span>
- <span data-ttu-id="4dacc-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="4dacc-135">Stop</span></span>
- <span data-ttu-id="4dacc-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4dacc-136">Suspend</span></span>

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

### <span data-ttu-id="4dacc-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4dacc-137">-InformationVariable</span></span>
<span data-ttu-id="4dacc-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4dacc-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4dacc-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4dacc-139">-ODataQuery</span></span>
<span data-ttu-id="4dacc-140">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4dacc-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="4dacc-141">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="4dacc-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="4dacc-142">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="4dacc-142">-Parameters</span></span>
<span data-ttu-id="4dacc-143">Anger parametrar som en hash-tabell för den åtgärd som denna cmdlet anropar.</span><span class="sxs-lookup"><span data-stu-id="4dacc-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="4dacc-144">-För</span><span class="sxs-lookup"><span data-stu-id="4dacc-144">-Pre</span></span>
<span data-ttu-id="4dacc-145">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4dacc-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4dacc-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dacc-146">-ResourceGroupName</span></span>
<span data-ttu-id="4dacc-147">Anger namnet på en resurs grupp där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4dacc-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="4dacc-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dacc-148">-ResourceId</span></span>
<span data-ttu-id="4dacc-149">Anger det fullständiga resurs-ID: t för resursen som denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4dacc-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4dacc-150">Detta ID inkluderar abonnemanget, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4dacc-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4dacc-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4dacc-151">-ResourceName</span></span>
<span data-ttu-id="4dacc-152">Anger namnet på resursen för resursen där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4dacc-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="4dacc-153">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4dacc-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4dacc-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4dacc-154">-ResourceType</span></span>
<span data-ttu-id="4dacc-155">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="4dacc-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="4dacc-156">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4dacc-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4dacc-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4dacc-157">-TenantLevel</span></span>
<span data-ttu-id="4dacc-158">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="4dacc-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4dacc-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dacc-159">-Confirm</span></span>
<span data-ttu-id="4dacc-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dacc-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dacc-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dacc-161">-WhatIf</span></span>
<span data-ttu-id="4dacc-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dacc-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dacc-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4dacc-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dacc-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dacc-164">CommonParameters</span></span>
<span data-ttu-id="4dacc-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dacc-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dacc-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dacc-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dacc-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dacc-167">INPUTS</span></span>

## <span data-ttu-id="4dacc-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dacc-168">OUTPUTS</span></span>

## <span data-ttu-id="4dacc-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dacc-169">NOTES</span></span>

## <span data-ttu-id="4dacc-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dacc-170">RELATED LINKS</span></span>
