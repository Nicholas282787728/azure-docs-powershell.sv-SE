---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575866"
---
# <span data-ttu-id="dddf2-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="dddf2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dddf2-102">SYNOPSIS</span></span>
<span data-ttu-id="dddf2-103">Söker efter resurser baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="dddf2-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddf2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dddf2-104">SYNTAX</span></span>

### <span data-ttu-id="dddf2-105">Visar resurserna baserat på det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="dddf2-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="dddf2-106">Vis</span><span class="sxs-lookup"><span data-stu-id="dddf2-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dddf2-107">Visar de resurser som baseras på den angivna omfattningen på klient organisations nivå.</span><span class="sxs-lookup"><span data-stu-id="dddf2-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dddf2-108">Skaffa en resurs med en fråga med flera prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="dddf2-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dddf2-109">Visar en lista över resurser med ett taggattribut angivet som en HashSet.</span><span class="sxs-lookup"><span data-stu-id="dddf2-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dddf2-110">Visar en lista med resurser efter en tagg angiven som ett individuellt namn och värde parametrar.</span><span class="sxs-lookup"><span data-stu-id="dddf2-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dddf2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dddf2-111">DESCRIPTION</span></span>
<span data-ttu-id="dddf2-112">Cmdleten **find-AzureRmResource** söker efter resurser baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="dddf2-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="dddf2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dddf2-113">EXAMPLES</span></span>

### <span data-ttu-id="dddf2-114">Exempel 1: Sök efter resurser efter typ och resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="dddf2-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="dddf2-115">Det här kommandot söker efter resurser av typen Microsoft. Web/Sites under resurs grupper med namn som matchar strängen ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dddf2-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="dddf2-116">Exempel 2: Sök efter resurser efter typ och resurs namn</span><span class="sxs-lookup"><span data-stu-id="dddf2-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="dddf2-117">Det här kommandot söker efter resurser av typen Microsoft. Web/webbplatser som har ett resurs namn som matchar sträng testet.</span><span class="sxs-lookup"><span data-stu-id="dddf2-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="dddf2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dddf2-118">PARAMETERS</span></span>

### <span data-ttu-id="dddf2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dddf2-119">-ApiVersion</span></span>
<span data-ttu-id="dddf2-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="dddf2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dddf2-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="dddf2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dddf2-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="dddf2-122">-ExpandProperties</span></span>
<span data-ttu-id="dddf2-123">Anger att den här cmdleten expanderar egenskaperna för resursen.</span><span class="sxs-lookup"><span data-stu-id="dddf2-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="dddf2-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="dddf2-124">-ExtensionResourceType</span></span>
<span data-ttu-id="dddf2-125">Anger den typ av tilläggs resurs för resurser som genomsöks med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dddf2-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="dddf2-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="dddf2-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dddf2-127">-InformationAction</span></span>
<span data-ttu-id="dddf2-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="dddf2-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dddf2-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dddf2-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dddf2-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="dddf2-130">Continue</span></span>
- <span data-ttu-id="dddf2-131">Över</span><span class="sxs-lookup"><span data-stu-id="dddf2-131">Ignore</span></span>
- <span data-ttu-id="dddf2-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="dddf2-132">Inquire</span></span>
- <span data-ttu-id="dddf2-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dddf2-133">SilentlyContinue</span></span>
- <span data-ttu-id="dddf2-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="dddf2-134">Stop</span></span>
- <span data-ttu-id="dddf2-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="dddf2-135">Suspend</span></span>

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

### <span data-ttu-id="dddf2-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dddf2-136">-InformationVariable</span></span>
<span data-ttu-id="dddf2-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="dddf2-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dddf2-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="dddf2-138">-ODataQuery</span></span>
<span data-ttu-id="dddf2-139">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="dddf2-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="dddf2-140">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="dddf2-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="dddf2-141">-För</span><span class="sxs-lookup"><span data-stu-id="dddf2-141">-Pre</span></span>
<span data-ttu-id="dddf2-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="dddf2-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dddf2-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="dddf2-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="dddf2-144">Anger ett delvis namn på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dddf2-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="dddf2-145">Denna cmdlet matchar resurs grupper vars värde är en under sträng.</span><span class="sxs-lookup"><span data-stu-id="dddf2-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="dddf2-146">Cmdleten söker efter resurser i resurs grupperna.</span><span class="sxs-lookup"><span data-stu-id="dddf2-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="dddf2-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="dddf2-148">Resurs grupps namnet för en fullständig matchning.</span><span class="sxs-lookup"><span data-stu-id="dddf2-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="dddf2-149">-ResourceNameContains</span></span>
<span data-ttu-id="dddf2-150">Anger ett delvis namn på en resurs.</span><span class="sxs-lookup"><span data-stu-id="dddf2-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="dddf2-151">Cmdleten söker efter resurser som innehåller detta värde som en under sträng.</span><span class="sxs-lookup"><span data-stu-id="dddf2-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="dddf2-152">-ResourceNameEquals</span></span>
<span data-ttu-id="dddf2-153">Resurs namnet för en fullständig matchning.</span><span class="sxs-lookup"><span data-stu-id="dddf2-153">The resource name for a full match.</span></span> <span data-ttu-id="dddf2-154">till exempel: om ditt resurs namn är testResource kan du ange testResource.</span><span class="sxs-lookup"><span data-stu-id="dddf2-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dddf2-155">-ResourceType</span></span>
<span data-ttu-id="dddf2-156">Anger typen för en resurs.</span><span class="sxs-lookup"><span data-stu-id="dddf2-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="dddf2-157">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="dddf2-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="dddf2-158">Denna cmdlet söker efter resurser av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="dddf2-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dddf2-159">-Tag</span></span>
<span data-ttu-id="dddf2-160">Tag-filtret för OData-frågan.</span><span class="sxs-lookup"><span data-stu-id="dddf2-160">The tag filter for the OData query.</span></span> <span data-ttu-id="dddf2-161">Det förväntade formatet är @ {tagName = $null} eller @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="dddf2-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="dddf2-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="dddf2-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="dddf2-164">-TenantLevel</span></span>
<span data-ttu-id="dddf2-165">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="dddf2-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-166">-Överst</span><span class="sxs-lookup"><span data-stu-id="dddf2-166">-Top</span></span>
<span data-ttu-id="dddf2-167">Anger antalet resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="dddf2-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dddf2-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddf2-168">-DefaultProfile</span></span>
<span data-ttu-id="dddf2-169">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dddf2-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dddf2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddf2-170">CommonParameters</span></span>
<span data-ttu-id="dddf2-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dddf2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddf2-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddf2-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddf2-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dddf2-173">INPUTS</span></span>

## <span data-ttu-id="dddf2-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dddf2-174">OUTPUTS</span></span>

### <span data-ttu-id="dddf2-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="dddf2-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dddf2-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dddf2-176">NOTES</span></span>

## <span data-ttu-id="dddf2-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dddf2-177">RELATED LINKS</span></span>

[<span data-ttu-id="dddf2-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="dddf2-179">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="dddf2-180">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="dddf2-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="dddf2-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dddf2-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
