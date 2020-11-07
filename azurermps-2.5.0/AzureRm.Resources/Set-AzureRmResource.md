---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
ms.openlocfilehash: 6d243cccb5f5a64ef0275da1020222416c491ee3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929613"
---
# <span data-ttu-id="a8113-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a8113-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="a8113-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8113-102">SYNOPSIS</span></span>
<span data-ttu-id="a8113-103">Ändrar en resurs.</span><span class="sxs-lookup"><span data-stu-id="a8113-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8113-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8113-104">SYNTAX</span></span>

### <span data-ttu-id="a8113-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="a8113-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8113-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8113-106">ByInputObject</span></span>
```
Set-AzureRmResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8113-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a8113-107">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8113-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a8113-108">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8113-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8113-109">DESCRIPTION</span></span>
<span data-ttu-id="a8113-110">Cmdleten **set-AzureRmResource** ändrar en befintlig Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="a8113-110">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="a8113-111">Ange en resurs som ska ändras med namn och typ eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="a8113-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="a8113-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8113-112">EXAMPLES</span></span>

### <span data-ttu-id="a8113-113">Exempel 1: ändra en resurs</span><span class="sxs-lookup"><span data-stu-id="a8113-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="a8113-114">Det första kommandot får resursen som heter ContosoSite med hjälp av Get-AzureRmResource cmdlet och lagrar den i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a8113-114">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="a8113-115">Det andra kommandot ändrar en egenskap för $Resource.</span><span class="sxs-lookup"><span data-stu-id="a8113-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="a8113-116">Det sista kommandot uppdaterar resursen så att den matchar $Resource.</span><span class="sxs-lookup"><span data-stu-id="a8113-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="a8113-117">Exempel 2: ändra alla resurser i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a8113-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzureRmResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="a8113-118">Det första kommandot får resurserna i resurs gruppen testrg och lagrar dem sedan i $Resource variabel.</span><span class="sxs-lookup"><span data-stu-id="a8113-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="a8113-119">Det andra kommandot upprepar de olika resurserna i resurs gruppen och lägger till en ny tagg till dem.</span><span class="sxs-lookup"><span data-stu-id="a8113-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="a8113-120">Det sista kommandot uppdaterar var och en av dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="a8113-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="a8113-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8113-121">PARAMETERS</span></span>

### <span data-ttu-id="a8113-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a8113-122">-ApiVersion</span></span>
<span data-ttu-id="a8113-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a8113-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a8113-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a8113-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a8113-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8113-125">-AsJob</span></span>
<span data-ttu-id="a8113-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a8113-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8113-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8113-127">-DefaultProfile</span></span>
<span data-ttu-id="a8113-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a8113-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8113-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a8113-129">-ExtensionResourceName</span></span>
<span data-ttu-id="a8113-130">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="a8113-131">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="a8113-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a8113-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a8113-132">-ExtensionResourceType</span></span>
<span data-ttu-id="a8113-133">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="a8113-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a8113-134">Om tilläggs resursen till exempel är en databas anger du följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a8113-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a8113-135">-Force</span><span class="sxs-lookup"><span data-stu-id="a8113-135">-Force</span></span>
<span data-ttu-id="a8113-136">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a8113-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8113-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8113-137">-InputObject</span></span>
<span data-ttu-id="a8113-138">Objekt representation för resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a8113-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-139">-Sort</span><span class="sxs-lookup"><span data-stu-id="a8113-139">-Kind</span></span>
<span data-ttu-id="a8113-140">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a8113-141">-ODataQuery</span></span>
<span data-ttu-id="a8113-142">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a8113-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="a8113-143">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="a8113-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a8113-144">-Planera</span><span class="sxs-lookup"><span data-stu-id="a8113-144">-Plan</span></span>
<span data-ttu-id="a8113-145">Anger resurs Plans egenskaper som en hash-tabell för resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-146">-För</span><span class="sxs-lookup"><span data-stu-id="a8113-146">-Pre</span></span>
<span data-ttu-id="a8113-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a8113-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a8113-148">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="a8113-148">-Properties</span></span>
<span data-ttu-id="a8113-149">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8113-150">-ResourceGroupName</span></span>
<span data-ttu-id="a8113-151">Anger namnet på resurs gruppen där denna cmdlet ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="a8113-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8113-152">-ResourceId</span></span>
<span data-ttu-id="a8113-153">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a8113-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a8113-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a8113-154">-ResourceName</span></span>
<span data-ttu-id="a8113-155">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="a8113-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="a8113-156">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a8113-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a8113-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a8113-157">-ResourceType</span></span>
<span data-ttu-id="a8113-158">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="a8113-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="a8113-159">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a8113-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a8113-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="a8113-160">-Sku</span></span>
<span data-ttu-id="a8113-161">Anger SKU-objekt för resursen som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8113-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-162">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a8113-162">-Tag</span></span>
<span data-ttu-id="a8113-163">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8113-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a8113-164">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a8113-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8113-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a8113-165">-TenantLevel</span></span>
<span data-ttu-id="a8113-166">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="a8113-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a8113-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="a8113-167">-UsePatchSemantics</span></span>
<span data-ttu-id="a8113-168">Anger att denna cmdlet använder en HTTP-korrigering för att uppdatera objektet, i stället för ett HTTP-PUT.</span><span class="sxs-lookup"><span data-stu-id="a8113-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="a8113-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8113-169">-Confirm</span></span>
<span data-ttu-id="a8113-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8113-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8113-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8113-171">-WhatIf</span></span>
<span data-ttu-id="a8113-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8113-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8113-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8113-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8113-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8113-174">CommonParameters</span></span>
<span data-ttu-id="a8113-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8113-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8113-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8113-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8113-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8113-177">INPUTS</span></span>

### <span data-ttu-id="a8113-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="a8113-178">None</span></span>

## <span data-ttu-id="a8113-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8113-179">OUTPUTS</span></span>

### <span data-ttu-id="a8113-180">Microsoft. Azure. commands. ResourceManager. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="a8113-180">Microsoft.Azure.Commands.ResourceManager.Models.PSResource</span></span>

## <span data-ttu-id="a8113-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8113-181">NOTES</span></span>

## <span data-ttu-id="a8113-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8113-182">RELATED LINKS</span></span>



[<span data-ttu-id="a8113-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a8113-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="a8113-184">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a8113-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="a8113-185">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a8113-185">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a8113-186">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a8113-186">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
