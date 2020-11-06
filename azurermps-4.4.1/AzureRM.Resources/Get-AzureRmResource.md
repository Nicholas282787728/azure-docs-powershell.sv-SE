---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581351"
---
# <span data-ttu-id="75245-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="75245-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75245-102">SYNOPSIS</span></span>
<span data-ttu-id="75245-103">Hämtar resurser.</span><span class="sxs-lookup"><span data-stu-id="75245-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75245-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75245-104">SYNTAX</span></span>

### <span data-ttu-id="75245-105">Parametern lista alla resurser.</span><span class="sxs-lookup"><span data-stu-id="75245-105">The list all resources parameter set.</span></span> <span data-ttu-id="75245-106">Vis</span><span class="sxs-lookup"><span data-stu-id="75245-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-107">Skaffa en enda resurs utifrån dess ID.</span><span class="sxs-lookup"><span data-stu-id="75245-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-108">Skaffa en enda resurs på klient organisations nivå.</span><span class="sxs-lookup"><span data-stu-id="75245-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-109">Visar de resurser som baseras på den angivna omfattningen på klient organisations nivå.</span><span class="sxs-lookup"><span data-stu-id="75245-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-110">Hämta resurs utifrån namn och grupp</span><span class="sxs-lookup"><span data-stu-id="75245-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75245-111">Skaffa en resurs via namn och typ.</span><span class="sxs-lookup"><span data-stu-id="75245-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-112">Hämta resurs efter namn, grupp och typ</span><span class="sxs-lookup"><span data-stu-id="75245-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75245-113">Skaffa resurs samling</span><span class="sxs-lookup"><span data-stu-id="75245-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75245-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75245-114">DESCRIPTION</span></span>
<span data-ttu-id="75245-115">Cmdleten **Get-AzureRmResource** får Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="75245-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="75245-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75245-116">EXAMPLES</span></span>

### <span data-ttu-id="75245-117">Exempel 1: skaffa en resurs</span><span class="sxs-lookup"><span data-stu-id="75245-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="75245-118">Det här kommandot får en resurs av typen Microsoft. Web/Sites, med namnet ContosoWebsite under ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="75245-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="75245-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75245-119">PARAMETERS</span></span>

### <span data-ttu-id="75245-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75245-120">-ApiVersion</span></span>
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

### <span data-ttu-id="75245-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="75245-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="75245-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="75245-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="75245-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="75245-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75245-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="75245-125">-ODataQuery</span></span>
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

### <span data-ttu-id="75245-126">-För</span><span class="sxs-lookup"><span data-stu-id="75245-126">-Pre</span></span>
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

### <span data-ttu-id="75245-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75245-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75245-128">-ResourceId</span></span>
<span data-ttu-id="75245-129">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="75245-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="75245-130">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="75245-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="75245-131">Denna cmdlet tar resursen med detta ID.</span><span class="sxs-lookup"><span data-stu-id="75245-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="75245-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="75245-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75245-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="75245-134">-TenantLevel</span></span>
<span data-ttu-id="75245-135">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="75245-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75245-136">-Överst</span><span class="sxs-lookup"><span data-stu-id="75245-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75245-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75245-137">-DefaultProfile</span></span>
<span data-ttu-id="75245-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75245-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75245-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75245-139">CommonParameters</span></span>
<span data-ttu-id="75245-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75245-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75245-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75245-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75245-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75245-142">INPUTS</span></span>

## <span data-ttu-id="75245-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75245-143">OUTPUTS</span></span>

### <span data-ttu-id="75245-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="75245-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="75245-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75245-145">NOTES</span></span>

## <span data-ttu-id="75245-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75245-146">RELATED LINKS</span></span>

[<span data-ttu-id="75245-147">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="75245-148">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="75245-149">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="75245-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="75245-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="75245-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


