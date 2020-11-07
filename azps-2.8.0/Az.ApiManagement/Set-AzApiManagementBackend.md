---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745670"
---
# <span data-ttu-id="ace09-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ace09-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="ace09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ace09-102">SYNOPSIS</span></span>
<span data-ttu-id="ace09-103">Uppdaterar en server del.</span><span class="sxs-lookup"><span data-stu-id="ace09-103">Updates a Backend.</span></span>

## <span data-ttu-id="ace09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ace09-104">SYNTAX</span></span>

### <span data-ttu-id="ace09-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ace09-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace09-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ace09-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ace09-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ace09-107">DESCRIPTION</span></span>
<span data-ttu-id="ace09-108">Uppdaterar en befintlig server del i API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="ace09-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="ace09-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ace09-109">EXAMPLES</span></span>

### <span data-ttu-id="ace09-110">Uppdaterar beskrivningen av Server delen 123</span><span class="sxs-lookup"><span data-stu-id="ace09-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="ace09-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ace09-111">PARAMETERS</span></span>

### <span data-ttu-id="ace09-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ace09-112">-BackendId</span></span>
<span data-ttu-id="ace09-113">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="ace09-113">Identifier of new backend.</span></span>
<span data-ttu-id="ace09-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ace09-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ace09-115">-Context</span></span>
<span data-ttu-id="ace09-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ace09-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ace09-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ace09-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ace09-118">-Credential</span></span>
<span data-ttu-id="ace09-119">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="ace09-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace09-121">-DefaultProfile</span></span>
<span data-ttu-id="ace09-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ace09-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace09-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ace09-123">-Description</span></span>
<span data-ttu-id="ace09-124">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="ace09-124">Backend Description.</span></span>
<span data-ttu-id="ace09-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ace09-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ace09-126">-InputObject</span></span>
<span data-ttu-id="ace09-127">Instans av PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="ace09-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="ace09-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ace09-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ace09-129">-PassThru</span></span>
<span data-ttu-id="ace09-130">Anger att denna cmdlet returnerar  **PsApiManagementBackend** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ace09-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ace09-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ace09-131">-Protocol</span></span>
<span data-ttu-id="ace09-132">Backend Communication Protocol (http eller SOAP).</span><span class="sxs-lookup"><span data-stu-id="ace09-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="ace09-133">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="ace09-133">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="ace09-134">-Proxy</span></span>
<span data-ttu-id="ace09-135">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="ace09-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace09-137">-ResourceId</span></span>
<span data-ttu-id="ace09-138">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="ace09-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="ace09-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-139">This parameter is optional.</span></span>
<span data-ttu-id="ace09-140">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="ace09-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="ace09-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ace09-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="ace09-142">Information om tjänstens infrastruktur Server.</span><span class="sxs-lookup"><span data-stu-id="ace09-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="ace09-143">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-143">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="ace09-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="ace09-145">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="ace09-146">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-146">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="ace09-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="ace09-148">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="ace09-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-149">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace09-150">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="ace09-150">-Title</span></span>
<span data-ttu-id="ace09-151">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-151">Backend Title.</span></span>
<span data-ttu-id="ace09-152">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="ace09-153">-URL</span><span class="sxs-lookup"><span data-stu-id="ace09-153">-Url</span></span>
<span data-ttu-id="ace09-154">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="ace09-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="ace09-155">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ace09-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="ace09-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ace09-156">-Confirm</span></span>
<span data-ttu-id="ace09-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ace09-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ace09-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ace09-158">-WhatIf</span></span>
<span data-ttu-id="ace09-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ace09-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ace09-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ace09-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ace09-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace09-161">CommonParameters</span></span>
<span data-ttu-id="ace09-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace09-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace09-163">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ace09-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace09-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ace09-164">INPUTS</span></span>

### <span data-ttu-id="ace09-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ace09-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ace09-166">System. String</span><span class="sxs-lookup"><span data-stu-id="ace09-166">System.String</span></span>

### <span data-ttu-id="ace09-167">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ace09-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ace09-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ace09-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="ace09-169">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ace09-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="ace09-170">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ace09-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="ace09-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ace09-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ace09-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ace09-172">OUTPUTS</span></span>

### <span data-ttu-id="ace09-173">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ace09-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="ace09-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ace09-174">NOTES</span></span>

## <span data-ttu-id="ace09-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ace09-175">RELATED LINKS</span></span>

[<span data-ttu-id="ace09-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ace09-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="ace09-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ace09-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ace09-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ace09-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ace09-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ace09-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ace09-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ace09-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)