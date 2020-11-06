---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575533"
---
# <span data-ttu-id="a4ce9-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-101">New-AzureRmResource</span></span>

## <span data-ttu-id="a4ce9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ce9-103">Skapar en resurs.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4ce9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4ce9-104">SYNTAX</span></span>

### <span data-ttu-id="a4ce9-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="a4ce9-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4ce9-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a4ce9-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ce9-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a4ce9-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ce9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4ce9-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ce9-109">Cmdleten **New-AzureRmResource** skapar en Azure-resurs, till exempel en webbplats, en Azure SQL-databas eller en Azure SQL-databas, i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="a4ce9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4ce9-110">EXAMPLES</span></span>

### <span data-ttu-id="a4ce9-111">Exempel 1: skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="a4ce9-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="a4ce9-112">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="a4ce9-113">Exempel 2: skapa en resurs med splatting</span><span class="sxs-lookup"><span data-stu-id="a4ce9-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="a4ce9-114">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="a4ce9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4ce9-115">PARAMETERS</span></span>

### <span data-ttu-id="a4ce9-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4ce9-116">-ApiVersion</span></span>
<span data-ttu-id="a4ce9-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a4ce9-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a4ce9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4ce9-119">-AsJob</span></span>
<span data-ttu-id="a4ce9-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4ce9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4ce9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ce9-121">-DefaultProfile</span></span>
<span data-ttu-id="a4ce9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4ce9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4ce9-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a4ce9-123">-ExtensionResourceName</span></span>
<span data-ttu-id="a4ce9-124">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="a4ce9-125">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="a4ce9-126">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="a4ce9-126">server name`/`database name</span></span>

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

### <span data-ttu-id="a4ce9-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a4ce9-127">-ExtensionResourceType</span></span>
<span data-ttu-id="a4ce9-128">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a4ce9-129">Om tilläggs resursen till exempel är en databas anger du följande typ:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-129">For instance, if the extension resource is a database, specify the following type:</span></span>

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

### <span data-ttu-id="a4ce9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a4ce9-130">-Force</span></span>
<span data-ttu-id="a4ce9-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4ce9-132">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="a4ce9-132">-IsFullObject</span></span>
<span data-ttu-id="a4ce9-133">Anger att det objekt som parametern *Egenskaper* anger är det fullständiga objektet.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="a4ce9-134">-Sort</span><span class="sxs-lookup"><span data-stu-id="a4ce9-134">-Kind</span></span>
<span data-ttu-id="a4ce9-135">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-135">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a4ce9-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4ce9-136">-Location</span></span>
<span data-ttu-id="a4ce9-137">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="a4ce9-138">Ange plats för data Center, till exempel Central USA eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="a4ce9-139">Du kan lägga till en resurs på alla platser som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="a4ce9-140">Resurs grupper kan innehålla resurser från olika platser.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="a4ce9-141">Om du vill ta reda på vilka platser som har stöd för varje resurs typ använder du Get-AzureLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="a4ce9-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a4ce9-142">-ODataQuery</span></span>
<span data-ttu-id="a4ce9-143">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a4ce9-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="a4ce9-144">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a4ce9-145">-Planera</span><span class="sxs-lookup"><span data-stu-id="a4ce9-145">-Plan</span></span>
<span data-ttu-id="a4ce9-146">En hash-tabell som representerar egenskaper för resurs plan.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ce9-147">-För</span><span class="sxs-lookup"><span data-stu-id="a4ce9-147">-Pre</span></span>
<span data-ttu-id="a4ce9-148">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a4ce9-149">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="a4ce9-149">-Properties</span></span>
<span data-ttu-id="a4ce9-150">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="a4ce9-151">Använd den här parametern för att ange värden för egenskaper som är specifika för en resurs typ.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ce9-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ce9-152">-ResourceGroupName</span></span>
<span data-ttu-id="a4ce9-153">Anger namnet på resurs gruppen där denna cmdlet skapar resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="a4ce9-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ce9-154">-ResourceId</span></span>
<span data-ttu-id="a4ce9-155">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="a4ce9-156">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a4ce9-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a4ce9-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4ce9-157">-ResourceName</span></span>
<span data-ttu-id="a4ce9-158">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-158">Specifies the name of the resource.</span></span> <span data-ttu-id="a4ce9-159">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-159">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="a4ce9-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a4ce9-160">-ResourceType</span></span>
<span data-ttu-id="a4ce9-161">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="a4ce9-162">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-162">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="a4ce9-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="a4ce9-163">-Sku</span></span>
<span data-ttu-id="a4ce9-164">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ce9-165">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a4ce9-165">-Tag</span></span>
<span data-ttu-id="a4ce9-166">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a4ce9-167">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="a4ce9-167">For example:</span></span>

<span data-ttu-id="a4ce9-168">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a4ce9-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ce9-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a4ce9-169">-TenantLevel</span></span>
<span data-ttu-id="a4ce9-170">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-170">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a4ce9-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4ce9-171">-Confirm</span></span>
<span data-ttu-id="a4ce9-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ce9-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ce9-173">-WhatIf</span></span>
<span data-ttu-id="a4ce9-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ce9-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ce9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ce9-176">CommonParameters</span></span>
<span data-ttu-id="a4ce9-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ce9-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ce9-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ce9-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4ce9-179">INPUTS</span></span>

### <span data-ttu-id="a4ce9-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4ce9-180">None</span></span>
<span data-ttu-id="a4ce9-181">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a4ce9-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4ce9-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4ce9-182">OUTPUTS</span></span>

### <span data-ttu-id="a4ce9-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a4ce9-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a4ce9-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4ce9-184">NOTES</span></span>

## <span data-ttu-id="a4ce9-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4ce9-185">RELATED LINKS</span></span>

[<span data-ttu-id="a4ce9-186">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="a4ce9-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="a4ce9-188">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="a4ce9-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="a4ce9-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4ce9-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
