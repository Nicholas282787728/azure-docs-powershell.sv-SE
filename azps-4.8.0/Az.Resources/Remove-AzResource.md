---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ecd70916f1ddb6e365fb9f880db9974f6c9ae771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258672"
---
# <span data-ttu-id="6649a-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-101">Remove-AzResource</span></span>

## <span data-ttu-id="6649a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6649a-102">SYNOPSIS</span></span>
<span data-ttu-id="6649a-103">Tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="6649a-103">Removes a resource.</span></span>

## <span data-ttu-id="6649a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6649a-104">SYNTAX</span></span>

### <span data-ttu-id="6649a-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="6649a-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6649a-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6649a-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6649a-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6649a-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6649a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6649a-108">DESCRIPTION</span></span>
<span data-ttu-id="6649a-109">Cmdleten **Remove-AzResource** tar bort en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="6649a-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="6649a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6649a-110">EXAMPLES</span></span>

### <span data-ttu-id="6649a-111">Exempel 1: ta bort en webbplats resurs</span><span class="sxs-lookup"><span data-stu-id="6649a-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="6649a-112">Det här kommandot tar bort webbplats resursen som heter ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="6649a-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="6649a-113">I exemplet används ett platshållarfält för prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="6649a-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="6649a-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="6649a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6649a-115">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6649a-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6649a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6649a-116">PARAMETERS</span></span>

### <span data-ttu-id="6649a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6649a-117">-ApiVersion</span></span>
<span data-ttu-id="6649a-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6649a-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6649a-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="6649a-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6649a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6649a-120">-AsJob</span></span>
<span data-ttu-id="6649a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6649a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6649a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6649a-122">-DefaultProfile</span></span>
<span data-ttu-id="6649a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6649a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6649a-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6649a-124">-ExtensionResourceName</span></span>
<span data-ttu-id="6649a-125">Anger namnet på en tilläggs resurs för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6649a-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6649a-126">Om du till exempel vill ange en databas använder du följande format: Server namn `/` databas namn</span><span class="sxs-lookup"><span data-stu-id="6649a-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="6649a-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6649a-127">-ExtensionResourceType</span></span>
<span data-ttu-id="6649a-128">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="6649a-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6649a-129">Anger resurs typen för tilläggs resursen för resursen.</span><span class="sxs-lookup"><span data-stu-id="6649a-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="6649a-130">Till exempel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6649a-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6649a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="6649a-131">-Force</span></span>
<span data-ttu-id="6649a-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6649a-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6649a-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6649a-133">-ODataQuery</span></span>
<span data-ttu-id="6649a-134">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="6649a-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6649a-135">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="6649a-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6649a-136">-För</span><span class="sxs-lookup"><span data-stu-id="6649a-136">-Pre</span></span>
<span data-ttu-id="6649a-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6649a-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6649a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6649a-138">-ResourceGroupName</span></span>
<span data-ttu-id="6649a-139">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="6649a-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="6649a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6649a-140">-ResourceId</span></span>
<span data-ttu-id="6649a-141">Anger det fullständigt kvalificerade resurs-ID: t för resursen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6649a-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6649a-142">Detta ID inkluderar abonnemanget, som i följande exempel: `/subscriptions/` prenumerations-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6649a-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6649a-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6649a-143">-ResourceName</span></span>
<span data-ttu-id="6649a-144">Anger namnet på den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6649a-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6649a-145">Om du till exempel vill ange en databas använder du följande format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6649a-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6649a-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6649a-146">-ResourceType</span></span>
<span data-ttu-id="6649a-147">Anger typen för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6649a-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="6649a-148">För en databas är exempelvis resurs typen följande: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6649a-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6649a-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6649a-149">-TenantLevel</span></span>
<span data-ttu-id="6649a-150">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="6649a-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6649a-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6649a-151">-Confirm</span></span>
<span data-ttu-id="6649a-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6649a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6649a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6649a-153">-WhatIf</span></span>
<span data-ttu-id="6649a-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6649a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6649a-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6649a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6649a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6649a-156">CommonParameters</span></span>
<span data-ttu-id="6649a-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6649a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6649a-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6649a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6649a-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6649a-159">INPUTS</span></span>

### <span data-ttu-id="6649a-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6649a-160">System.String</span></span>

## <span data-ttu-id="6649a-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6649a-161">OUTPUTS</span></span>

### <span data-ttu-id="6649a-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6649a-162">System.Boolean</span></span>

## <span data-ttu-id="6649a-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6649a-163">NOTES</span></span>

## <span data-ttu-id="6649a-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6649a-164">RELATED LINKS</span></span>

[<span data-ttu-id="6649a-165">Sök-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-165">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="6649a-166">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-166">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="6649a-167">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-167">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="6649a-168">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-168">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="6649a-169">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="6649a-169">Set-AzResource</span></span>](./Set-AzResource.md)


