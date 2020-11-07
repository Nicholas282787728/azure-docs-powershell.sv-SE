---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 5caef678df0aef88f4655c031d53e995920d0379
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745790"
---
# <span data-ttu-id="b903c-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b903c-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="b903c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b903c-102">SYNOPSIS</span></span>
<span data-ttu-id="b903c-103">Skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="b903c-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="b903c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b903c-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b903c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b903c-105">DESCRIPTION</span></span>
<span data-ttu-id="b903c-106">Skapar en ny backend-enhet i API-hantering.</span><span class="sxs-lookup"><span data-stu-id="b903c-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="b903c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b903c-107">EXAMPLES</span></span>

### <span data-ttu-id="b903c-108">Skapa en server del 123 med ett grundläggande Authorization-schema</span><span class="sxs-lookup"><span data-stu-id="b903c-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b903c-109">Skapar en ny server del</span><span class="sxs-lookup"><span data-stu-id="b903c-109">Creates a new Backend</span></span>

## <span data-ttu-id="b903c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b903c-110">PARAMETERS</span></span>

### <span data-ttu-id="b903c-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="b903c-111">-BackendId</span></span>
<span data-ttu-id="b903c-112">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="b903c-112">Identifier of new backend.</span></span>
<span data-ttu-id="b903c-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-113">This parameter is optional.</span></span>
<span data-ttu-id="b903c-114">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="b903c-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b903c-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b903c-115">-Context</span></span>
<span data-ttu-id="b903c-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b903c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b903c-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b903c-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b903c-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b903c-118">-Credential</span></span>
<span data-ttu-id="b903c-119">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="b903c-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b903c-121">-DefaultProfile</span></span>
<span data-ttu-id="b903c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b903c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b903c-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b903c-123">-Description</span></span>
<span data-ttu-id="b903c-124">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="b903c-124">Backend Description.</span></span>
<span data-ttu-id="b903c-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b903c-126">-Protocol</span></span>
<span data-ttu-id="b903c-127">Backend-kommunikations protokoll.</span><span class="sxs-lookup"><span data-stu-id="b903c-127">Backend Communication protocol.</span></span>
<span data-ttu-id="b903c-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b903c-128">This parameter is required.</span></span>
<span data-ttu-id="b903c-129">Giltiga värden är "http" och "SOAP".</span><span class="sxs-lookup"><span data-stu-id="b903c-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b903c-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="b903c-130">-Proxy</span></span>
<span data-ttu-id="b903c-131">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="b903c-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b903c-133">-ResourceId</span></span>
<span data-ttu-id="b903c-134">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="b903c-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="b903c-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-135">This parameter is optional.</span></span>
<span data-ttu-id="b903c-136">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="b903c-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="b903c-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b903c-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="b903c-138">Information om tjänstens infrastruktur Server.</span><span class="sxs-lookup"><span data-stu-id="b903c-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="b903c-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="b903c-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="b903c-141">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="b903c-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="b903c-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="b903c-144">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="b903c-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-146">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="b903c-146">-Title</span></span>
<span data-ttu-id="b903c-147">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-147">Backend Title.</span></span>
<span data-ttu-id="b903c-148">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b903c-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="b903c-149">-URL</span><span class="sxs-lookup"><span data-stu-id="b903c-149">-Url</span></span>
<span data-ttu-id="b903c-150">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="b903c-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="b903c-151">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b903c-151">This parameter is required.</span></span>

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

### <span data-ttu-id="b903c-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b903c-152">-Confirm</span></span>
<span data-ttu-id="b903c-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b903c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b903c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b903c-154">-WhatIf</span></span>
<span data-ttu-id="b903c-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b903c-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b903c-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b903c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b903c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b903c-157">CommonParameters</span></span>
<span data-ttu-id="b903c-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b903c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b903c-159">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b903c-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b903c-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b903c-160">INPUTS</span></span>

### <span data-ttu-id="b903c-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b903c-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b903c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b903c-162">System.String</span></span>

### <span data-ttu-id="b903c-163">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b903c-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b903c-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b903c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="b903c-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b903c-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="b903c-166">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b903c-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="b903c-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b903c-167">OUTPUTS</span></span>

### <span data-ttu-id="b903c-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b903c-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b903c-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b903c-169">NOTES</span></span>

## <span data-ttu-id="b903c-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b903c-170">RELATED LINKS</span></span>

[<span data-ttu-id="b903c-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b903c-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="b903c-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b903c-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b903c-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b903c-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b903c-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b903c-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b903c-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b903c-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

