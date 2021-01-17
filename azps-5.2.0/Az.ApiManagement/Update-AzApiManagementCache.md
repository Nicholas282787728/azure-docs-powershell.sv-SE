---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388068"
---
# <span data-ttu-id="81f1f-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="81f1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="81f1f-103">uppdaterar ett cacheminne i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="81f1f-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="81f1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81f1f-104">SYNTAX</span></span>

### <span data-ttu-id="81f1f-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="81f1f-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f1f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81f1f-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81f1f-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81f1f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81f1f-108">DESCRIPTION</span></span>
<span data-ttu-id="81f1f-109">Cmdlet **Update-AzApiManagementCache** uppdaterar en cache i ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="81f1f-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="81f1f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81f1f-110">EXAMPLES</span></span>

### <span data-ttu-id="81f1f-111">Exempel 1: uppdaterar beskrivningen av cachen i Central</span><span class="sxs-lookup"><span data-stu-id="81f1f-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="81f1f-112">Uppdaterar beskrivningen av cachen i Central USA.</span><span class="sxs-lookup"><span data-stu-id="81f1f-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="81f1f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81f1f-113">PARAMETERS</span></span>

### <span data-ttu-id="81f1f-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="81f1f-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="81f1f-115">Arm-ResourceId för Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="81f1f-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="81f1f-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="81f1f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="81f1f-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="81f1f-117">-CacheId</span></span>
<span data-ttu-id="81f1f-118">ID för ny cache.</span><span class="sxs-lookup"><span data-stu-id="81f1f-118">Identifier of new cache.</span></span>
<span data-ttu-id="81f1f-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="81f1f-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="81f1f-120">-ConnectionString</span></span>
<span data-ttu-id="81f1f-121">Redis anslutnings sträng.</span><span class="sxs-lookup"><span data-stu-id="81f1f-121">Redis Connection String.</span></span>
<span data-ttu-id="81f1f-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="81f1f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="81f1f-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="81f1f-123">-Context</span></span>
<span data-ttu-id="81f1f-124">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="81f1f-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="81f1f-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="81f1f-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f1f-126">-DefaultProfile</span></span>
<span data-ttu-id="81f1f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81f1f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f1f-128">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="81f1f-128">-Description</span></span>
<span data-ttu-id="81f1f-129">Cachestorlek.</span><span class="sxs-lookup"><span data-stu-id="81f1f-129">Cache Description.</span></span>
<span data-ttu-id="81f1f-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="81f1f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="81f1f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81f1f-131">-InputObject</span></span>
<span data-ttu-id="81f1f-132">Instans av PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="81f1f-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="81f1f-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="81f1f-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81f1f-134">-PassThru</span></span>
<span data-ttu-id="81f1f-135">Om det här anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache typ som representerar den ändrade cachen att skrivas till output.</span><span class="sxs-lookup"><span data-stu-id="81f1f-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81f1f-136">-ResourceId</span></span>
<span data-ttu-id="81f1f-137">Arm ResourceId för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="81f1f-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="81f1f-138">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="81f1f-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81f1f-139">-Confirm</span></span>
<span data-ttu-id="81f1f-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81f1f-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f1f-141">-WhatIf</span></span>
<span data-ttu-id="81f1f-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81f1f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81f1f-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81f1f-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f1f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f1f-144">CommonParameters</span></span>
<span data-ttu-id="81f1f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f1f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f1f-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81f1f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f1f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81f1f-147">INPUTS</span></span>

### <span data-ttu-id="81f1f-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81f1f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81f1f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="81f1f-149">System.String</span></span>

### <span data-ttu-id="81f1f-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="81f1f-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81f1f-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81f1f-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81f1f-152">OUTPUTS</span></span>

### <span data-ttu-id="81f1f-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="81f1f-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81f1f-154">NOTES</span></span>

## <span data-ttu-id="81f1f-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81f1f-155">RELATED LINKS</span></span>

[<span data-ttu-id="81f1f-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="81f1f-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="81f1f-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="81f1f-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
