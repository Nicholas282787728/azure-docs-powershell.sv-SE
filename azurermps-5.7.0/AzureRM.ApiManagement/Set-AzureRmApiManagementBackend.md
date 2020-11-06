---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577279"
---
# <span data-ttu-id="a24b0-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a24b0-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a24b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a24b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a24b0-103">Uppdaterar en server del.</span><span class="sxs-lookup"><span data-stu-id="a24b0-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a24b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a24b0-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a24b0-105">DESCRIPTION</span></span>
<span data-ttu-id="a24b0-106">Uppdaterar en befintlig server del i API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="a24b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a24b0-107">EXAMPLES</span></span>

### <span data-ttu-id="a24b0-108">Uppdaterar beskrivningen av Server delen 123</span><span class="sxs-lookup"><span data-stu-id="a24b0-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="a24b0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a24b0-109">PARAMETERS</span></span>

### <span data-ttu-id="a24b0-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="a24b0-110">-BackendId</span></span>
<span data-ttu-id="a24b0-111">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="a24b0-111">Identifier of new backend.</span></span>
<span data-ttu-id="a24b0-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a24b0-112">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a24b0-113">-Context</span></span>
<span data-ttu-id="a24b0-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a24b0-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a24b0-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a24b0-115">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a24b0-116">-Credential</span></span>
<span data-ttu-id="a24b0-117">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="a24b0-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24b0-119">-DefaultProfile</span></span>
<span data-ttu-id="a24b0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a24b0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a24b0-121">-Description</span></span>
<span data-ttu-id="a24b0-122">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="a24b0-122">Backend Description.</span></span>
<span data-ttu-id="a24b0-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-123">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a24b0-124">-PassThru</span></span>
<span data-ttu-id="a24b0-125">Anger att denna cmdlet returnerar  **PsApiManagementBackend** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a24b0-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a24b0-126">-Protocol</span></span>
<span data-ttu-id="a24b0-127">Backend Communication Protocol (http eller SOAP).</span><span class="sxs-lookup"><span data-stu-id="a24b0-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="a24b0-128">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="a24b0-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="a24b0-129">-Proxy</span></span>
<span data-ttu-id="a24b0-130">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="a24b0-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a24b0-132">-ResourceId</span></span>
<span data-ttu-id="a24b0-133">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="a24b0-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="a24b0-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-134">This parameter is optional.</span></span>
<span data-ttu-id="a24b0-135">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="a24b0-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="a24b0-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="a24b0-137">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="a24b0-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="a24b0-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="a24b0-140">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="a24b0-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-142">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="a24b0-142">-Title</span></span>
<span data-ttu-id="a24b0-143">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-143">Backend Title.</span></span>
<span data-ttu-id="a24b0-144">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-144">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-145">-URL</span><span class="sxs-lookup"><span data-stu-id="a24b0-145">-Url</span></span>
<span data-ttu-id="a24b0-146">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="a24b0-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="a24b0-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="a24b0-147">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a24b0-148">-Confirm</span></span>
<span data-ttu-id="a24b0-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a24b0-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24b0-150">-WhatIf</span></span>
<span data-ttu-id="a24b0-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a24b0-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a24b0-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a24b0-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24b0-153">CommonParameters</span></span>
<span data-ttu-id="a24b0-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24b0-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24b0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24b0-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a24b0-156">INPUTS</span></span>

### <span data-ttu-id="a24b0-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="a24b0-157">None</span></span>
<span data-ttu-id="a24b0-158">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a24b0-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a24b0-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a24b0-159">OUTPUTS</span></span>

### <span data-ttu-id="a24b0-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a24b0-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a24b0-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a24b0-161">NOTES</span></span>

## <span data-ttu-id="a24b0-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a24b0-162">RELATED LINKS</span></span>

[<span data-ttu-id="a24b0-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a24b0-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a24b0-164">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a24b0-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a24b0-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a24b0-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a24b0-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a24b0-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a24b0-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a24b0-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
