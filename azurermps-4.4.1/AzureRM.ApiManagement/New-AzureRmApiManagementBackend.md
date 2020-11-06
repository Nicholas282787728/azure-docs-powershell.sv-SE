---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578659"
---
# <span data-ttu-id="0bc9b-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0bc9b-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="0bc9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc9b-103">Skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bc9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bc9b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc9b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bc9b-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc9b-106">Skapar en ny backend-enhet i API-hantering.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="0bc9b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bc9b-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc9b-108">Skapa en server del 123 med ett grundläggande Authorization-schema</span><span class="sxs-lookup"><span data-stu-id="0bc9b-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="0bc9b-109">Skapar en ny server del</span><span class="sxs-lookup"><span data-stu-id="0bc9b-109">Creates a new Backend</span></span>

## <span data-ttu-id="0bc9b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bc9b-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc9b-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0bc9b-111">-BackendId</span></span>
<span data-ttu-id="0bc9b-112">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-112">Identifier of new backend.</span></span>
<span data-ttu-id="0bc9b-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-113">This parameter is optional.</span></span>
<span data-ttu-id="0bc9b-114">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="0bc9b-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0bc9b-115">-Context</span></span>
<span data-ttu-id="0bc9b-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0bc9b-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="0bc9b-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="0bc9b-118">-Credential</span></span>
<span data-ttu-id="0bc9b-119">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="0bc9b-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0bc9b-121">-Description</span></span>
<span data-ttu-id="0bc9b-122">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-122">Backend Description.</span></span>
<span data-ttu-id="0bc9b-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0bc9b-124">-Protocol</span></span>
<span data-ttu-id="0bc9b-125">Backend-kommunikations protokoll.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-125">Backend Communication protocol.</span></span>
<span data-ttu-id="0bc9b-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-126">This parameter is required.</span></span>
<span data-ttu-id="0bc9b-127">Giltiga värden är "http" och "SOAP".</span><span class="sxs-lookup"><span data-stu-id="0bc9b-127">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="0bc9b-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="0bc9b-128">-Proxy</span></span>
<span data-ttu-id="0bc9b-129">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="0bc9b-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc9b-131">-ResourceId</span></span>
<span data-ttu-id="0bc9b-132">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="0bc9b-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-133">This parameter is optional.</span></span>
<span data-ttu-id="0bc9b-134">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="0bc9b-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="0bc9b-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="0bc9b-136">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="0bc9b-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="0bc9b-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="0bc9b-139">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="0bc9b-140">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-141">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="0bc9b-141">-Title</span></span>
<span data-ttu-id="0bc9b-142">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-142">Backend Title.</span></span>
<span data-ttu-id="0bc9b-143">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bc9b-144">-URL</span><span class="sxs-lookup"><span data-stu-id="0bc9b-144">-Url</span></span>
<span data-ttu-id="0bc9b-145">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="0bc9b-146">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-146">This parameter is required.</span></span>

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

### <span data-ttu-id="0bc9b-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bc9b-147">-Confirm</span></span>
<span data-ttu-id="0bc9b-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc9b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc9b-149">-WhatIf</span></span>
<span data-ttu-id="0bc9b-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bc9b-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc9b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc9b-152">-DefaultProfile</span></span>
<span data-ttu-id="0bc9b-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bc9b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc9b-154">CommonParameters</span></span>
<span data-ttu-id="0bc9b-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc9b-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc9b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc9b-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bc9b-157">INPUTS</span></span>

## <span data-ttu-id="0bc9b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bc9b-158">OUTPUTS</span></span>

### <span data-ttu-id="0bc9b-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0bc9b-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0bc9b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bc9b-160">NOTES</span></span>

## <span data-ttu-id="0bc9b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bc9b-161">RELATED LINKS</span></span>

[<span data-ttu-id="0bc9b-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0bc9b-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="0bc9b-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0bc9b-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="0bc9b-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0bc9b-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="0bc9b-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0bc9b-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0bc9b-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0bc9b-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

