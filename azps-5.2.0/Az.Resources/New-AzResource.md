---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400491"
---
# <span data-ttu-id="99190-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="99190-101">New-AzResource</span></span>

## <span data-ttu-id="99190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99190-102">SYNOPSIS</span></span>
<span data-ttu-id="99190-103">Skapar en resurs.</span><span class="sxs-lookup"><span data-stu-id="99190-103">Creates a resource.</span></span>

## <span data-ttu-id="99190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99190-104">SYNTAX</span></span>

### <span data-ttu-id="99190-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="99190-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99190-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="99190-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99190-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="99190-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99190-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99190-108">DESCRIPTION</span></span>
<span data-ttu-id="99190-109">Cmdleten **New-AzResource** skapar en Azure-resurs, till exempel en webbplats, en Azure SQL-databas eller en Azure SQL-databas, i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="99190-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="99190-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99190-110">EXAMPLES</span></span>

### <span data-ttu-id="99190-111">Exempel 1: skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="99190-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="99190-112">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="99190-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="99190-113">Exempel 2: skapa en resurs med splatting</span><span class="sxs-lookup"><span data-stu-id="99190-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="99190-114">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="99190-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="99190-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99190-115">PARAMETERS</span></span>

### <span data-ttu-id="99190-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99190-116">-ApiVersion</span></span>
<span data-ttu-id="99190-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="99190-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="99190-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="99190-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="99190-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99190-119">-AsJob</span></span>
<span data-ttu-id="99190-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="99190-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99190-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99190-121">-DefaultProfile</span></span>
<span data-ttu-id="99190-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99190-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99190-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="99190-123">-ExtensionResourceName</span></span>
<span data-ttu-id="99190-124">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="99190-125">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="99190-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="99190-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="99190-126">-ExtensionResourceType</span></span>
<span data-ttu-id="99190-127">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="99190-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="99190-128">Om tilläggs resursen till exempel är en databas anger du följande typ: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="99190-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="99190-129">-Force</span><span class="sxs-lookup"><span data-stu-id="99190-129">-Force</span></span>
<span data-ttu-id="99190-130">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="99190-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99190-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="99190-131">-IsFullObject</span></span>
<span data-ttu-id="99190-132">Anger att det objekt som parametern *Egenskaper* anger är det fullständiga objektet.</span><span class="sxs-lookup"><span data-stu-id="99190-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="99190-133">-Sort</span><span class="sxs-lookup"><span data-stu-id="99190-133">-Kind</span></span>
<span data-ttu-id="99190-134">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="99190-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="99190-135">-Location</span></span>
<span data-ttu-id="99190-136">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="99190-137">Ange plats för data Center, till exempel Central USA eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="99190-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="99190-138">Du kan lägga till en resurs på alla platser som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="99190-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="99190-139">Resurs grupper kan innehålla resurser från olika platser.</span><span class="sxs-lookup"><span data-stu-id="99190-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="99190-140">Om du vill ta reda på vilka platser som har stöd för varje resurs typ använder du Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99190-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="99190-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="99190-141">-ODataQuery</span></span>
<span data-ttu-id="99190-142">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="99190-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="99190-143">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="99190-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="99190-144">-Planera</span><span class="sxs-lookup"><span data-stu-id="99190-144">-Plan</span></span>
<span data-ttu-id="99190-145">En hash-tabell som representerar egenskaper för resurs plan.</span><span class="sxs-lookup"><span data-stu-id="99190-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="99190-146">-För</span><span class="sxs-lookup"><span data-stu-id="99190-146">-Pre</span></span>
<span data-ttu-id="99190-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="99190-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="99190-148">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="99190-148">-Properties</span></span>
<span data-ttu-id="99190-149">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="99190-150">Använd den här parametern för att ange värden för egenskaper som är specifika för en resurs typ.</span><span class="sxs-lookup"><span data-stu-id="99190-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="99190-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99190-151">-ResourceGroupName</span></span>
<span data-ttu-id="99190-152">Anger namnet på resurs gruppen där denna cmdlet skapar resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="99190-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99190-153">-ResourceId</span></span>
<span data-ttu-id="99190-154">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="99190-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="99190-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="99190-155">-ResourceName</span></span>
<span data-ttu-id="99190-156">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="99190-156">Specifies the name of the resource.</span></span> <span data-ttu-id="99190-157">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="99190-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="99190-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="99190-158">-ResourceType</span></span>
<span data-ttu-id="99190-159">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="99190-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="99190-160">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="99190-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="99190-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="99190-161">-Sku</span></span>
<span data-ttu-id="99190-162">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="99190-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="99190-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="99190-163">-Tag</span></span>
<span data-ttu-id="99190-164">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="99190-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="99190-165">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="99190-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99190-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="99190-166">-TenantLevel</span></span>
<span data-ttu-id="99190-167">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="99190-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="99190-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99190-168">-Confirm</span></span>
<span data-ttu-id="99190-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99190-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99190-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99190-170">-WhatIf</span></span>
<span data-ttu-id="99190-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99190-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99190-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99190-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99190-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99190-173">CommonParameters</span></span>
<span data-ttu-id="99190-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99190-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99190-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99190-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99190-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99190-176">INPUTS</span></span>

### <span data-ttu-id="99190-177">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="99190-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="99190-178">System. String</span><span class="sxs-lookup"><span data-stu-id="99190-178">System.String</span></span>

## <span data-ttu-id="99190-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99190-179">OUTPUTS</span></span>

### <span data-ttu-id="99190-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="99190-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="99190-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99190-181">NOTES</span></span>

## <span data-ttu-id="99190-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99190-182">RELATED LINKS</span></span>

[<span data-ttu-id="99190-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="99190-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="99190-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="99190-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="99190-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="99190-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="99190-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="99190-186">Set-AzResource</span></span>](./Set-AzResource.md)
