---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579427"
---
# <span data-ttu-id="5ae0b-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="5ae0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ae0b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae0b-103">Tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ae0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ae0b-104">SYNTAX</span></span>

### <span data-ttu-id="5ae0b-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="5ae0b-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ae0b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5ae0b-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ae0b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5ae0b-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ae0b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ae0b-108">DESCRIPTION</span></span>
<span data-ttu-id="5ae0b-109">Cmdleten **Remove-AzureRmResource** tar bort en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="5ae0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ae0b-110">EXAMPLES</span></span>

### <span data-ttu-id="5ae0b-111">Exempel 1: ta bort en webbplats resurs</span><span class="sxs-lookup"><span data-stu-id="5ae0b-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="5ae0b-112">Det här kommandot tar bort webbplats resursen som heter ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="5ae0b-113">I exemplet används ett platshållarfält för prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="5ae0b-114">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="5ae0b-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5ae0b-115">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5ae0b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ae0b-116">PARAMETERS</span></span>

### <span data-ttu-id="5ae0b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ae0b-117">-ApiVersion</span></span>
<span data-ttu-id="5ae0b-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5ae0b-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5ae0b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ae0b-120">-AsJob</span></span>
<span data-ttu-id="5ae0b-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5ae0b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ae0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae0b-122">-DefaultProfile</span></span>
<span data-ttu-id="5ae0b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5ae0b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ae0b-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5ae0b-124">-ExtensionResourceName</span></span>
<span data-ttu-id="5ae0b-125">Anger namnet på en tilläggs resurs för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5ae0b-126">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="5ae0b-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="5ae0b-127">`/`namn på Server namn</span><span class="sxs-lookup"><span data-stu-id="5ae0b-127">server name`/`database name</span></span>

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

### <span data-ttu-id="5ae0b-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5ae0b-128">-ExtensionResourceType</span></span>
<span data-ttu-id="5ae0b-129">Anger resurs typen för en tilläggs resurs.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5ae0b-130">Anger resurs typen för tilläggs resursen för resursen.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="5ae0b-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="5ae0b-131">For instance:</span></span> 

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

### <span data-ttu-id="5ae0b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5ae0b-132">-Force</span></span>
<span data-ttu-id="5ae0b-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ae0b-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5ae0b-134">-ODataQuery</span></span>
<span data-ttu-id="5ae0b-135">Anger ett filter för Open data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="5ae0b-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="5ae0b-136">Denna cmdlet lägger till det här värdet till begäran utöver eventuella andra filter.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5ae0b-137">-För</span><span class="sxs-lookup"><span data-stu-id="5ae0b-137">-Pre</span></span>
<span data-ttu-id="5ae0b-138">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5ae0b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae0b-139">-ResourceGroupName</span></span>
<span data-ttu-id="5ae0b-140">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en resurs.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="5ae0b-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ae0b-141">-ResourceId</span></span>
<span data-ttu-id="5ae0b-142">Anger det fullständigt kvalificerade resurs-ID: t för resursen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5ae0b-143">Detta ID inkluderar prenumerationen, som i följande exempel:</span><span class="sxs-lookup"><span data-stu-id="5ae0b-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="5ae0b-144">`/subscriptions/`abonnemangs-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5ae0b-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5ae0b-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5ae0b-145">-ResourceName</span></span>
<span data-ttu-id="5ae0b-146">Anger namnet på den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5ae0b-147">Om du till exempel vill ange en databas använder du följande format:</span><span class="sxs-lookup"><span data-stu-id="5ae0b-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="5ae0b-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5ae0b-148">-ResourceType</span></span>
<span data-ttu-id="5ae0b-149">Anger typen för den resurs som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="5ae0b-150">För en databas är exempelvis resurs typen följande:</span><span class="sxs-lookup"><span data-stu-id="5ae0b-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="5ae0b-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5ae0b-151">-TenantLevel</span></span>
<span data-ttu-id="5ae0b-152">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="5ae0b-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ae0b-153">-Confirm</span></span>
<span data-ttu-id="5ae0b-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ae0b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ae0b-155">-WhatIf</span></span>
<span data-ttu-id="5ae0b-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ae0b-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ae0b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae0b-158">CommonParameters</span></span>
<span data-ttu-id="5ae0b-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae0b-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae0b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae0b-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ae0b-161">INPUTS</span></span>

### <span data-ttu-id="5ae0b-162">Ingen</span><span class="sxs-lookup"><span data-stu-id="5ae0b-162">None</span></span>
<span data-ttu-id="5ae0b-163">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5ae0b-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ae0b-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ae0b-164">OUTPUTS</span></span>

### <span data-ttu-id="5ae0b-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ae0b-165">System.Boolean</span></span>

## <span data-ttu-id="5ae0b-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ae0b-166">NOTES</span></span>

## <span data-ttu-id="5ae0b-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ae0b-167">RELATED LINKS</span></span>

[<span data-ttu-id="5ae0b-168">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="5ae0b-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="5ae0b-170">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="5ae0b-171">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="5ae0b-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5ae0b-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)

