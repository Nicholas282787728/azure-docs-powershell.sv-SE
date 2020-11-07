---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755323"
---
# <span data-ttu-id="50389-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-101">New-AzureRmResource</span></span>

## <span data-ttu-id="50389-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50389-102">SYNOPSIS</span></span>
<span data-ttu-id="50389-103">Skapar en resurs.</span><span class="sxs-lookup"><span data-stu-id="50389-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50389-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50389-104">SYNTAX</span></span>

### <span data-ttu-id="50389-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="50389-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50389-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="50389-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50389-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="50389-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50389-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50389-108">DESCRIPTION</span></span>
<span data-ttu-id="50389-109">Cmdleten **New-AzureRmResource** skapar en Azure-resurs, till exempel en webbplats, en Azure SQL-databas eller en Azure SQL-databas, i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="50389-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="50389-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50389-110">EXAMPLES</span></span>

### <span data-ttu-id="50389-111">Exempel 1: skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="50389-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="50389-112">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="50389-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="50389-113">Exempel 2: skapa en resurs med splatting</span><span class="sxs-lookup"><span data-stu-id="50389-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="50389-114">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="50389-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="50389-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50389-115">PARAMETERS</span></span>

### <span data-ttu-id="50389-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50389-116">-ApiVersion</span></span>
<span data-ttu-id="50389-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="50389-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="50389-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="50389-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="50389-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50389-119">-AsJob</span></span>
<span data-ttu-id="50389-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50389-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50389-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50389-121">-DefaultProfile</span></span>
<span data-ttu-id="50389-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50389-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50389-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="50389-123">-ExtensionResourceName</span></span>
<span data-ttu-id="50389-124">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="50389-125">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="50389-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="50389-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="50389-126">-ExtensionResourceType</span></span>
<span data-ttu-id="50389-127">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="50389-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="50389-128">Om tilläggs resursen till exempel är en databas anger du följande typ: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="50389-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="50389-129">-Force</span><span class="sxs-lookup"><span data-stu-id="50389-129">-Force</span></span>
<span data-ttu-id="50389-130">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50389-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50389-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="50389-131">-IsFullObject</span></span>
<span data-ttu-id="50389-132">Anger att det objekt som parametern *Egenskaper* anger är det fullständiga objektet.</span><span class="sxs-lookup"><span data-stu-id="50389-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="50389-133">-Sort</span><span class="sxs-lookup"><span data-stu-id="50389-133">-Kind</span></span>
<span data-ttu-id="50389-134">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="50389-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="50389-135">-Location</span></span>
<span data-ttu-id="50389-136">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="50389-137">Ange plats för data Center, till exempel Central USA eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="50389-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="50389-138">Du kan lägga till en resurs på alla platser som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="50389-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="50389-139">Resurs grupper kan innehålla resurser från olika platser.</span><span class="sxs-lookup"><span data-stu-id="50389-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="50389-140">Om du vill ta reda på vilka platser som har stöd för varje resurs typ använder du Get-AzureLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50389-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="50389-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="50389-141">-ODataQuery</span></span>
<span data-ttu-id="50389-142">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="50389-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="50389-143">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="50389-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="50389-144">-Planera</span><span class="sxs-lookup"><span data-stu-id="50389-144">-Plan</span></span>
<span data-ttu-id="50389-145">En hash-tabell som representerar egenskaper för resurs plan.</span><span class="sxs-lookup"><span data-stu-id="50389-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="50389-146">-För</span><span class="sxs-lookup"><span data-stu-id="50389-146">-Pre</span></span>
<span data-ttu-id="50389-147">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="50389-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="50389-148">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="50389-148">-Properties</span></span>
<span data-ttu-id="50389-149">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="50389-150">Använd den här parametern för att ange värden för egenskaper som är specifika för en resurs typ.</span><span class="sxs-lookup"><span data-stu-id="50389-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="50389-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50389-151">-ResourceGroupName</span></span>
<span data-ttu-id="50389-152">Anger namnet på resurs gruppen där denna cmdlet skapar resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="50389-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50389-153">-ResourceId</span></span>
<span data-ttu-id="50389-154">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="50389-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="50389-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="50389-155">-ResourceName</span></span>
<span data-ttu-id="50389-156">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="50389-156">Specifies the name of the resource.</span></span> <span data-ttu-id="50389-157">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="50389-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="50389-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="50389-158">-ResourceType</span></span>
<span data-ttu-id="50389-159">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="50389-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="50389-160">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="50389-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="50389-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="50389-161">-Sku</span></span>
<span data-ttu-id="50389-162">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="50389-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="50389-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="50389-163">-Tag</span></span>
<span data-ttu-id="50389-164">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="50389-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="50389-165">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="50389-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="50389-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="50389-166">-TenantLevel</span></span>
<span data-ttu-id="50389-167">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="50389-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="50389-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50389-168">-Confirm</span></span>
<span data-ttu-id="50389-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50389-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50389-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50389-170">-WhatIf</span></span>
<span data-ttu-id="50389-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50389-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50389-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50389-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50389-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50389-173">CommonParameters</span></span>
<span data-ttu-id="50389-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50389-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50389-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50389-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50389-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50389-176">INPUTS</span></span>

### <span data-ttu-id="50389-177">Ingen</span><span class="sxs-lookup"><span data-stu-id="50389-177">None</span></span>

## <span data-ttu-id="50389-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50389-178">OUTPUTS</span></span>

### <span data-ttu-id="50389-179">Microsoft. Azure. commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="50389-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="50389-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50389-180">NOTES</span></span>

## <span data-ttu-id="50389-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50389-181">RELATED LINKS</span></span>

[<span data-ttu-id="50389-182">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-182">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="50389-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="50389-184">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="50389-185">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-185">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="50389-186">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="50389-186">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
