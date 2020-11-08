---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 7a4929ffff531bb11b19b44ca9c0914c71662c8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100876"
---
# <span data-ttu-id="8c0be-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-101">Set-AzResource</span></span>

## <span data-ttu-id="8c0be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c0be-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0be-103">Ändrar en resurs.</span><span class="sxs-lookup"><span data-stu-id="8c0be-103">Modifies a resource.</span></span>

## <span data-ttu-id="8c0be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c0be-104">SYNTAX</span></span>

### <span data-ttu-id="8c0be-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="8c0be-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c0be-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0be-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8c0be-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0be-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8c0be-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c0be-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c0be-109">DESCRIPTION</span></span>
<span data-ttu-id="8c0be-110">Cmdleten **set-AzResource** ändrar en befintlig Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="8c0be-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="8c0be-111">Ange en resurs som ska ändras med namn och typ eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="8c0be-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="8c0be-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c0be-112">EXAMPLES</span></span>

### <span data-ttu-id="8c0be-113">Exempel 1: ändra en resurs</span><span class="sxs-lookup"><span data-stu-id="8c0be-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="8c0be-114">Det första kommandot får resursen som heter ContosoSite med hjälp av Get-AzResource cmdlet och lagrar den i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8c0be-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="8c0be-115">Det andra kommandot ändrar en egenskap för $Resource.</span><span class="sxs-lookup"><span data-stu-id="8c0be-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="8c0be-116">Det sista kommandot uppdaterar resursen så att den matchar $Resource.</span><span class="sxs-lookup"><span data-stu-id="8c0be-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="8c0be-117">Exempel 2: ändra alla resurser i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8c0be-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

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

<span data-ttu-id="8c0be-118">Det första kommandot får resurserna i resurs gruppen testrg och lagrar dem sedan i $Resource variabel.</span><span class="sxs-lookup"><span data-stu-id="8c0be-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="8c0be-119">Det andra kommandot upprepar de olika resurserna i resurs gruppen och lägger till en ny tagg till dem.</span><span class="sxs-lookup"><span data-stu-id="8c0be-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="8c0be-120">Det sista kommandot uppdaterar var och en av dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="8c0be-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="8c0be-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c0be-121">PARAMETERS</span></span>

### <span data-ttu-id="8c0be-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c0be-122">-ApiVersion</span></span>
<span data-ttu-id="8c0be-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8c0be-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c0be-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8c0be-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c0be-125">-AsJob</span></span>
<span data-ttu-id="8c0be-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8c0be-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c0be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0be-127">-DefaultProfile</span></span>
<span data-ttu-id="8c0be-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8c0be-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c0be-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8c0be-129">-ExtensionResourceName</span></span>
<span data-ttu-id="8c0be-130">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="8c0be-131">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="8c0be-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="8c0be-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8c0be-132">-ExtensionResourceType</span></span>
<span data-ttu-id="8c0be-133">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="8c0be-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="8c0be-134">Om tilläggs resursen till exempel är en databas anger du följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8c0be-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="8c0be-135">-Force</span><span class="sxs-lookup"><span data-stu-id="8c0be-135">-Force</span></span>
<span data-ttu-id="8c0be-136">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8c0be-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c0be-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c0be-137">-InputObject</span></span>
<span data-ttu-id="8c0be-138">Objekt representation för resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8c0be-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="8c0be-139">-Sort</span><span class="sxs-lookup"><span data-stu-id="8c0be-139">-Kind</span></span>
<span data-ttu-id="8c0be-140">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="8c0be-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8c0be-141">-ODataQuery</span></span>
<span data-ttu-id="8c0be-142">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8c0be-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8c0be-143">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="8c0be-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8c0be-144">-Planera</span><span class="sxs-lookup"><span data-stu-id="8c0be-144">-Plan</span></span>
<span data-ttu-id="8c0be-145">Anger resurs Plans egenskaper som en hash-tabell för resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="8c0be-146">-För</span><span class="sxs-lookup"><span data-stu-id="8c0be-146">-Pre</span></span>
<span data-ttu-id="8c0be-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8c0be-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8c0be-148">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="8c0be-148">-Properties</span></span>
<span data-ttu-id="8c0be-149">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="8c0be-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c0be-150">-ResourceGroupName</span></span>
<span data-ttu-id="8c0be-151">Anger namnet på resurs gruppen där denna cmdlet ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="8c0be-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c0be-152">-ResourceId</span></span>
<span data-ttu-id="8c0be-153">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8c0be-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8c0be-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8c0be-154">-ResourceName</span></span>
<span data-ttu-id="8c0be-155">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="8c0be-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="8c0be-156">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8c0be-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8c0be-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8c0be-157">-ResourceType</span></span>
<span data-ttu-id="8c0be-158">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="8c0be-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="8c0be-159">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8c0be-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="8c0be-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="8c0be-160">-Sku</span></span>
<span data-ttu-id="8c0be-161">Anger SKU-objekt för resursen som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8c0be-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="8c0be-162">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8c0be-162">-Tag</span></span>
<span data-ttu-id="8c0be-163">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8c0be-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c0be-164">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="8c0be-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8c0be-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8c0be-165">-TenantLevel</span></span>
<span data-ttu-id="8c0be-166">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="8c0be-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8c0be-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="8c0be-167">-UsePatchSemantics</span></span>
<span data-ttu-id="8c0be-168">Anger att denna cmdlet använder en HTTP-korrigering för att uppdatera objektet, i stället för ett HTTP-PUT.</span><span class="sxs-lookup"><span data-stu-id="8c0be-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="8c0be-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c0be-169">-Confirm</span></span>
<span data-ttu-id="8c0be-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c0be-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0be-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0be-171">-WhatIf</span></span>
<span data-ttu-id="8c0be-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c0be-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0be-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c0be-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0be-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0be-174">CommonParameters</span></span>
<span data-ttu-id="8c0be-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0be-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0be-176">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c0be-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0be-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c0be-177">INPUTS</span></span>

### <span data-ttu-id="8c0be-178">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="8c0be-179">System. String</span><span class="sxs-lookup"><span data-stu-id="8c0be-179">System.String</span></span>

### <span data-ttu-id="8c0be-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8c0be-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="8c0be-181">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8c0be-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8c0be-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c0be-182">OUTPUTS</span></span>

### <span data-ttu-id="8c0be-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8c0be-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8c0be-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c0be-184">NOTES</span></span>

## <span data-ttu-id="8c0be-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c0be-185">RELATED LINKS</span></span>

[<span data-ttu-id="8c0be-186">Sök-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-186">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="8c0be-187">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-187">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="8c0be-188">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-188">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8c0be-189">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-189">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8c0be-190">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8c0be-190">Remove-AzResource</span></span>](./Remove-AzResource.md)
