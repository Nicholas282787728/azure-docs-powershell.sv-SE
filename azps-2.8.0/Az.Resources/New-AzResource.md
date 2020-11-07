---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 0ccbabbb863b99aefd19b8f8a53257ac8c46faaa
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93931618"
---
# <span data-ttu-id="8a7ea-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a7ea-101">New-AzResource</span></span>

## <span data-ttu-id="8a7ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7ea-103">Skapar en resurs.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-103">Creates a resource.</span></span>

## <span data-ttu-id="8a7ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a7ea-104">SYNTAX</span></span>

### <span data-ttu-id="8a7ea-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="8a7ea-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a7ea-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8a7ea-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a7ea-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8a7ea-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a7ea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a7ea-108">DESCRIPTION</span></span>
<span data-ttu-id="8a7ea-109">Cmdleten **New-AzResource** skapar en Azure-resurs, till exempel en webbplats, en Azure SQL-databas eller en Azure SQL-databas, i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="8a7ea-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a7ea-110">EXAMPLES</span></span>

### <span data-ttu-id="8a7ea-111">Exempel 1: skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="8a7ea-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="8a7ea-112">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="8a7ea-113">Exempel 2: skapa en resurs med splatting</span><span class="sxs-lookup"><span data-stu-id="8a7ea-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="8a7ea-114">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="8a7ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a7ea-115">PARAMETERS</span></span>

### <span data-ttu-id="8a7ea-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a7ea-116">-ApiVersion</span></span>
<span data-ttu-id="8a7ea-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="8a7ea-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8a7ea-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a7ea-119">-AsJob</span></span>
<span data-ttu-id="8a7ea-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8a7ea-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a7ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7ea-121">-DefaultProfile</span></span>
<span data-ttu-id="8a7ea-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a7ea-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a7ea-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8a7ea-123">-ExtensionResourceName</span></span>
<span data-ttu-id="8a7ea-124">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="8a7ea-125">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="8a7ea-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="8a7ea-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8a7ea-126">-ExtensionResourceType</span></span>
<span data-ttu-id="8a7ea-127">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="8a7ea-128">Om tilläggs resursen till exempel är en databas anger du följande typ: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8a7ea-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="8a7ea-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8a7ea-129">-Force</span></span>
<span data-ttu-id="8a7ea-130">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a7ea-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="8a7ea-131">-IsFullObject</span></span>
<span data-ttu-id="8a7ea-132">Anger att det objekt som parametern *Egenskaper* anger är det fullständiga objektet.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="8a7ea-133">-Sort</span><span class="sxs-lookup"><span data-stu-id="8a7ea-133">-Kind</span></span>
<span data-ttu-id="8a7ea-134">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="8a7ea-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a7ea-135">-Location</span></span>
<span data-ttu-id="8a7ea-136">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="8a7ea-137">Ange plats för data Center, till exempel Central USA eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="8a7ea-138">Du kan lägga till en resurs på alla platser som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="8a7ea-139">Resurs grupper kan innehålla resurser från olika platser.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="8a7ea-140">Om du vill ta reda på vilka platser som har stöd för varje resurs typ använder du Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="8a7ea-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8a7ea-141">-ODataQuery</span></span>
<span data-ttu-id="8a7ea-142">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8a7ea-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="8a7ea-143">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8a7ea-144">-Planera</span><span class="sxs-lookup"><span data-stu-id="8a7ea-144">-Plan</span></span>
<span data-ttu-id="8a7ea-145">En hash-tabell som representerar egenskaper för resurs plan.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7ea-146">-För</span><span class="sxs-lookup"><span data-stu-id="8a7ea-146">-Pre</span></span>
<span data-ttu-id="8a7ea-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a7ea-148">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="8a7ea-148">-Properties</span></span>
<span data-ttu-id="8a7ea-149">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="8a7ea-150">Använd den här parametern för att ange värden för egenskaper som är specifika för en resurs typ.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7ea-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a7ea-151">-ResourceGroupName</span></span>
<span data-ttu-id="8a7ea-152">Anger namnet på resurs gruppen där denna cmdlet skapar resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="8a7ea-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a7ea-153">-ResourceId</span></span>
<span data-ttu-id="8a7ea-154">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8a7ea-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8a7ea-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8a7ea-155">-ResourceName</span></span>
<span data-ttu-id="8a7ea-156">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-156">Specifies the name of the resource.</span></span> <span data-ttu-id="8a7ea-157">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8a7ea-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8a7ea-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8a7ea-158">-ResourceType</span></span>
<span data-ttu-id="8a7ea-159">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="8a7ea-160">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8a7ea-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="8a7ea-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="8a7ea-161">-Sku</span></span>
<span data-ttu-id="8a7ea-162">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="8a7ea-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8a7ea-163">-Tag</span></span>
<span data-ttu-id="8a7ea-164">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a7ea-165">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="8a7ea-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7ea-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8a7ea-166">-TenantLevel</span></span>
<span data-ttu-id="8a7ea-167">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8a7ea-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a7ea-168">-Confirm</span></span>
<span data-ttu-id="8a7ea-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a7ea-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a7ea-170">-WhatIf</span></span>
<span data-ttu-id="8a7ea-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a7ea-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a7ea-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7ea-173">CommonParameters</span></span>
<span data-ttu-id="8a7ea-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a7ea-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7ea-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7ea-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7ea-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a7ea-176">INPUTS</span></span>

### <span data-ttu-id="8a7ea-177">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8a7ea-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8a7ea-178">System. String</span><span class="sxs-lookup"><span data-stu-id="8a7ea-178">System.String</span></span>

## <span data-ttu-id="8a7ea-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a7ea-179">OUTPUTS</span></span>

### <span data-ttu-id="8a7ea-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8a7ea-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8a7ea-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a7ea-181">NOTES</span></span>

## <span data-ttu-id="8a7ea-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a7ea-182">RELATED LINKS</span></span>

[<span data-ttu-id="8a7ea-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a7ea-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="8a7ea-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a7ea-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8a7ea-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a7ea-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="8a7ea-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a7ea-186">Set-AzResource</span></span>](./Set-AzResource.md)
