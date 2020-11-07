---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757230"
---
# <span data-ttu-id="f3fab-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="f3fab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3fab-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fab-103">Ändrar en resurs.</span><span class="sxs-lookup"><span data-stu-id="f3fab-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3fab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3fab-104">SYNTAX</span></span>

### <span data-ttu-id="f3fab-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="f3fab-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3fab-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f3fab-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3fab-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3fab-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3fab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3fab-108">DESCRIPTION</span></span>
<span data-ttu-id="f3fab-109">Cmdleten **set-AzureRmResource** ändrar en befintlig Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="f3fab-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="f3fab-110">Ange en resurs som ska ändras med namn och typ eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="f3fab-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="f3fab-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3fab-111">EXAMPLES</span></span>

### <span data-ttu-id="f3fab-112">Exempel 1: ändra en resurs</span><span class="sxs-lookup"><span data-stu-id="f3fab-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="f3fab-113">Det första kommandot får resursen som heter ContosoSite med hjälp av Get-AzureRmResource cmdlet och lagrar den i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f3fab-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="f3fab-114">Det andra kommandot ändrar en egenskap för $Resource.</span><span class="sxs-lookup"><span data-stu-id="f3fab-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="f3fab-115">Det sista kommandot uppdaterar resursen så att den matchar $Resource.</span><span class="sxs-lookup"><span data-stu-id="f3fab-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="f3fab-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3fab-116">PARAMETERS</span></span>

### <span data-ttu-id="f3fab-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3fab-117">-ApiVersion</span></span>
<span data-ttu-id="f3fab-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f3fab-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f3fab-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f3fab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3fab-120">-AsJob</span></span>
<span data-ttu-id="f3fab-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f3fab-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3fab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fab-122">-DefaultProfile</span></span>
<span data-ttu-id="f3fab-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3fab-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3fab-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f3fab-124">-ExtensionResourceName</span></span>
<span data-ttu-id="f3fab-125">Anger namnet på en tilläggs resurs för resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="f3fab-126">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="f3fab-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="f3fab-127">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="f3fab-127">server name`/`database name</span></span>

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

### <span data-ttu-id="f3fab-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f3fab-128">-ExtensionResourceType</span></span>
<span data-ttu-id="f3fab-129">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="f3fab-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="f3fab-130">Om tilläggs resursen till exempel är en databas anger du följande:</span><span class="sxs-lookup"><span data-stu-id="f3fab-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="f3fab-131">-Force</span><span class="sxs-lookup"><span data-stu-id="f3fab-131">-Force</span></span>
<span data-ttu-id="f3fab-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f3fab-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3fab-133">-Sort</span><span class="sxs-lookup"><span data-stu-id="f3fab-133">-Kind</span></span>
<span data-ttu-id="f3fab-134">Anger resurs typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fab-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f3fab-135">-ODataQuery</span></span>
<span data-ttu-id="f3fab-136">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="f3fab-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f3fab-137">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="f3fab-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="f3fab-138">-Planera</span><span class="sxs-lookup"><span data-stu-id="f3fab-138">-Plan</span></span>
<span data-ttu-id="f3fab-139">Anger resurs Plans egenskaper som en hash-tabell för resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fab-140">-För</span><span class="sxs-lookup"><span data-stu-id="f3fab-140">-Pre</span></span>
<span data-ttu-id="f3fab-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f3fab-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3fab-142">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="f3fab-142">-Properties</span></span>
<span data-ttu-id="f3fab-143">Anger resurs egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fab-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fab-144">-ResourceGroupName</span></span>
<span data-ttu-id="f3fab-145">Anger namnet på resurs gruppen där denna cmdlet ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="f3fab-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3fab-146">-ResourceId</span></span>
<span data-ttu-id="f3fab-147">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="f3fab-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="f3fab-148">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f3fab-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f3fab-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3fab-149">-ResourceName</span></span>
<span data-ttu-id="f3fab-150">Anger namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="f3fab-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="f3fab-151">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="f3fab-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="f3fab-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3fab-152">-ResourceType</span></span>
<span data-ttu-id="f3fab-153">Anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="f3fab-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="f3fab-154">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="f3fab-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="f3fab-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="f3fab-155">-Sku</span></span>
<span data-ttu-id="f3fab-156">Anger SKU-objekt för resursen som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f3fab-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="f3fab-157">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f3fab-157">-Tag</span></span>
<span data-ttu-id="f3fab-158">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f3fab-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f3fab-159">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="f3fab-159">For example:</span></span>

<span data-ttu-id="f3fab-160">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f3fab-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fab-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3fab-161">-TenantLevel</span></span>
<span data-ttu-id="f3fab-162">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="f3fab-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f3fab-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="f3fab-163">-UsePatchSemantics</span></span>
<span data-ttu-id="f3fab-164">Anger att denna cmdlet använder en HTTP-korrigering för att uppdatera objektet, i stället för ett HTTP-PUT.</span><span class="sxs-lookup"><span data-stu-id="f3fab-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="f3fab-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3fab-165">-Confirm</span></span>
<span data-ttu-id="f3fab-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3fab-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3fab-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3fab-167">-WhatIf</span></span>
<span data-ttu-id="f3fab-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3fab-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3fab-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3fab-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3fab-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fab-170">CommonParameters</span></span>
<span data-ttu-id="f3fab-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fab-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fab-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3fab-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fab-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3fab-173">INPUTS</span></span>

### <span data-ttu-id="f3fab-174">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3fab-174">None</span></span>
<span data-ttu-id="f3fab-175">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f3fab-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3fab-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3fab-176">OUTPUTS</span></span>

### <span data-ttu-id="f3fab-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f3fab-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f3fab-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3fab-178">NOTES</span></span>

## <span data-ttu-id="f3fab-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3fab-179">RELATED LINKS</span></span>

[<span data-ttu-id="f3fab-180">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="f3fab-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="f3fab-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="f3fab-183">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f3fab-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f3fab-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
