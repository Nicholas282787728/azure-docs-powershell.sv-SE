---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271107"
---
# <span data-ttu-id="d6534-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="d6534-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6534-102">SYNOPSIS</span></span>
<span data-ttu-id="d6534-103">Skapar en ny diagnostik i det globala scopet eller API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="d6534-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="d6534-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6534-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6534-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6534-105">DESCRIPTION</span></span>
<span data-ttu-id="d6534-106">Cmdlet **New-AzApiManagementDiagnostic** skapar en diagnostisk enhet antingen i globalt scope eller specifikt API-omfattning.</span><span class="sxs-lookup"><span data-stu-id="d6534-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="d6534-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6534-107">EXAMPLES</span></span>

### <span data-ttu-id="d6534-108">Exempel 1: skapa en ny global scope-diagnostik</span><span class="sxs-lookup"><span data-stu-id="d6534-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="d6534-109">I det här exemplet skapas en diagnostisk enhet med globalt scope.</span><span class="sxs-lookup"><span data-stu-id="d6534-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="d6534-110">Exempel 2: skapa en diagnostik med API-omfattning</span><span class="sxs-lookup"><span data-stu-id="d6534-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="d6534-111">Exemplet ovan skapar en diagnostik för API: t `httpbin` för att logga sidhuvudet och 100 byte av brödtext till `azuremonitor` loggning.</span><span class="sxs-lookup"><span data-stu-id="d6534-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="d6534-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6534-112">PARAMETERS</span></span>

### <span data-ttu-id="d6534-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="d6534-113">-AlwaysLog</span></span>
<span data-ttu-id="d6534-114">Anger för vilken typ av meddelanden som du inte vill använda.</span><span class="sxs-lookup"><span data-stu-id="d6534-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="d6534-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d6534-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="d6534-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d6534-116">-ApiId</span></span>
<span data-ttu-id="d6534-117">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="d6534-117">Identifier of existing API.</span></span>
<span data-ttu-id="d6534-118">Ange API-scope-princip om den anges.</span><span class="sxs-lookup"><span data-stu-id="d6534-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="d6534-119">De här parametrarna är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="d6534-119">This parameters is required.</span></span>

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

### <span data-ttu-id="d6534-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-120">-BackendSetting</span></span>
<span data-ttu-id="d6534-121">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till Server delen.</span><span class="sxs-lookup"><span data-stu-id="d6534-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="d6534-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d6534-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d6534-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d6534-123">-Context</span></span>
<span data-ttu-id="d6534-124">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6534-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6534-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d6534-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6534-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6534-126">-DefaultProfile</span></span>
<span data-ttu-id="d6534-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6534-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6534-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="d6534-128">-DiagnosticId</span></span>
<span data-ttu-id="d6534-129">Identifierare för Diagnostics-entiteten.</span><span class="sxs-lookup"><span data-stu-id="d6534-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="d6534-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d6534-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d6534-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-131">-FrontEndSetting</span></span>
<span data-ttu-id="d6534-132">Diagnostisk inställning för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d6534-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="d6534-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d6534-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d6534-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d6534-134">-LoggerId</span></span>
<span data-ttu-id="d6534-135">Identifierare för den loggade för att push-Diagnostics to.</span><span class="sxs-lookup"><span data-stu-id="d6534-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="d6534-136">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d6534-136">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6534-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-137">-SamplingSetting</span></span>
<span data-ttu-id="d6534-138">Inställning av diagnostik.</span><span class="sxs-lookup"><span data-stu-id="d6534-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="d6534-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d6534-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d6534-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6534-140">-Confirm</span></span>
<span data-ttu-id="d6534-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6534-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6534-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6534-142">-WhatIf</span></span>
<span data-ttu-id="d6534-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6534-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6534-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6534-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6534-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6534-145">CommonParameters</span></span>
<span data-ttu-id="d6534-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6534-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6534-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6534-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6534-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6534-148">INPUTS</span></span>

### <span data-ttu-id="d6534-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6534-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6534-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d6534-150">System.String</span></span>

### <span data-ttu-id="d6534-151">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="d6534-152">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d6534-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6534-153">OUTPUTS</span></span>

### <span data-ttu-id="d6534-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="d6534-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6534-155">NOTES</span></span>

## <span data-ttu-id="d6534-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6534-156">RELATED LINKS</span></span>

[<span data-ttu-id="d6534-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d6534-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d6534-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d6534-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6534-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="d6534-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d6534-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)