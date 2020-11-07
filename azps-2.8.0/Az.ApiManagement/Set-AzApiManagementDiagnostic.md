---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745667"
---
# <span data-ttu-id="b4596-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b4596-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="b4596-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4596-102">SYNOPSIS</span></span>
<span data-ttu-id="b4596-103">Ändrar en API-hanterings diagnos vid global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="b4596-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="b4596-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4596-104">SYNTAX</span></span>

### <span data-ttu-id="b4596-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="b4596-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4596-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4596-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4596-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4596-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4596-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4596-108">DESCRIPTION</span></span>
<span data-ttu-id="b4596-109">Cmdlet **set-AzApiManagementDiagnostic** uppdaterar den diagnostik som har kon figurer ATS i global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="b4596-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="b4596-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4596-110">EXAMPLES</span></span>

### <span data-ttu-id="b4596-111">Exempel 1: ändra en diagnostik i global omfattning</span><span class="sxs-lookup"><span data-stu-id="b4596-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="b4596-112">Det här kommandot ändrar den angivna standardvärden för diagnos sampling från 100 till 50%</span><span class="sxs-lookup"><span data-stu-id="b4596-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="b4596-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4596-113">PARAMETERS</span></span>

### <span data-ttu-id="b4596-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="b4596-114">-AlwaysLog</span></span>
<span data-ttu-id="b4596-115">Anger för vilken typ av meddelanden som du inte vill använda.</span><span class="sxs-lookup"><span data-stu-id="b4596-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="b4596-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b4596-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4596-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b4596-117">-ApiId</span></span>
<span data-ttu-id="b4596-118">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="b4596-118">Identifier of existing API.</span></span>
<span data-ttu-id="b4596-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b4596-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4596-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="b4596-120">-BackendSetting</span></span>
<span data-ttu-id="b4596-121">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till Server delen.</span><span class="sxs-lookup"><span data-stu-id="b4596-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="b4596-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b4596-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4596-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b4596-123">-Context</span></span>
<span data-ttu-id="b4596-124">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b4596-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4596-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4596-125">This parameter is required.</span></span>

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

### <span data-ttu-id="b4596-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4596-126">-DefaultProfile</span></span>
<span data-ttu-id="b4596-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4596-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4596-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="b4596-128">-DiagnosticId</span></span>
<span data-ttu-id="b4596-129">Identifierare för befintlig diagnostik.</span><span class="sxs-lookup"><span data-stu-id="b4596-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="b4596-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4596-130">This parameter is required.</span></span>

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

### <span data-ttu-id="b4596-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="b4596-131">-FrontEndSetting</span></span>
<span data-ttu-id="b4596-132">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b4596-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="b4596-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b4596-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4596-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4596-134">-InputObject</span></span>
<span data-ttu-id="b4596-135">Instans av PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b4596-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="b4596-136">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4596-136">This parameter is required.</span></span>

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

### <span data-ttu-id="b4596-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="b4596-137">-LoggerId</span></span>
<span data-ttu-id="b4596-138">Identifierare för den loggade för att push-Diagnostics to.</span><span class="sxs-lookup"><span data-stu-id="b4596-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="b4596-139">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4596-139">This parameter is required.</span></span>

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

### <span data-ttu-id="b4596-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4596-140">-PassThru</span></span>
<span data-ttu-id="b4596-141">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic typ som representerar den inställda diagnostiken.</span><span class="sxs-lookup"><span data-stu-id="b4596-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="b4596-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4596-142">-ResourceId</span></span>
<span data-ttu-id="b4596-143">Arm-ResourceId för diagnostik eller API-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="b4596-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="b4596-144">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4596-144">This parameter is required.</span></span>

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

### <span data-ttu-id="b4596-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="b4596-145">-SamplingSetting</span></span>
<span data-ttu-id="b4596-146">Inställning av diagnostik.</span><span class="sxs-lookup"><span data-stu-id="b4596-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="b4596-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b4596-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4596-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4596-148">-Confirm</span></span>
<span data-ttu-id="b4596-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4596-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4596-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4596-150">-WhatIf</span></span>
<span data-ttu-id="b4596-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4596-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4596-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4596-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4596-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4596-153">CommonParameters</span></span>
<span data-ttu-id="b4596-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4596-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4596-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4596-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4596-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4596-156">INPUTS</span></span>

### <span data-ttu-id="b4596-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4596-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4596-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b4596-158">System.String</span></span>

### <span data-ttu-id="b4596-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b4596-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="b4596-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="b4596-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="b4596-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b4596-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="b4596-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b4596-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4596-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4596-163">OUTPUTS</span></span>

### <span data-ttu-id="b4596-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b4596-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="b4596-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4596-165">NOTES</span></span>

## <span data-ttu-id="b4596-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4596-166">RELATED LINKS</span></span>
