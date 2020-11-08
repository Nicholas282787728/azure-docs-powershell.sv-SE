---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101765"
---
# <span data-ttu-id="e2560-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e2560-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="e2560-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2560-102">SYNOPSIS</span></span>
<span data-ttu-id="e2560-103">Ändrar en API-hanterings diagnos vid global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="e2560-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="e2560-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2560-104">SYNTAX</span></span>

### <span data-ttu-id="e2560-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="e2560-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2560-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2560-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2560-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2560-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2560-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2560-108">DESCRIPTION</span></span>
<span data-ttu-id="e2560-109">Cmdlet **set-AzApiManagementDiagnostic** uppdaterar den diagnostik som har kon figurer ATS i global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="e2560-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="e2560-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2560-110">EXAMPLES</span></span>

### <span data-ttu-id="e2560-111">Exempel 1: ändra en diagnostik i global omfattning</span><span class="sxs-lookup"><span data-stu-id="e2560-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="e2560-112">Det här kommandot ändrar den angivna standardvärden för diagnos sampling från 100 till 50%</span><span class="sxs-lookup"><span data-stu-id="e2560-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="e2560-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e2560-113">Example 2</span></span>

<span data-ttu-id="e2560-114">Ändrar en API-hanterings diagnos vid global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="e2560-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="e2560-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="e2560-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="e2560-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2560-116">PARAMETERS</span></span>

### <span data-ttu-id="e2560-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="e2560-117">-AlwaysLog</span></span>
<span data-ttu-id="e2560-118">Anger för vilken typ av meddelanden som du inte vill använda.</span><span class="sxs-lookup"><span data-stu-id="e2560-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="e2560-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e2560-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e2560-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e2560-120">-ApiId</span></span>
<span data-ttu-id="e2560-121">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="e2560-121">Identifier of existing API.</span></span>
<span data-ttu-id="e2560-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e2560-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="e2560-123">-BackendSetting</span></span>
<span data-ttu-id="e2560-124">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till Server delen.</span><span class="sxs-lookup"><span data-stu-id="e2560-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="e2560-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e2560-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-126">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e2560-126">-Context</span></span>
<span data-ttu-id="e2560-127">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e2560-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e2560-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e2560-128">This parameter is required.</span></span>

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

### <span data-ttu-id="e2560-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2560-129">-DefaultProfile</span></span>
<span data-ttu-id="e2560-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2560-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2560-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="e2560-131">-DiagnosticId</span></span>
<span data-ttu-id="e2560-132">Identifierare för befintlig diagnostik.</span><span class="sxs-lookup"><span data-stu-id="e2560-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="e2560-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e2560-133">This parameter is required.</span></span>

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

### <span data-ttu-id="e2560-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="e2560-134">-FrontEndSetting</span></span>
<span data-ttu-id="e2560-135">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e2560-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="e2560-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e2560-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2560-137">-InputObject</span></span>
<span data-ttu-id="e2560-138">Instans av PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e2560-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="e2560-139">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e2560-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e2560-140">-LoggerId</span></span>
<span data-ttu-id="e2560-141">Identifierare för den loggade för att push-Diagnostics to.</span><span class="sxs-lookup"><span data-stu-id="e2560-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="e2560-142">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e2560-142">This parameter is required.</span></span>

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

### <span data-ttu-id="e2560-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2560-143">-PassThru</span></span>
<span data-ttu-id="e2560-144">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic typ som representerar den inställda diagnostiken.</span><span class="sxs-lookup"><span data-stu-id="e2560-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="e2560-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2560-145">-ResourceId</span></span>
<span data-ttu-id="e2560-146">Arm-ResourceId för diagnostik eller API-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="e2560-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="e2560-147">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e2560-147">This parameter is required.</span></span>

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

### <span data-ttu-id="e2560-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e2560-148">-SamplingSetting</span></span>
<span data-ttu-id="e2560-149">Inställning av diagnostik.</span><span class="sxs-lookup"><span data-stu-id="e2560-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="e2560-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e2560-150">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2560-151">-Confirm</span></span>
<span data-ttu-id="e2560-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2560-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2560-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2560-153">-WhatIf</span></span>
<span data-ttu-id="e2560-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2560-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2560-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2560-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2560-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2560-156">CommonParameters</span></span>
<span data-ttu-id="e2560-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2560-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2560-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2560-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2560-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2560-159">INPUTS</span></span>

### <span data-ttu-id="e2560-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e2560-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e2560-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e2560-161">System.String</span></span>

### <span data-ttu-id="e2560-162">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e2560-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="e2560-163">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e2560-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="e2560-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e2560-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="e2560-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e2560-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e2560-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2560-166">OUTPUTS</span></span>

### <span data-ttu-id="e2560-167">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e2560-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="e2560-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2560-168">NOTES</span></span>

## <span data-ttu-id="e2560-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2560-169">RELATED LINKS</span></span>
