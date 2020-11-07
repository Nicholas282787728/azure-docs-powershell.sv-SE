---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756463"
---
# <span data-ttu-id="be405-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="be405-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="be405-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be405-102">SYNOPSIS</span></span>
<span data-ttu-id="be405-103">Anropar en åtgärd för en resurs.</span><span class="sxs-lookup"><span data-stu-id="be405-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be405-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be405-104">SYNTAX</span></span>

### <span data-ttu-id="be405-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="be405-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be405-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="be405-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be405-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="be405-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be405-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be405-108">DESCRIPTION</span></span>
<span data-ttu-id="be405-109">Cmdleten **Invoke-AzureRmResourceAction** anropar en åtgärd på en angiven Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="be405-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="be405-110">Använd Azure Resource Explorer-verktyget för att få en lista över vilka åtgärder som stöds.</span><span class="sxs-lookup"><span data-stu-id="be405-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="be405-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be405-111">EXAMPLES</span></span>

## <span data-ttu-id="be405-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be405-112">PARAMETERS</span></span>

### <span data-ttu-id="be405-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="be405-113">-Action</span></span>
<span data-ttu-id="be405-114">Anger namnet på den åtgärd som ska anropas.</span><span class="sxs-lookup"><span data-stu-id="be405-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be405-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be405-115">-ApiVersion</span></span>
<span data-ttu-id="be405-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="be405-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="be405-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="be405-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="be405-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be405-118">-DefaultProfile</span></span>
<span data-ttu-id="be405-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be405-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be405-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="be405-120">-ExtensionResourceName</span></span>
<span data-ttu-id="be405-121">Anger namnet på en tilläggs resurs för den resurs där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="be405-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="be405-122">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="be405-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="be405-123">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="be405-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="be405-124">-ExtensionResourceType</span></span>
<span data-ttu-id="be405-125">Anger typen för tilläggs resursen.</span><span class="sxs-lookup"><span data-stu-id="be405-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="be405-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="be405-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-127">-Force</span><span class="sxs-lookup"><span data-stu-id="be405-127">-Force</span></span>
<span data-ttu-id="be405-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="be405-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be405-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="be405-129">-InformationAction</span></span>
<span data-ttu-id="be405-130">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="be405-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="be405-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="be405-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be405-132">Vidare</span><span class="sxs-lookup"><span data-stu-id="be405-132">Continue</span></span>
- <span data-ttu-id="be405-133">Över</span><span class="sxs-lookup"><span data-stu-id="be405-133">Ignore</span></span>
- <span data-ttu-id="be405-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="be405-134">Inquire</span></span>
- <span data-ttu-id="be405-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="be405-135">SilentlyContinue</span></span>
- <span data-ttu-id="be405-136">Stanna</span><span class="sxs-lookup"><span data-stu-id="be405-136">Stop</span></span>
- <span data-ttu-id="be405-137">Avbryt</span><span class="sxs-lookup"><span data-stu-id="be405-137">Suspend</span></span>

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

### <span data-ttu-id="be405-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be405-138">-InformationVariable</span></span>
<span data-ttu-id="be405-139">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="be405-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="be405-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="be405-140">-ODataQuery</span></span>
<span data-ttu-id="be405-141">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="be405-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="be405-142">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="be405-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="be405-143">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="be405-143">-Parameters</span></span>
<span data-ttu-id="be405-144">Anger parametrar som en hash-tabell för den åtgärd som denna cmdlet anropar.</span><span class="sxs-lookup"><span data-stu-id="be405-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be405-145">-För</span><span class="sxs-lookup"><span data-stu-id="be405-145">-Pre</span></span>
<span data-ttu-id="be405-146">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="be405-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be405-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be405-147">-ResourceGroupName</span></span>
<span data-ttu-id="be405-148">Anger namnet på en resurs grupp där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="be405-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be405-149">-ResourceId</span></span>
<span data-ttu-id="be405-150">Anger det fullständiga resurs-ID: t för resursen som denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="be405-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="be405-151">Detta ID inkluderar prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="be405-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="be405-152">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="be405-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="be405-153">-ResourceName</span></span>
<span data-ttu-id="be405-154">Anger namnet på resursen för resursen där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="be405-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="be405-155">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="be405-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="be405-156">-ResourceType</span></span>
<span data-ttu-id="be405-157">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="be405-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="be405-158">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="be405-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be405-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="be405-159">-TenantLevel</span></span>
<span data-ttu-id="be405-160">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="be405-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="be405-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be405-161">-Confirm</span></span>
<span data-ttu-id="be405-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be405-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be405-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be405-163">-WhatIf</span></span>
<span data-ttu-id="be405-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be405-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be405-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be405-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be405-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be405-166">CommonParameters</span></span>
<span data-ttu-id="be405-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be405-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be405-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be405-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be405-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be405-169">INPUTS</span></span>

### <span data-ttu-id="be405-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="be405-170">None</span></span>
<span data-ttu-id="be405-171">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="be405-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be405-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be405-172">OUTPUTS</span></span>

### <span data-ttu-id="be405-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="be405-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="be405-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be405-174">NOTES</span></span>

## <span data-ttu-id="be405-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be405-175">RELATED LINKS</span></span>
