---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757464"
---
# <span data-ttu-id="da39d-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="da39d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da39d-102">SYNOPSIS</span></span>
<span data-ttu-id="da39d-103">Ändrar en resurs.</span><span class="sxs-lookup"><span data-stu-id="da39d-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da39d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da39d-104">SYNTAX</span></span>

### <span data-ttu-id="da39d-105">Resurs-ID. (standard)</span><span class="sxs-lookup"><span data-stu-id="da39d-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da39d-106">Resurs som finns på abonnemangs nivån.</span><span class="sxs-lookup"><span data-stu-id="da39d-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da39d-107">Resurs som finns på klient nivå.</span><span class="sxs-lookup"><span data-stu-id="da39d-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da39d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da39d-108">DESCRIPTION</span></span>
<span data-ttu-id="da39d-109">Cmdleten **set-AzureRmResource** ändrar en befintlig Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="da39d-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="da39d-110">Ange en resurs som ska ändras med namn och typ eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="da39d-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="da39d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da39d-111">EXAMPLES</span></span>

### <span data-ttu-id="da39d-112">Exempel 1: ändra en resurs</span><span class="sxs-lookup"><span data-stu-id="da39d-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="da39d-113">Det första kommandot får resursen som heter ContosoSite med hjälp av Get-AzureRmResource cmdlet och lagrar den i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="da39d-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="da39d-114">Det andra kommandot ändrar en egenskap för $Resource.</span><span class="sxs-lookup"><span data-stu-id="da39d-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="da39d-115">Det sista kommandot uppdaterar resursen så att den matchar $Resource.</span><span class="sxs-lookup"><span data-stu-id="da39d-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="da39d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da39d-116">PARAMETERS</span></span>

### <span data-ttu-id="da39d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da39d-117">-ApiVersion</span></span>
<span data-ttu-id="da39d-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="da39d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="da39d-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="da39d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="da39d-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="da39d-120">-ExtensionResourceName</span></span>
<span data-ttu-id="da39d-121">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="da39d-122">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="da39d-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="da39d-123">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="da39d-123">server name`/`database name</span></span>

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

### <span data-ttu-id="da39d-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="da39d-124">-ExtensionResourceType</span></span>
<span data-ttu-id="da39d-125">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="da39d-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="da39d-126">Om tilläggs resursen till exempel är en databas anger du följande:</span><span class="sxs-lookup"><span data-stu-id="da39d-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="da39d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="da39d-127">-Force</span></span>
<span data-ttu-id="da39d-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="da39d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da39d-129">-Sort</span><span class="sxs-lookup"><span data-stu-id="da39d-129">-Kind</span></span>
<span data-ttu-id="da39d-130">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="da39d-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="da39d-131">-ODataQuery</span></span>
<span data-ttu-id="da39d-132">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="da39d-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="da39d-133">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="da39d-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="da39d-134">-Planera</span><span class="sxs-lookup"><span data-stu-id="da39d-134">-Plan</span></span>
<span data-ttu-id="da39d-135">Anger resurs Plans egenskaper som en hash-tabell för resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="da39d-136">-För</span><span class="sxs-lookup"><span data-stu-id="da39d-136">-Pre</span></span>
<span data-ttu-id="da39d-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="da39d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da39d-138">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="da39d-138">-Properties</span></span>
<span data-ttu-id="da39d-139">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="da39d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da39d-140">-ResourceGroupName</span></span>
<span data-ttu-id="da39d-141">Anger namnet på resurs gruppen där denna cmdlet ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="da39d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da39d-142">-ResourceId</span></span>
<span data-ttu-id="da39d-143">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="da39d-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="da39d-144">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="da39d-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="da39d-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="da39d-145">-ResourceName</span></span>
<span data-ttu-id="da39d-146">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="da39d-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="da39d-147">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="da39d-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="da39d-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="da39d-148">-ResourceType</span></span>
<span data-ttu-id="da39d-149">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="da39d-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="da39d-150">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="da39d-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="da39d-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="da39d-151">-Sku</span></span>
<span data-ttu-id="da39d-152">Anger SKU-objekt för resursen som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da39d-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="da39d-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="da39d-153">-Tag</span></span>
<span data-ttu-id="da39d-154">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da39d-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da39d-155">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="da39d-155">For example:</span></span>

<span data-ttu-id="da39d-156">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="da39d-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da39d-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="da39d-157">-TenantLevel</span></span>
<span data-ttu-id="da39d-158">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="da39d-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="da39d-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="da39d-159">-UsePatchSemantics</span></span>
<span data-ttu-id="da39d-160">Anger att denna cmdlet använder en HTTP-korrigering för att uppdatera objektet, i stället för ett HTTP-PUT.</span><span class="sxs-lookup"><span data-stu-id="da39d-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="da39d-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da39d-161">-Confirm</span></span>
<span data-ttu-id="da39d-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da39d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da39d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da39d-163">-WhatIf</span></span>
<span data-ttu-id="da39d-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da39d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da39d-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da39d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da39d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da39d-166">-DefaultProfile</span></span>
<span data-ttu-id="da39d-167">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da39d-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da39d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da39d-168">CommonParameters</span></span>
<span data-ttu-id="da39d-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da39d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da39d-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da39d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da39d-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da39d-171">INPUTS</span></span>

## <span data-ttu-id="da39d-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da39d-172">OUTPUTS</span></span>

### <span data-ttu-id="da39d-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="da39d-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="da39d-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da39d-174">NOTES</span></span>

## <span data-ttu-id="da39d-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da39d-175">RELATED LINKS</span></span>

[<span data-ttu-id="da39d-176">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="da39d-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="da39d-178">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="da39d-179">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="da39d-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da39d-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
