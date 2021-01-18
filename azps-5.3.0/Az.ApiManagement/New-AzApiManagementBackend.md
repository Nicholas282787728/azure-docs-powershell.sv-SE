---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525043"
---
# <span data-ttu-id="c7758-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c7758-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="c7758-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7758-102">SYNOPSIS</span></span>
<span data-ttu-id="c7758-103">Skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="c7758-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="c7758-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7758-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7758-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7758-105">DESCRIPTION</span></span>
<span data-ttu-id="c7758-106">Skapar en ny backend-enhet i API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c7758-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="c7758-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7758-107">EXAMPLES</span></span>

### <span data-ttu-id="c7758-108">Exempel 1: skapa en server del 123 med ett grundläggande Authorization-schema</span><span class="sxs-lookup"><span data-stu-id="c7758-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="c7758-109">Skapar en ny server del</span><span class="sxs-lookup"><span data-stu-id="c7758-109">Creates a new Backend</span></span>

## <span data-ttu-id="c7758-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7758-110">PARAMETERS</span></span>

### <span data-ttu-id="c7758-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c7758-111">-BackendId</span></span>
<span data-ttu-id="c7758-112">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="c7758-112">Identifier of new backend.</span></span>
<span data-ttu-id="c7758-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-113">This parameter is optional.</span></span>
<span data-ttu-id="c7758-114">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="c7758-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="c7758-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c7758-115">-Context</span></span>
<span data-ttu-id="c7758-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c7758-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c7758-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c7758-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c7758-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="c7758-118">-Credential</span></span>
<span data-ttu-id="c7758-119">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="c7758-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7758-121">-DefaultProfile</span></span>
<span data-ttu-id="c7758-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7758-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7758-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c7758-123">-Description</span></span>
<span data-ttu-id="c7758-124">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="c7758-124">Backend Description.</span></span>
<span data-ttu-id="c7758-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c7758-126">-Protocol</span></span>
<span data-ttu-id="c7758-127">Backend-kommunikations protokoll.</span><span class="sxs-lookup"><span data-stu-id="c7758-127">Backend Communication protocol.</span></span>
<span data-ttu-id="c7758-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c7758-128">This parameter is required.</span></span>
<span data-ttu-id="c7758-129">Giltiga värden är "http" och "SOAP".</span><span class="sxs-lookup"><span data-stu-id="c7758-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="c7758-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="c7758-130">-Proxy</span></span>
<span data-ttu-id="c7758-131">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="c7758-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7758-133">-ResourceId</span></span>
<span data-ttu-id="c7758-134">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="c7758-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="c7758-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-135">This parameter is optional.</span></span>
<span data-ttu-id="c7758-136">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="c7758-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="c7758-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c7758-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="c7758-138">Information om tjänstens infrastruktur Server.</span><span class="sxs-lookup"><span data-stu-id="c7758-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="c7758-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="c7758-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="c7758-141">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="c7758-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="c7758-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="c7758-144">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="c7758-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-146">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="c7758-146">-Title</span></span>
<span data-ttu-id="c7758-147">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-147">Backend Title.</span></span>
<span data-ttu-id="c7758-148">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c7758-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7758-149">-URL</span><span class="sxs-lookup"><span data-stu-id="c7758-149">-Url</span></span>
<span data-ttu-id="c7758-150">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="c7758-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="c7758-151">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c7758-151">This parameter is required.</span></span>

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

### <span data-ttu-id="c7758-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7758-152">-Confirm</span></span>
<span data-ttu-id="c7758-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7758-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7758-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7758-154">-WhatIf</span></span>
<span data-ttu-id="c7758-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7758-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7758-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7758-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7758-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7758-157">CommonParameters</span></span>
<span data-ttu-id="c7758-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7758-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7758-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7758-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7758-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7758-160">INPUTS</span></span>

### <span data-ttu-id="c7758-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7758-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7758-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c7758-162">System.String</span></span>

### <span data-ttu-id="c7758-163">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c7758-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c7758-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c7758-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="c7758-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c7758-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="c7758-166">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c7758-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="c7758-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7758-167">OUTPUTS</span></span>

### <span data-ttu-id="c7758-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c7758-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="c7758-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7758-169">NOTES</span></span>

## <span data-ttu-id="c7758-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7758-170">RELATED LINKS</span></span>

[<span data-ttu-id="c7758-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c7758-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="c7758-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c7758-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="c7758-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c7758-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="c7758-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c7758-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="c7758-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c7758-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

