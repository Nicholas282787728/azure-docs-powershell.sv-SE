---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271386"
---
# <span data-ttu-id="8b89f-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b89f-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8b89f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b89f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b89f-103">Ta bort den diagnostiska enheten från globalt område eller API-nivå.</span><span class="sxs-lookup"><span data-stu-id="8b89f-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="8b89f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b89f-104">SYNTAX</span></span>

### <span data-ttu-id="8b89f-105">ByResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b89f-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b89f-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8b89f-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b89f-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b89f-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b89f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b89f-108">DESCRIPTION</span></span>
<span data-ttu-id="8b89f-109">Cmdlet **Remove-AzApiManagementDiagnostic** tar bort den diagnostiska enhet som anges av `DiagnosticId` från globalt scope eller ett `ApiId` scope</span><span class="sxs-lookup"><span data-stu-id="8b89f-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="8b89f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b89f-110">EXAMPLES</span></span>

### <span data-ttu-id="8b89f-111">Exempel 1: ta bort den diagnostiska enheten</span><span class="sxs-lookup"><span data-stu-id="8b89f-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="8b89f-112">I det här exemplet tas diagnostik bort `applicationinsights` från API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8b89f-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="8b89f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b89f-113">PARAMETERS</span></span>

### <span data-ttu-id="8b89f-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8b89f-114">-ApiId</span></span>
<span data-ttu-id="8b89f-115">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="8b89f-115">Identifier of the API.</span></span>
<span data-ttu-id="8b89f-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8b89f-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b89f-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8b89f-117">-Context</span></span>
<span data-ttu-id="8b89f-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8b89f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8b89f-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8b89f-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b89f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b89f-120">-DefaultProfile</span></span>
<span data-ttu-id="8b89f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b89f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b89f-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8b89f-122">-DiagnosticId</span></span>
<span data-ttu-id="8b89f-123">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="8b89f-123">Identifier of existing product.</span></span>
<span data-ttu-id="8b89f-124">Om det anges returnerar produkt-scope-policyn.</span><span class="sxs-lookup"><span data-stu-id="8b89f-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="8b89f-125">De här parametrarna är valfria.</span><span class="sxs-lookup"><span data-stu-id="8b89f-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b89f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b89f-126">-InputObject</span></span>
<span data-ttu-id="8b89f-127">Instans av PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8b89f-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="8b89f-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8b89f-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b89f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b89f-129">-PassThru</span></span>
<span data-ttu-id="8b89f-130">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="8b89f-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8b89f-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8b89f-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="8b89f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b89f-132">-ResourceId</span></span>
<span data-ttu-id="8b89f-133">Arm ResourceId för diagnostik.</span><span class="sxs-lookup"><span data-stu-id="8b89f-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="8b89f-134">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8b89f-134">This parameter is required.</span></span>

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

### <span data-ttu-id="8b89f-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b89f-135">-Confirm</span></span>
<span data-ttu-id="8b89f-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b89f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b89f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b89f-137">-WhatIf</span></span>
<span data-ttu-id="8b89f-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b89f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b89f-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b89f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b89f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b89f-140">CommonParameters</span></span>
<span data-ttu-id="8b89f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b89f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b89f-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b89f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b89f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b89f-143">INPUTS</span></span>

### <span data-ttu-id="8b89f-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8b89f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b89f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8b89f-145">System.String</span></span>

### <span data-ttu-id="8b89f-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b89f-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b89f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b89f-147">OUTPUTS</span></span>

### <span data-ttu-id="8b89f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b89f-148">System.Boolean</span></span>

## <span data-ttu-id="8b89f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b89f-149">NOTES</span></span>

## <span data-ttu-id="8b89f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b89f-150">RELATED LINKS</span></span>

[<span data-ttu-id="8b89f-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b89f-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8b89f-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b89f-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8b89f-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b89f-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)