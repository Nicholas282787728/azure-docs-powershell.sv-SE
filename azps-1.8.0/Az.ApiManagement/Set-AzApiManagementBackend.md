---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917702"
---
# <span data-ttu-id="a1ffc-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a1ffc-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="a1ffc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ffc-103">Uppdaterar en server del.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-103">Updates a Backend.</span></span>

## <span data-ttu-id="a1ffc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1ffc-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1ffc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="a1ffc-106">Uppdaterar en befintlig server del i API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="a1ffc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="a1ffc-108">Uppdaterar beskrivningen av Server delen 123</span><span class="sxs-lookup"><span data-stu-id="a1ffc-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="a1ffc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1ffc-109">PARAMETERS</span></span>

### <span data-ttu-id="a1ffc-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="a1ffc-110">-BackendId</span></span>
<span data-ttu-id="a1ffc-111">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-111">Identifier of new backend.</span></span>
<span data-ttu-id="a1ffc-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-112">This parameter is required.</span></span>

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

### <span data-ttu-id="a1ffc-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a1ffc-113">-Context</span></span>
<span data-ttu-id="a1ffc-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a1ffc-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ffc-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a1ffc-116">-Credential</span></span>
<span data-ttu-id="a1ffc-117">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="a1ffc-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ffc-119">-DefaultProfile</span></span>
<span data-ttu-id="a1ffc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1ffc-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a1ffc-121">-Description</span></span>
<span data-ttu-id="a1ffc-122">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-122">Backend Description.</span></span>
<span data-ttu-id="a1ffc-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1ffc-124">-PassThru</span></span>
<span data-ttu-id="a1ffc-125">Anger att denna cmdlet returnerar  **PsApiManagementBackend** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1ffc-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a1ffc-126">-Protocol</span></span>
<span data-ttu-id="a1ffc-127">Backend Communication Protocol (http eller SOAP).</span><span class="sxs-lookup"><span data-stu-id="a1ffc-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="a1ffc-128">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="a1ffc-128">This parameter is optional</span></span>

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

### <span data-ttu-id="a1ffc-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="a1ffc-129">-Proxy</span></span>
<span data-ttu-id="a1ffc-130">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="a1ffc-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ffc-132">-ResourceId</span></span>
<span data-ttu-id="a1ffc-133">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="a1ffc-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-134">This parameter is optional.</span></span>
<span data-ttu-id="a1ffc-135">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="a1ffc-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a1ffc-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="a1ffc-137">Information om tjänstens infrastruktur Server.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="a1ffc-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="a1ffc-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="a1ffc-140">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="a1ffc-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="a1ffc-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="a1ffc-143">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="a1ffc-144">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-145">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="a1ffc-145">-Title</span></span>
<span data-ttu-id="a1ffc-146">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-146">Backend Title.</span></span>
<span data-ttu-id="a1ffc-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-148">-URL</span><span class="sxs-lookup"><span data-stu-id="a1ffc-148">-Url</span></span>
<span data-ttu-id="a1ffc-149">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="a1ffc-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1ffc-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1ffc-151">-Confirm</span></span>
<span data-ttu-id="a1ffc-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1ffc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1ffc-153">-WhatIf</span></span>
<span data-ttu-id="a1ffc-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1ffc-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1ffc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ffc-156">CommonParameters</span></span>
<span data-ttu-id="a1ffc-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ffc-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ffc-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ffc-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1ffc-159">INPUTS</span></span>

### <span data-ttu-id="a1ffc-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1ffc-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1ffc-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a1ffc-161">System.String</span></span>

### <span data-ttu-id="a1ffc-162">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1ffc-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1ffc-163">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a1ffc-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="a1ffc-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a1ffc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="a1ffc-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a1ffc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="a1ffc-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1ffc-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1ffc-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1ffc-167">OUTPUTS</span></span>

### <span data-ttu-id="a1ffc-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a1ffc-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a1ffc-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1ffc-169">NOTES</span></span>

## <span data-ttu-id="a1ffc-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1ffc-170">RELATED LINKS</span></span>

[<span data-ttu-id="a1ffc-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a1ffc-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="a1ffc-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a1ffc-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a1ffc-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a1ffc-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="a1ffc-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a1ffc-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a1ffc-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a1ffc-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
