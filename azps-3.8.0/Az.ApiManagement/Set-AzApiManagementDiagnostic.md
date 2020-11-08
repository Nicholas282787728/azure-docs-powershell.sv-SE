---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091583"
---
# <span data-ttu-id="26883-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="26883-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="26883-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26883-102">SYNOPSIS</span></span>
<span data-ttu-id="26883-103">Ändrar en API-hanterings diagnos vid global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="26883-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="26883-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26883-104">SYNTAX</span></span>

### <span data-ttu-id="26883-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="26883-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26883-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="26883-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26883-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26883-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26883-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26883-108">DESCRIPTION</span></span>
<span data-ttu-id="26883-109">Cmdlet **set-AzApiManagementDiagnostic** uppdaterar den diagnostik som har kon figurer ATS i global or API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="26883-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="26883-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26883-110">EXAMPLES</span></span>

### <span data-ttu-id="26883-111">Exempel 1: ändra en diagnostik i global omfattning</span><span class="sxs-lookup"><span data-stu-id="26883-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="26883-112">Det här kommandot ändrar den angivna standardvärden för diagnos sampling från 100 till 50%</span><span class="sxs-lookup"><span data-stu-id="26883-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="26883-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26883-113">PARAMETERS</span></span>

### <span data-ttu-id="26883-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="26883-114">-AlwaysLog</span></span>
<span data-ttu-id="26883-115">Anger för vilken typ av meddelanden som du inte vill använda.</span><span class="sxs-lookup"><span data-stu-id="26883-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="26883-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="26883-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="26883-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="26883-117">-ApiId</span></span>
<span data-ttu-id="26883-118">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="26883-118">Identifier of existing API.</span></span>
<span data-ttu-id="26883-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="26883-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="26883-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="26883-120">-BackendSetting</span></span>
<span data-ttu-id="26883-121">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till Server delen.</span><span class="sxs-lookup"><span data-stu-id="26883-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="26883-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="26883-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="26883-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="26883-123">-Context</span></span>
<span data-ttu-id="26883-124">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="26883-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="26883-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="26883-125">This parameter is required.</span></span>

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

### <span data-ttu-id="26883-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26883-126">-DefaultProfile</span></span>
<span data-ttu-id="26883-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26883-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26883-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="26883-128">-DiagnosticId</span></span>
<span data-ttu-id="26883-129">Identifierare för befintlig diagnostik.</span><span class="sxs-lookup"><span data-stu-id="26883-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="26883-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="26883-130">This parameter is required.</span></span>

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

### <span data-ttu-id="26883-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="26883-131">-FrontEndSetting</span></span>
<span data-ttu-id="26883-132">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="26883-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="26883-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="26883-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="26883-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26883-134">-InputObject</span></span>
<span data-ttu-id="26883-135">Instans av PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="26883-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="26883-136">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="26883-136">This parameter is required.</span></span>

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

### <span data-ttu-id="26883-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="26883-137">-LoggerId</span></span>
<span data-ttu-id="26883-138">Identifierare för den loggade för att push-Diagnostics to.</span><span class="sxs-lookup"><span data-stu-id="26883-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="26883-139">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="26883-139">This parameter is required.</span></span>

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

### <span data-ttu-id="26883-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26883-140">-PassThru</span></span>
<span data-ttu-id="26883-141">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic typ som representerar den inställda diagnostiken.</span><span class="sxs-lookup"><span data-stu-id="26883-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="26883-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26883-142">-ResourceId</span></span>
<span data-ttu-id="26883-143">Arm-ResourceId för diagnostik eller API-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="26883-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="26883-144">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="26883-144">This parameter is required.</span></span>

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

### <span data-ttu-id="26883-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="26883-145">-SamplingSetting</span></span>
<span data-ttu-id="26883-146">Inställning av diagnostik.</span><span class="sxs-lookup"><span data-stu-id="26883-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="26883-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="26883-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="26883-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26883-148">-Confirm</span></span>
<span data-ttu-id="26883-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26883-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26883-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26883-150">-WhatIf</span></span>
<span data-ttu-id="26883-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26883-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26883-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26883-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26883-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26883-153">CommonParameters</span></span>
<span data-ttu-id="26883-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26883-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26883-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26883-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26883-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26883-156">INPUTS</span></span>

### <span data-ttu-id="26883-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26883-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26883-158">System. String</span><span class="sxs-lookup"><span data-stu-id="26883-158">System.String</span></span>

### <span data-ttu-id="26883-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="26883-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="26883-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="26883-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="26883-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="26883-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="26883-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26883-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26883-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26883-163">OUTPUTS</span></span>

### <span data-ttu-id="26883-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="26883-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="26883-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26883-165">NOTES</span></span>

## <span data-ttu-id="26883-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26883-166">RELATED LINKS</span></span>
