---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757509"
---
# <span data-ttu-id="fa10f-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa10f-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="fa10f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa10f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa10f-103">Uppdaterar en server del.</span><span class="sxs-lookup"><span data-stu-id="fa10f-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa10f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa10f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa10f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa10f-105">DESCRIPTION</span></span>
<span data-ttu-id="fa10f-106">Uppdaterar en befintlig server del i API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="fa10f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa10f-107">EXAMPLES</span></span>

### <span data-ttu-id="fa10f-108">Uppdaterar beskrivningen av Server delen 123</span><span class="sxs-lookup"><span data-stu-id="fa10f-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="fa10f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa10f-109">PARAMETERS</span></span>

### <span data-ttu-id="fa10f-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="fa10f-110">-BackendId</span></span>
<span data-ttu-id="fa10f-111">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="fa10f-111">Identifier of new backend.</span></span>
<span data-ttu-id="fa10f-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fa10f-112">This parameter is required.</span></span>

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

### <span data-ttu-id="fa10f-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fa10f-113">-Context</span></span>
<span data-ttu-id="fa10f-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fa10f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fa10f-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fa10f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fa10f-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="fa10f-116">-Credential</span></span>
<span data-ttu-id="fa10f-117">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="fa10f-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fa10f-119">-Description</span></span>
<span data-ttu-id="fa10f-120">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="fa10f-120">Backend Description.</span></span>
<span data-ttu-id="fa10f-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa10f-122">-PassThru</span></span>
<span data-ttu-id="fa10f-123">Anger att denna cmdlet returnerar  **PsApiManagementBackend** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="fa10f-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa10f-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fa10f-124">-Protocol</span></span>
<span data-ttu-id="fa10f-125">Backend Communication Protocol (http eller SOAP).</span><span class="sxs-lookup"><span data-stu-id="fa10f-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="fa10f-126">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="fa10f-126">This parameter is optional</span></span>

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

### <span data-ttu-id="fa10f-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="fa10f-127">-Proxy</span></span>
<span data-ttu-id="fa10f-128">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="fa10f-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa10f-130">-ResourceId</span></span>
<span data-ttu-id="fa10f-131">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="fa10f-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="fa10f-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-132">This parameter is optional.</span></span>
<span data-ttu-id="fa10f-133">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="fa10f-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="fa10f-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="fa10f-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="fa10f-135">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="fa10f-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="fa10f-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="fa10f-138">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="fa10f-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-140">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="fa10f-140">-Title</span></span>
<span data-ttu-id="fa10f-141">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-141">Backend Title.</span></span>
<span data-ttu-id="fa10f-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-143">-URL</span><span class="sxs-lookup"><span data-stu-id="fa10f-143">-Url</span></span>
<span data-ttu-id="fa10f-144">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="fa10f-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="fa10f-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa10f-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa10f-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa10f-146">-Confirm</span></span>
<span data-ttu-id="fa10f-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa10f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa10f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa10f-148">-WhatIf</span></span>
<span data-ttu-id="fa10f-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa10f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa10f-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa10f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa10f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa10f-151">-DefaultProfile</span></span>
<span data-ttu-id="fa10f-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa10f-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa10f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa10f-153">CommonParameters</span></span>
<span data-ttu-id="fa10f-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa10f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa10f-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa10f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa10f-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa10f-156">INPUTS</span></span>

## <span data-ttu-id="fa10f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa10f-157">OUTPUTS</span></span>

### <span data-ttu-id="fa10f-158">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa10f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="fa10f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa10f-159">NOTES</span></span>

## <span data-ttu-id="fa10f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa10f-160">RELATED LINKS</span></span>

[<span data-ttu-id="fa10f-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa10f-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="fa10f-162">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa10f-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="fa10f-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fa10f-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="fa10f-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fa10f-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="fa10f-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa10f-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
