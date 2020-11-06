---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581296"
---
# <span data-ttu-id="1d356-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="1d356-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d356-102">SYNOPSIS</span></span>
<span data-ttu-id="1d356-103">Tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="1d356-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d356-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d356-104">SYNTAX</span></span>

### <span data-ttu-id="1d356-105">Resurs-ID. (standard)</span><span class="sxs-lookup"><span data-stu-id="1d356-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d356-106">Resurs som finns på abonnemangs nivån.</span><span class="sxs-lookup"><span data-stu-id="1d356-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d356-107">Resurs som finns på klient nivå.</span><span class="sxs-lookup"><span data-stu-id="1d356-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d356-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d356-108">DESCRIPTION</span></span>
<span data-ttu-id="1d356-109">Cmdleten **Remove-AzureRmResource** tar bort en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="1d356-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="1d356-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d356-110">EXAMPLES</span></span>

### <span data-ttu-id="1d356-111">Exempel 1: ta bort en webbplats resurs</span><span class="sxs-lookup"><span data-stu-id="1d356-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="1d356-112">Det här kommandot tar bort webbplats resursen som heter ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="1d356-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="1d356-113">I exemplet används ett platshållarfält för prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="1d356-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="1d356-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="1d356-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1d356-115">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1d356-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1d356-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d356-116">PARAMETERS</span></span>

### <span data-ttu-id="1d356-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d356-117">-ApiVersion</span></span>
<span data-ttu-id="1d356-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1d356-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1d356-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="1d356-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1d356-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="1d356-120">-ExtensionResourceName</span></span>
<span data-ttu-id="1d356-121">Anger namnet på en tilläggs resurs för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1d356-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="1d356-122">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="1d356-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="1d356-123">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="1d356-123">server name`/`database name</span></span>

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

### <span data-ttu-id="1d356-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="1d356-124">-ExtensionResourceType</span></span>
<span data-ttu-id="1d356-125">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="1d356-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="1d356-126">Anger resurs typen för tilläggs resursen för resursen.</span><span class="sxs-lookup"><span data-stu-id="1d356-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="1d356-127">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1d356-127">For instance:</span></span> 

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

### <span data-ttu-id="1d356-128">-Force</span><span class="sxs-lookup"><span data-stu-id="1d356-128">-Force</span></span>
<span data-ttu-id="1d356-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1d356-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d356-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1d356-130">-ODataQuery</span></span>
<span data-ttu-id="1d356-131">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="1d356-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="1d356-132">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="1d356-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="1d356-133">-För</span><span class="sxs-lookup"><span data-stu-id="1d356-133">-Pre</span></span>
<span data-ttu-id="1d356-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1d356-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1d356-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d356-135">-ResourceGroupName</span></span>
<span data-ttu-id="1d356-136">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="1d356-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="1d356-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d356-137">-ResourceId</span></span>
<span data-ttu-id="1d356-138">Anger det fullständigt kvalificerade resurs-ID: t för resursen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1d356-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="1d356-139">Detta ID inkluderar prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="1d356-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="1d356-140">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1d356-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="1d356-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1d356-141">-ResourceName</span></span>
<span data-ttu-id="1d356-142">Anger namnet på den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1d356-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="1d356-143">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="1d356-143">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="1d356-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1d356-144">-ResourceType</span></span>
<span data-ttu-id="1d356-145">Anger typen för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1d356-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="1d356-146">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="1d356-146">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="1d356-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1d356-147">-TenantLevel</span></span>
<span data-ttu-id="1d356-148">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="1d356-148">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="1d356-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d356-149">-Confirm</span></span>
<span data-ttu-id="1d356-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d356-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d356-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d356-151">-WhatIf</span></span>
<span data-ttu-id="1d356-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d356-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d356-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d356-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d356-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d356-154">-DefaultProfile</span></span>
<span data-ttu-id="1d356-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d356-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d356-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d356-156">CommonParameters</span></span>
<span data-ttu-id="1d356-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d356-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d356-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d356-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d356-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d356-159">INPUTS</span></span>

## <span data-ttu-id="1d356-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d356-160">OUTPUTS</span></span>

### <span data-ttu-id="1d356-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d356-161">System.Boolean</span></span>

## <span data-ttu-id="1d356-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d356-162">NOTES</span></span>

## <span data-ttu-id="1d356-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d356-163">RELATED LINKS</span></span>

[<span data-ttu-id="1d356-164">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="1d356-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="1d356-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="1d356-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="1d356-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1d356-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


