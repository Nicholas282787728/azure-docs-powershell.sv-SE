---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579452"
---
# <span data-ttu-id="ccc26-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="ccc26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccc26-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc26-103">Söker efter resurser baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="ccc26-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccc26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccc26-104">SYNTAX</span></span>

### <span data-ttu-id="ccc26-105">GetBySpecifiedScope (standard)</span><span class="sxs-lookup"><span data-stu-id="ccc26-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccc26-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ccc26-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccc26-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="ccc26-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccc26-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="ccc26-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccc26-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="ccc26-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ccc26-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccc26-110">DESCRIPTION</span></span>
<span data-ttu-id="ccc26-111">Cmdleten **find-AzureRmResource** söker efter resurser baserat på angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="ccc26-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="ccc26-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccc26-112">EXAMPLES</span></span>

### <span data-ttu-id="ccc26-113">Exempel 1: Sök efter resurser efter typ och resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="ccc26-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="ccc26-114">Det här kommandot söker efter resurser av typen Microsoft. Web/Sites under resurs grupper med namn som matchar strängen ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ccc26-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="ccc26-115">Exempel 2: Sök efter resurser efter typ och resurs namn</span><span class="sxs-lookup"><span data-stu-id="ccc26-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="ccc26-116">Det här kommandot söker efter resurser av typen Microsoft. Web/webbplatser som har ett resurs namn som matchar sträng testet.</span><span class="sxs-lookup"><span data-stu-id="ccc26-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="ccc26-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccc26-117">PARAMETERS</span></span>

### <span data-ttu-id="ccc26-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ccc26-118">-ApiVersion</span></span>
<span data-ttu-id="ccc26-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ccc26-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ccc26-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ccc26-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ccc26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc26-121">-DefaultProfile</span></span>
<span data-ttu-id="ccc26-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ccc26-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccc26-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="ccc26-123">-ExpandProperties</span></span>
<span data-ttu-id="ccc26-124">Anger att den här cmdleten expanderar egenskaperna för resursen.</span><span class="sxs-lookup"><span data-stu-id="ccc26-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="ccc26-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ccc26-125">-ExtensionResourceType</span></span>
<span data-ttu-id="ccc26-126">Anger den typ av tilläggs resurs för resurser som genomsöks med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccc26-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="ccc26-127">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ccc26-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ccc26-128">-InformationAction</span></span>
<span data-ttu-id="ccc26-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ccc26-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ccc26-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ccc26-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccc26-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="ccc26-131">Continue</span></span>
- <span data-ttu-id="ccc26-132">Över</span><span class="sxs-lookup"><span data-stu-id="ccc26-132">Ignore</span></span>
- <span data-ttu-id="ccc26-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="ccc26-133">Inquire</span></span>
- <span data-ttu-id="ccc26-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ccc26-134">SilentlyContinue</span></span>
- <span data-ttu-id="ccc26-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="ccc26-135">Stop</span></span>
- <span data-ttu-id="ccc26-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ccc26-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ccc26-137">-InformationVariable</span></span>
<span data-ttu-id="ccc26-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ccc26-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ccc26-139">-ODataQuery</span></span>
<span data-ttu-id="ccc26-140">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="ccc26-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ccc26-141">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="ccc26-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ccc26-142">-För</span><span class="sxs-lookup"><span data-stu-id="ccc26-142">-Pre</span></span>
<span data-ttu-id="ccc26-143">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ccc26-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ccc26-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="ccc26-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="ccc26-145">Anger ett delvis namn på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ccc26-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="ccc26-146">Denna cmdlet matchar resurs grupper vars värde är en under sträng.</span><span class="sxs-lookup"><span data-stu-id="ccc26-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="ccc26-147">Cmdleten söker efter resurser i resurs grupperna.</span><span class="sxs-lookup"><span data-stu-id="ccc26-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="ccc26-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="ccc26-149">Resurs grupps namnet för en fullständig matchning.</span><span class="sxs-lookup"><span data-stu-id="ccc26-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="ccc26-150">-ResourceNameContains</span></span>
<span data-ttu-id="ccc26-151">Anger ett delvis namn på en resurs.</span><span class="sxs-lookup"><span data-stu-id="ccc26-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="ccc26-152">Cmdleten söker efter resurser som innehåller detta värde som en under sträng.</span><span class="sxs-lookup"><span data-stu-id="ccc26-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="ccc26-153">-ResourceNameEquals</span></span>
<span data-ttu-id="ccc26-154">Resurs namnet för en fullständig matchning.</span><span class="sxs-lookup"><span data-stu-id="ccc26-154">The resource name for a full match.</span></span> <span data-ttu-id="ccc26-155">till exempel: om ditt resurs namn är testResource kan du ange testResource.</span><span class="sxs-lookup"><span data-stu-id="ccc26-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ccc26-156">-ResourceType</span></span>
<span data-ttu-id="ccc26-157">Anger typen för en resurs.</span><span class="sxs-lookup"><span data-stu-id="ccc26-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="ccc26-158">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="ccc26-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="ccc26-159">Denna cmdlet söker efter resurser av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="ccc26-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-160">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ccc26-160">-Tag</span></span>
<span data-ttu-id="ccc26-161">Tag-filtret för OData-frågan.</span><span class="sxs-lookup"><span data-stu-id="ccc26-161">The tag filter for the OData query.</span></span> <span data-ttu-id="ccc26-162">Det förväntade formatet är @ {tagName = $null} eller @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="ccc26-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="ccc26-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="ccc26-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ccc26-165">-TenantLevel</span></span>
<span data-ttu-id="ccc26-166">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="ccc26-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-167">-Överst</span><span class="sxs-lookup"><span data-stu-id="ccc26-167">-Top</span></span>
<span data-ttu-id="ccc26-168">Anger antalet resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="ccc26-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc26-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc26-169">CommonParameters</span></span>
<span data-ttu-id="ccc26-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc26-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc26-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc26-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc26-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccc26-172">INPUTS</span></span>

### <span data-ttu-id="ccc26-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="ccc26-173">None</span></span>
<span data-ttu-id="ccc26-174">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ccc26-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccc26-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccc26-175">OUTPUTS</span></span>

### <span data-ttu-id="ccc26-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ccc26-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ccc26-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccc26-177">NOTES</span></span>

## <span data-ttu-id="ccc26-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccc26-178">RELATED LINKS</span></span>

[<span data-ttu-id="ccc26-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ccc26-180">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ccc26-181">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ccc26-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ccc26-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ccc26-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
