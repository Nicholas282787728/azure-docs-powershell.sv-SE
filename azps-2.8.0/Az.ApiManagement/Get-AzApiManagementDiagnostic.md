---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2ff4660a0e8f4929e8f79c20a8e42e0deac11f3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745841"
---
# <span data-ttu-id="737eb-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="737eb-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="737eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="737eb-102">SYNOPSIS</span></span>
<span data-ttu-id="737eb-103">Få information om den diagnostik som är konfigurerad på tjänst nivå eller API-nivå.</span><span class="sxs-lookup"><span data-stu-id="737eb-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="737eb-104">Diagnostik används för att logga begär Anden/svar från API Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="737eb-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="737eb-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="737eb-105">SYNTAX</span></span>

### <span data-ttu-id="737eb-106">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="737eb-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="737eb-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="737eb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="737eb-108">DESCRIPTION</span></span>
<span data-ttu-id="737eb-109">**Get-AzApiManagementDiagnostic** hämtar information om diagnostikverktygen som har kon figurer ATS i API-hanterings tjänsten i ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="737eb-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="737eb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="737eb-110">EXAMPLES</span></span>

### <span data-ttu-id="737eb-111">Exempel 1: Hämta all diagnostik som är konfigurerad för klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="737eb-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="737eb-112">Det här kommandot får all diagnostik som är konfigurerad i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="737eb-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="737eb-113">Exempel 2: få all diagnostik konfigurerad i API-omfattningen</span><span class="sxs-lookup"><span data-stu-id="737eb-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="737eb-114">Det här kommandot får all diagnostik som har kon figurer ATS i `echo-api` API-omfattningen</span><span class="sxs-lookup"><span data-stu-id="737eb-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="737eb-115">Exempel 3: Hämta API-tidsdiagnostiken som anges av ett ID</span><span class="sxs-lookup"><span data-stu-id="737eb-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="737eb-116">Det här kommandot får `applicationinsights` diagnostiken konfigurerad i API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="737eb-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="737eb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="737eb-117">PARAMETERS</span></span>

### <span data-ttu-id="737eb-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="737eb-118">-ApiId</span></span>
<span data-ttu-id="737eb-119">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="737eb-119">Identifier of existing API.</span></span>
<span data-ttu-id="737eb-120">Om det här är angivet returneras API-autentiseringsomfång.</span><span class="sxs-lookup"><span data-stu-id="737eb-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="737eb-121">De här parametrarna är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="737eb-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737eb-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="737eb-122">-Context</span></span>
<span data-ttu-id="737eb-123">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="737eb-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="737eb-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="737eb-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737eb-125">-DefaultProfile</span></span>
<span data-ttu-id="737eb-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="737eb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737eb-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="737eb-127">-DiagnosticId</span></span>
<span data-ttu-id="737eb-128">Identifierare för befintlig diagnostik.</span><span class="sxs-lookup"><span data-stu-id="737eb-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="737eb-129">Om det anges returnerar produkt-scope-policyn.</span><span class="sxs-lookup"><span data-stu-id="737eb-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="737eb-130">De här parametrarna är valfria.</span><span class="sxs-lookup"><span data-stu-id="737eb-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="737eb-131">-ResourceId</span></span>
<span data-ttu-id="737eb-132">Arm-ID för en diagnostik eller API-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="737eb-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="737eb-133">Om det här alternativet är angivet görs en sökning efter diagnostik enligt ID.</span><span class="sxs-lookup"><span data-stu-id="737eb-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="737eb-134">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="737eb-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737eb-135">CommonParameters</span></span>
<span data-ttu-id="737eb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737eb-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737eb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737eb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="737eb-138">INPUTS</span></span>

### <span data-ttu-id="737eb-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="737eb-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="737eb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="737eb-140">System.String</span></span>

## <span data-ttu-id="737eb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="737eb-141">OUTPUTS</span></span>

### <span data-ttu-id="737eb-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="737eb-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="737eb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="737eb-143">NOTES</span></span>

## <span data-ttu-id="737eb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="737eb-144">RELATED LINKS</span></span>
