---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576425"
---
# <span data-ttu-id="26151-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="26151-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26151-102">SYNOPSIS</span></span>
<span data-ttu-id="26151-103">Hämtar resurser.</span><span class="sxs-lookup"><span data-stu-id="26151-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26151-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26151-104">SYNTAX</span></span>

### <span data-ttu-id="26151-105">GetAllResources (standard)</span><span class="sxs-lookup"><span data-stu-id="26151-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26151-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="26151-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="26151-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="26151-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26151-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="26151-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="26151-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26151-112">GetResourceCollection</span><span class="sxs-lookup"><span data-stu-id="26151-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26151-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26151-113">DESCRIPTION</span></span>
<span data-ttu-id="26151-114">Cmdleten **Get-AzureRmResource** får Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="26151-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="26151-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26151-115">EXAMPLES</span></span>

### <span data-ttu-id="26151-116">Exempel 1: få alla resurser av en viss typ</span><span class="sxs-lookup"><span data-stu-id="26151-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="26151-117">Det här kommandot får en resurs av typen Microsoft. Web/Sites under ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="26151-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="26151-118">Exempel 2: Hämta en resurs med namn</span><span class="sxs-lookup"><span data-stu-id="26151-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="26151-119">Med det här kommandot får du resursen namnet ContosoWebsite under ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="26151-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="26151-120">Exempel 3: Visa alla status för lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="26151-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="26151-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26151-121">PARAMETERS</span></span>

### <span data-ttu-id="26151-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26151-122">-ApiVersion</span></span>
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

### <span data-ttu-id="26151-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26151-123">-DefaultProfile</span></span>
<span data-ttu-id="26151-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26151-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26151-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="26151-125">-ExpandProperties</span></span>
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

### <span data-ttu-id="26151-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="26151-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="26151-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="26151-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26151-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="26151-129">-ODataQuery</span></span>
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

### <span data-ttu-id="26151-130">-För</span><span class="sxs-lookup"><span data-stu-id="26151-130">-Pre</span></span>
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

### <span data-ttu-id="26151-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26151-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26151-132">-ResourceId</span></span>
<span data-ttu-id="26151-133">Anger fullständigt resurs-ID, inklusive prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="26151-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="26151-134">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="26151-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="26151-135">Denna cmdlet tar resursen med detta ID.</span><span class="sxs-lookup"><span data-stu-id="26151-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="26151-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="26151-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26151-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="26151-138">-TenantLevel</span></span>
<span data-ttu-id="26151-139">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="26151-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26151-140">-Överst</span><span class="sxs-lookup"><span data-stu-id="26151-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26151-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26151-141">CommonParameters</span></span>
<span data-ttu-id="26151-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26151-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26151-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26151-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26151-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26151-144">INPUTS</span></span>

### <span data-ttu-id="26151-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="26151-145">None</span></span>
<span data-ttu-id="26151-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="26151-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26151-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26151-147">OUTPUTS</span></span>

### <span data-ttu-id="26151-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="26151-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="26151-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26151-149">NOTES</span></span>

## <span data-ttu-id="26151-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26151-150">RELATED LINKS</span></span>

[<span data-ttu-id="26151-151">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="26151-152">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="26151-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="26151-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="26151-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="26151-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


