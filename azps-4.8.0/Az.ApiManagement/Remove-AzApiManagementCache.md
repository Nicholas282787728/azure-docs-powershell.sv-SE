---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103100"
---
# <span data-ttu-id="494d9-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="494d9-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="494d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="494d9-102">SYNOPSIS</span></span>
<span data-ttu-id="494d9-103">Tar bort cacheobjektet.</span><span class="sxs-lookup"><span data-stu-id="494d9-103">Removes the cache entity.</span></span>

## <span data-ttu-id="494d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="494d9-104">SYNTAX</span></span>

### <span data-ttu-id="494d9-105">ContextParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="494d9-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="494d9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="494d9-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="494d9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="494d9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="494d9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="494d9-108">DESCRIPTION</span></span>
<span data-ttu-id="494d9-109">Cmdlet **Remove-AzApiManagementCache** tar bort cacheobjektet.</span><span class="sxs-lookup"><span data-stu-id="494d9-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="494d9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="494d9-110">EXAMPLES</span></span>

### <span data-ttu-id="494d9-111">Exempel 1: ta bort cacheobjektet</span><span class="sxs-lookup"><span data-stu-id="494d9-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="494d9-112">Denna cmdlet tar bort cacheminnet `centralus` från API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="494d9-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="494d9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="494d9-113">PARAMETERS</span></span>

### <span data-ttu-id="494d9-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="494d9-114">-CacheId</span></span>
<span data-ttu-id="494d9-115">Identifierare för befintliga cacheId.</span><span class="sxs-lookup"><span data-stu-id="494d9-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="494d9-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="494d9-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494d9-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="494d9-117">-Context</span></span>
<span data-ttu-id="494d9-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="494d9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="494d9-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="494d9-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="494d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="494d9-120">-DefaultProfile</span></span>
<span data-ttu-id="494d9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="494d9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="494d9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="494d9-122">-InputObject</span></span>
<span data-ttu-id="494d9-123">Instans av PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="494d9-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="494d9-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="494d9-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="494d9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="494d9-125">-PassThru</span></span>
<span data-ttu-id="494d9-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="494d9-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="494d9-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="494d9-127">This parameter is optional.</span></span>
<span data-ttu-id="494d9-128">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="494d9-128">Default value is false.</span></span>

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

### <span data-ttu-id="494d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="494d9-129">-ResourceId</span></span>
<span data-ttu-id="494d9-130">Arm ResourceId för cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="494d9-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="494d9-131">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="494d9-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494d9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="494d9-132">-Confirm</span></span>
<span data-ttu-id="494d9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="494d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="494d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="494d9-134">-WhatIf</span></span>
<span data-ttu-id="494d9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="494d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="494d9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="494d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="494d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="494d9-137">CommonParameters</span></span>
<span data-ttu-id="494d9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="494d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="494d9-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="494d9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="494d9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="494d9-140">INPUTS</span></span>

### <span data-ttu-id="494d9-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="494d9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="494d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="494d9-142">System.String</span></span>

### <span data-ttu-id="494d9-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="494d9-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="494d9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="494d9-144">OUTPUTS</span></span>

### <span data-ttu-id="494d9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="494d9-145">System.Boolean</span></span>

## <span data-ttu-id="494d9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="494d9-146">NOTES</span></span>

## <span data-ttu-id="494d9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="494d9-147">RELATED LINKS</span></span>

[<span data-ttu-id="494d9-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="494d9-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="494d9-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="494d9-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="494d9-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="494d9-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
