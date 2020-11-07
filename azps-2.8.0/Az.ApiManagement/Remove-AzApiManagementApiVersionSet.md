---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 03092cf9577bb7b8a35fd0ef69f5d3c94e9c92de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745725"
---
# <span data-ttu-id="087ef-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="087ef-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="087ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="087ef-102">SYNOPSIS</span></span>
<span data-ttu-id="087ef-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="087ef-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="087ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="087ef-104">SYNTAX</span></span>

### <span data-ttu-id="087ef-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="087ef-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="087ef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="087ef-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="087ef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="087ef-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="087ef-108">DESCRIPTION</span></span>

<span data-ttu-id="087ef-109">Cmdleten **Remove-AzAzureRmApiManagementApiVersionSet** tar bort en befintlig API-version.</span><span class="sxs-lookup"><span data-stu-id="087ef-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="087ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="087ef-110">EXAMPLES</span></span>

### <span data-ttu-id="087ef-111">Exempel 1: ta bort en API-version</span><span class="sxs-lookup"><span data-stu-id="087ef-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="087ef-112">Det här kommandot tar bort API-versionen med angiven ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="087ef-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="087ef-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="087ef-113">PARAMETERS</span></span>

### <span data-ttu-id="087ef-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="087ef-114">-ApiVersionSetId</span></span>
<span data-ttu-id="087ef-115">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="087ef-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="087ef-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="087ef-116">This parameter is required.</span></span>

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

### <span data-ttu-id="087ef-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="087ef-117">-Context</span></span>
<span data-ttu-id="087ef-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="087ef-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="087ef-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="087ef-119">This parameter is required.</span></span>

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

### <span data-ttu-id="087ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087ef-120">-DefaultProfile</span></span>
<span data-ttu-id="087ef-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="087ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="087ef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="087ef-122">-InputObject</span></span>
<span data-ttu-id="087ef-123">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="087ef-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="087ef-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="087ef-124">This parameter is required.</span></span>

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

### <span data-ttu-id="087ef-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="087ef-125">-PassThru</span></span>
<span data-ttu-id="087ef-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="087ef-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="087ef-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="087ef-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="087ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="087ef-128">-ResourceId</span></span>
<span data-ttu-id="087ef-129">ResourceId för ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="087ef-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="087ef-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="087ef-130">This parameter is required.</span></span>

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

### <span data-ttu-id="087ef-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="087ef-131">-Confirm</span></span>
<span data-ttu-id="087ef-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="087ef-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="087ef-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087ef-133">-WhatIf</span></span>
<span data-ttu-id="087ef-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="087ef-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="087ef-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="087ef-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="087ef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087ef-136">CommonParameters</span></span>
<span data-ttu-id="087ef-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087ef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087ef-138">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="087ef-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087ef-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="087ef-139">INPUTS</span></span>

### <span data-ttu-id="087ef-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="087ef-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="087ef-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="087ef-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="087ef-142">System. String</span><span class="sxs-lookup"><span data-stu-id="087ef-142">System.String</span></span>

## <span data-ttu-id="087ef-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="087ef-143">OUTPUTS</span></span>

### <span data-ttu-id="087ef-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="087ef-144">System.Boolean</span></span>

## <span data-ttu-id="087ef-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="087ef-145">NOTES</span></span>

## <span data-ttu-id="087ef-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="087ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="087ef-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="087ef-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="087ef-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="087ef-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="087ef-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="087ef-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)