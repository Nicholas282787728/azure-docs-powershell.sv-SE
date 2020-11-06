---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582219"
---
# <span data-ttu-id="ef982-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-101">New-AzureRmResource</span></span>

## <span data-ttu-id="ef982-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef982-102">SYNOPSIS</span></span>
<span data-ttu-id="ef982-103">Skapar en resurs.</span><span class="sxs-lookup"><span data-stu-id="ef982-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef982-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef982-104">SYNTAX</span></span>

### <span data-ttu-id="ef982-105">Resurs-ID. (standard)</span><span class="sxs-lookup"><span data-stu-id="ef982-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef982-106">Resurs som finns på abonnemangs nivån.</span><span class="sxs-lookup"><span data-stu-id="ef982-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef982-107">Resurs som finns på klient nivå.</span><span class="sxs-lookup"><span data-stu-id="ef982-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef982-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef982-108">DESCRIPTION</span></span>
<span data-ttu-id="ef982-109">Cmdleten **New-AzureRmResource** skapar en Azure-resurs, till exempel en webbplats, en Azure SQL-databas eller en Azure SQL-databas, i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ef982-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="ef982-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef982-110">EXAMPLES</span></span>

### <span data-ttu-id="ef982-111">Exempel 1: skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="ef982-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="ef982-112">Det här kommandot skapar en resurs som är en webbplats i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ef982-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="ef982-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef982-113">PARAMETERS</span></span>

### <span data-ttu-id="ef982-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef982-114">-ApiVersion</span></span>
<span data-ttu-id="ef982-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ef982-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="ef982-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ef982-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef982-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ef982-117">-ExtensionResourceName</span></span>
<span data-ttu-id="ef982-118">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="ef982-119">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="ef982-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="ef982-120">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="ef982-120">server name`/`database name</span></span>

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

### <span data-ttu-id="ef982-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ef982-121">-ExtensionResourceType</span></span>
<span data-ttu-id="ef982-122">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="ef982-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="ef982-123">Om tilläggs resursen till exempel är en databas anger du följande typ:</span><span class="sxs-lookup"><span data-stu-id="ef982-123">For instance, if the extension resource is a database, specify the following type:</span></span>

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

### <span data-ttu-id="ef982-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ef982-124">-Force</span></span>
<span data-ttu-id="ef982-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ef982-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef982-126">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="ef982-126">-IsFullObject</span></span>
<span data-ttu-id="ef982-127">Anger att det objekt som parametern *Egenskaper* anger är det fullständiga objektet.</span><span class="sxs-lookup"><span data-stu-id="ef982-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="ef982-128">-Sort</span><span class="sxs-lookup"><span data-stu-id="ef982-128">-Kind</span></span>
<span data-ttu-id="ef982-129">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="ef982-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="ef982-130">-Location</span></span>
<span data-ttu-id="ef982-131">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="ef982-132">Ange plats för data Center, till exempel Central USA eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="ef982-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="ef982-133">Du kan lägga till en resurs på alla platser som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="ef982-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="ef982-134">Resurs grupper kan innehålla resurser från olika platser.</span><span class="sxs-lookup"><span data-stu-id="ef982-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="ef982-135">Om du vill ta reda på vilka platser som har stöd för varje resurs typ använder du Get-AzureLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef982-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="ef982-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ef982-136">-ODataQuery</span></span>
<span data-ttu-id="ef982-137">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ef982-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="ef982-138">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="ef982-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ef982-139">-Planera</span><span class="sxs-lookup"><span data-stu-id="ef982-139">-Plan</span></span>
<span data-ttu-id="ef982-140">En hash-tabell som representerar egenskaper för resurs plan.</span><span class="sxs-lookup"><span data-stu-id="ef982-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="ef982-141">-För</span><span class="sxs-lookup"><span data-stu-id="ef982-141">-Pre</span></span>
<span data-ttu-id="ef982-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ef982-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef982-143">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="ef982-143">-Properties</span></span>
<span data-ttu-id="ef982-144">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="ef982-145">Använd den här parametern för att ange värden för egenskaper som är specifika för en resurs typ.</span><span class="sxs-lookup"><span data-stu-id="ef982-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="ef982-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef982-146">-ResourceGroupName</span></span>
<span data-ttu-id="ef982-147">Anger namnet på resurs gruppen där denna cmdlet skapar resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="ef982-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef982-148">-ResourceId</span></span>
<span data-ttu-id="ef982-149">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="ef982-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="ef982-150">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ef982-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ef982-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef982-151">-ResourceName</span></span>
<span data-ttu-id="ef982-152">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="ef982-152">Specifies the name of the resource.</span></span> <span data-ttu-id="ef982-153">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="ef982-153">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="ef982-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef982-154">-ResourceType</span></span>
<span data-ttu-id="ef982-155">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="ef982-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="ef982-156">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="ef982-156">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="ef982-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="ef982-157">-Sku</span></span>
<span data-ttu-id="ef982-158">En hash-tabell som representerar SKU-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ef982-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="ef982-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ef982-159">-Tag</span></span>
<span data-ttu-id="ef982-160">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ef982-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef982-161">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ef982-161">For example:</span></span>

<span data-ttu-id="ef982-162">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ef982-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ef982-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef982-163">-TenantLevel</span></span>
<span data-ttu-id="ef982-164">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="ef982-164">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ef982-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef982-165">-Confirm</span></span>
<span data-ttu-id="ef982-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef982-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef982-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef982-167">-WhatIf</span></span>
<span data-ttu-id="ef982-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef982-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef982-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef982-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef982-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef982-170">-DefaultProfile</span></span>
<span data-ttu-id="ef982-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef982-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef982-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef982-172">CommonParameters</span></span>
<span data-ttu-id="ef982-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef982-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef982-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef982-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef982-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef982-175">INPUTS</span></span>

## <span data-ttu-id="ef982-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef982-176">OUTPUTS</span></span>

### <span data-ttu-id="ef982-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ef982-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ef982-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef982-178">NOTES</span></span>

## <span data-ttu-id="ef982-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef982-179">RELATED LINKS</span></span>

[<span data-ttu-id="ef982-180">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="ef982-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ef982-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ef982-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ef982-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef982-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
