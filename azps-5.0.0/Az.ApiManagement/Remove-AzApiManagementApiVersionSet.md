---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271097"
---
# <span data-ttu-id="af596-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="af596-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="af596-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af596-102">SYNOPSIS</span></span>
<span data-ttu-id="af596-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="af596-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="af596-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af596-104">SYNTAX</span></span>

### <span data-ttu-id="af596-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="af596-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af596-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af596-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af596-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af596-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af596-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af596-108">DESCRIPTION</span></span>

<span data-ttu-id="af596-109">Cmdleten **Remove-AzAzureRmApiManagementApiVersionSet** tar bort en befintlig API-version.</span><span class="sxs-lookup"><span data-stu-id="af596-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="af596-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af596-110">EXAMPLES</span></span>

### <span data-ttu-id="af596-111">Exempel 1: ta bort en API-version</span><span class="sxs-lookup"><span data-stu-id="af596-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="af596-112">Det här kommandot tar bort API-versionen med angiven ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="af596-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="af596-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af596-113">PARAMETERS</span></span>

### <span data-ttu-id="af596-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="af596-114">-ApiVersionSetId</span></span>
<span data-ttu-id="af596-115">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="af596-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="af596-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="af596-116">This parameter is required.</span></span>

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

### <span data-ttu-id="af596-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="af596-117">-Context</span></span>
<span data-ttu-id="af596-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="af596-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="af596-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="af596-119">This parameter is required.</span></span>

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

### <span data-ttu-id="af596-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af596-120">-DefaultProfile</span></span>
<span data-ttu-id="af596-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af596-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af596-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af596-122">-InputObject</span></span>
<span data-ttu-id="af596-123">Instans av PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="af596-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="af596-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="af596-124">This parameter is required.</span></span>

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

### <span data-ttu-id="af596-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af596-125">-PassThru</span></span>
<span data-ttu-id="af596-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="af596-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="af596-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="af596-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="af596-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af596-128">-ResourceId</span></span>
<span data-ttu-id="af596-129">ResourceId för ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="af596-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="af596-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="af596-130">This parameter is required.</span></span>

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

### <span data-ttu-id="af596-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af596-131">-Confirm</span></span>
<span data-ttu-id="af596-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af596-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af596-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af596-133">-WhatIf</span></span>
<span data-ttu-id="af596-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af596-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af596-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af596-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af596-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af596-136">CommonParameters</span></span>
<span data-ttu-id="af596-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af596-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af596-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af596-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af596-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af596-139">INPUTS</span></span>

### <span data-ttu-id="af596-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="af596-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af596-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="af596-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="af596-142">System. String</span><span class="sxs-lookup"><span data-stu-id="af596-142">System.String</span></span>

## <span data-ttu-id="af596-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af596-143">OUTPUTS</span></span>

### <span data-ttu-id="af596-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af596-144">System.Boolean</span></span>

## <span data-ttu-id="af596-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af596-145">NOTES</span></span>

## <span data-ttu-id="af596-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af596-146">RELATED LINKS</span></span>

[<span data-ttu-id="af596-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="af596-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="af596-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="af596-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="af596-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="af596-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)