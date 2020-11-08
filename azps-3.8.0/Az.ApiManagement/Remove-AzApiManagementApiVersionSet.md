---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089887"
---
# <span data-ttu-id="7d74f-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d74f-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7d74f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d74f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d74f-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="7d74f-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="7d74f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d74f-104">SYNTAX</span></span>

### <span data-ttu-id="7d74f-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="7d74f-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7d74f-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d74f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d74f-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d74f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d74f-108">DESCRIPTION</span></span>

<span data-ttu-id="7d74f-109">Cmdleten **Remove-AzAzureRmApiManagementApiVersionSet** tar bort en befintlig API-version.</span><span class="sxs-lookup"><span data-stu-id="7d74f-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="7d74f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d74f-110">EXAMPLES</span></span>

### <span data-ttu-id="7d74f-111">Exempel 1: ta bort en API-version</span><span class="sxs-lookup"><span data-stu-id="7d74f-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="7d74f-112">Det här kommandot tar bort API-versionen med angiven ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="7d74f-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="7d74f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d74f-113">PARAMETERS</span></span>

### <span data-ttu-id="7d74f-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="7d74f-114">-ApiVersionSetId</span></span>
<span data-ttu-id="7d74f-115">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="7d74f-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="7d74f-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7d74f-116">This parameter is required.</span></span>

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

### <span data-ttu-id="7d74f-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7d74f-117">-Context</span></span>
<span data-ttu-id="7d74f-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7d74f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7d74f-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7d74f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="7d74f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d74f-120">-DefaultProfile</span></span>
<span data-ttu-id="7d74f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d74f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d74f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d74f-122">-InputObject</span></span>
<span data-ttu-id="7d74f-123">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7d74f-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="7d74f-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7d74f-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d74f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d74f-125">-PassThru</span></span>
<span data-ttu-id="7d74f-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="7d74f-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="7d74f-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7d74f-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d74f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d74f-128">-ResourceId</span></span>
<span data-ttu-id="7d74f-129">ResourceId för ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7d74f-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="7d74f-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7d74f-130">This parameter is required.</span></span>

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

### <span data-ttu-id="7d74f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d74f-131">-Confirm</span></span>
<span data-ttu-id="7d74f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d74f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d74f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d74f-133">-WhatIf</span></span>
<span data-ttu-id="7d74f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d74f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d74f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d74f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d74f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d74f-136">CommonParameters</span></span>
<span data-ttu-id="7d74f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d74f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d74f-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d74f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d74f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d74f-139">INPUTS</span></span>

### <span data-ttu-id="7d74f-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7d74f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7d74f-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d74f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="7d74f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7d74f-142">System.String</span></span>

## <span data-ttu-id="7d74f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d74f-143">OUTPUTS</span></span>

### <span data-ttu-id="7d74f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d74f-144">System.Boolean</span></span>

## <span data-ttu-id="7d74f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d74f-145">NOTES</span></span>

## <span data-ttu-id="7d74f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d74f-146">RELATED LINKS</span></span>

[<span data-ttu-id="7d74f-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d74f-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="7d74f-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d74f-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="7d74f-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d74f-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)