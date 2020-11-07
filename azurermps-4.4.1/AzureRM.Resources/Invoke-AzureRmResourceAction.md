---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755427"
---
# <span data-ttu-id="8f844-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="8f844-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="8f844-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f844-102">SYNOPSIS</span></span>
<span data-ttu-id="8f844-103">Anropar en åtgärd för en resurs.</span><span class="sxs-lookup"><span data-stu-id="8f844-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f844-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f844-104">SYNTAX</span></span>

### <span data-ttu-id="8f844-105">Resurs-ID. (standard)</span><span class="sxs-lookup"><span data-stu-id="8f844-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f844-106">Resurs som finns på abonnemangs nivån.</span><span class="sxs-lookup"><span data-stu-id="8f844-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f844-107">Resurs som finns på klient nivå.</span><span class="sxs-lookup"><span data-stu-id="8f844-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f844-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f844-108">DESCRIPTION</span></span>
<span data-ttu-id="8f844-109">Cmdleten **Invoke-AzureRmResourceAction** anropar en åtgärd på en angiven Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="8f844-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="8f844-110">Använd Azure Resource Explorer-verktyget för att få en lista över vilka åtgärder som stöds.</span><span class="sxs-lookup"><span data-stu-id="8f844-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="8f844-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f844-111">EXAMPLES</span></span>

## <span data-ttu-id="8f844-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f844-112">PARAMETERS</span></span>

### <span data-ttu-id="8f844-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="8f844-113">-Action</span></span>
<span data-ttu-id="8f844-114">Anger namnet på den åtgärd som ska anropas.</span><span class="sxs-lookup"><span data-stu-id="8f844-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="8f844-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f844-115">-ApiVersion</span></span>
<span data-ttu-id="8f844-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8f844-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f844-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="8f844-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8f844-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8f844-118">-ExtensionResourceName</span></span>
<span data-ttu-id="8f844-119">Anger namnet på en tilläggs resurs för den resurs där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="8f844-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8f844-120">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="8f844-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="8f844-121">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="8f844-121">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8f844-122">-ExtensionResourceType</span></span>
<span data-ttu-id="8f844-123">Anger typen för tilläggs resursen.</span><span class="sxs-lookup"><span data-stu-id="8f844-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="8f844-124">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="8f844-124">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8f844-125">-Force</span></span>
<span data-ttu-id="8f844-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f844-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f844-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8f844-127">-InformationAction</span></span>
<span data-ttu-id="8f844-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="8f844-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8f844-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8f844-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f844-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="8f844-130">Continue</span></span>
- <span data-ttu-id="8f844-131">Över</span><span class="sxs-lookup"><span data-stu-id="8f844-131">Ignore</span></span>
- <span data-ttu-id="8f844-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="8f844-132">Inquire</span></span>
- <span data-ttu-id="8f844-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8f844-133">SilentlyContinue</span></span>
- <span data-ttu-id="8f844-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="8f844-134">Stop</span></span>
- <span data-ttu-id="8f844-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="8f844-135">Suspend</span></span>

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

### <span data-ttu-id="8f844-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8f844-136">-InformationVariable</span></span>
<span data-ttu-id="8f844-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="8f844-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8f844-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8f844-138">-ODataQuery</span></span>
<span data-ttu-id="8f844-139">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8f844-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8f844-140">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="8f844-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8f844-141">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="8f844-141">-Parameters</span></span>
<span data-ttu-id="8f844-142">Anger parametrar som en hash-tabell för den åtgärd som denna cmdlet anropar.</span><span class="sxs-lookup"><span data-stu-id="8f844-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="8f844-143">-För</span><span class="sxs-lookup"><span data-stu-id="8f844-143">-Pre</span></span>
<span data-ttu-id="8f844-144">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8f844-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8f844-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f844-145">-ResourceGroupName</span></span>
<span data-ttu-id="8f844-146">Anger namnet på en resurs grupp där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="8f844-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f844-147">-ResourceId</span></span>
<span data-ttu-id="8f844-148">Anger det fullständiga resurs-ID: t för resursen som denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="8f844-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8f844-149">Detta ID inkluderar prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="8f844-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="8f844-150">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8f844-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8f844-151">-ResourceName</span></span>
<span data-ttu-id="8f844-152">Anger namnet på resursen för resursen där denna cmdlet anropar en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="8f844-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8f844-153">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="8f844-153">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8f844-154">-ResourceType</span></span>
<span data-ttu-id="8f844-155">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="8f844-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="8f844-156">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="8f844-156">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8f844-157">-TenantLevel</span></span>
<span data-ttu-id="8f844-158">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="8f844-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f844-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f844-159">-Confirm</span></span>
<span data-ttu-id="8f844-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f844-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f844-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f844-161">-WhatIf</span></span>
<span data-ttu-id="8f844-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f844-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f844-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f844-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f844-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f844-164">-DefaultProfile</span></span>
<span data-ttu-id="8f844-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f844-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f844-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f844-166">CommonParameters</span></span>
<span data-ttu-id="8f844-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f844-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f844-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f844-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f844-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f844-169">INPUTS</span></span>

## <span data-ttu-id="8f844-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f844-170">OUTPUTS</span></span>

### <span data-ttu-id="8f844-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8f844-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f844-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f844-172">NOTES</span></span>

## <span data-ttu-id="8f844-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f844-173">RELATED LINKS</span></span>

