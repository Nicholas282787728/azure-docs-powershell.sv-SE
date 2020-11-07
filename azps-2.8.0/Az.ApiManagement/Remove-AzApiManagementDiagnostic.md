---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 430264a27cfff11416b322285a0db05b230b3bbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745711"
---
# <span data-ttu-id="9321c-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9321c-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9321c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9321c-102">SYNOPSIS</span></span>
<span data-ttu-id="9321c-103">Ta bort den diagnostiska enheten från globalt område eller API-nivå.</span><span class="sxs-lookup"><span data-stu-id="9321c-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="9321c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9321c-104">SYNTAX</span></span>

### <span data-ttu-id="9321c-105">ByResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9321c-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9321c-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9321c-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9321c-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9321c-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9321c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9321c-108">DESCRIPTION</span></span>
<span data-ttu-id="9321c-109">Cmdlet **Remove-AzApiManagementDiagnostic** tar bort den diagnostiska enhet som anges av `DiagnosticId` från globalt scope eller ett `ApiId` scope</span><span class="sxs-lookup"><span data-stu-id="9321c-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="9321c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9321c-110">EXAMPLES</span></span>

### <span data-ttu-id="9321c-111">Exempel 1: ta bort den diagnostiska enheten</span><span class="sxs-lookup"><span data-stu-id="9321c-111">Example 1 : Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="9321c-112">I det här exemplet tas diagnostik bort `applicationinsights` från API Management-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9321c-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="9321c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9321c-113">PARAMETERS</span></span>

### <span data-ttu-id="9321c-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9321c-114">-ApiId</span></span>
<span data-ttu-id="9321c-115">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="9321c-115">Identifier of the API.</span></span>
<span data-ttu-id="9321c-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9321c-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9321c-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9321c-117">-Context</span></span>
<span data-ttu-id="9321c-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9321c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9321c-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9321c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9321c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9321c-120">-DefaultProfile</span></span>
<span data-ttu-id="9321c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9321c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9321c-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9321c-122">-DiagnosticId</span></span>
<span data-ttu-id="9321c-123">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="9321c-123">Identifier of existing product.</span></span>
<span data-ttu-id="9321c-124">Om det anges returnerar produkt-scope-policyn.</span><span class="sxs-lookup"><span data-stu-id="9321c-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="9321c-125">De här parametrarna är valfria.</span><span class="sxs-lookup"><span data-stu-id="9321c-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="9321c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9321c-126">-InputObject</span></span>
<span data-ttu-id="9321c-127">Instans av PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9321c-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="9321c-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9321c-128">This parameter is required.</span></span>

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

### <span data-ttu-id="9321c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9321c-129">-PassThru</span></span>
<span data-ttu-id="9321c-130">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="9321c-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9321c-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9321c-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="9321c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9321c-132">-ResourceId</span></span>
<span data-ttu-id="9321c-133">Arm ResourceId för diagnostik.</span><span class="sxs-lookup"><span data-stu-id="9321c-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="9321c-134">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9321c-134">This parameter is required.</span></span>

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

### <span data-ttu-id="9321c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9321c-135">-Confirm</span></span>
<span data-ttu-id="9321c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9321c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9321c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9321c-137">-WhatIf</span></span>
<span data-ttu-id="9321c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9321c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9321c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9321c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9321c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9321c-140">CommonParameters</span></span>
<span data-ttu-id="9321c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9321c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9321c-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9321c-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9321c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9321c-143">INPUTS</span></span>

### <span data-ttu-id="9321c-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9321c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9321c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9321c-145">System.String</span></span>

### <span data-ttu-id="9321c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9321c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9321c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9321c-147">OUTPUTS</span></span>

### <span data-ttu-id="9321c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9321c-148">System.Boolean</span></span>

## <span data-ttu-id="9321c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9321c-149">NOTES</span></span>

## <span data-ttu-id="9321c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9321c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9321c-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9321c-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9321c-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9321c-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9321c-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9321c-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)