---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585219"
---
# <span data-ttu-id="3ade8-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ade8-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="3ade8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ade8-102">SYNOPSIS</span></span>
<span data-ttu-id="3ade8-103">Skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="3ade8-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ade8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ade8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ade8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ade8-105">DESCRIPTION</span></span>
<span data-ttu-id="3ade8-106">Skapar en ny backend-enhet i API-hantering.</span><span class="sxs-lookup"><span data-stu-id="3ade8-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="3ade8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ade8-107">EXAMPLES</span></span>

### <span data-ttu-id="3ade8-108">Skapa en server del 123 med ett grundläggande Authorization-schema</span><span class="sxs-lookup"><span data-stu-id="3ade8-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="3ade8-109">Skapar en ny server del</span><span class="sxs-lookup"><span data-stu-id="3ade8-109">Creates a new Backend</span></span>

## <span data-ttu-id="3ade8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ade8-110">PARAMETERS</span></span>

### <span data-ttu-id="3ade8-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="3ade8-111">-BackendId</span></span>
<span data-ttu-id="3ade8-112">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="3ade8-112">Identifier of new backend.</span></span>
<span data-ttu-id="3ade8-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-113">This parameter is optional.</span></span>
<span data-ttu-id="3ade8-114">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="3ade8-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3ade8-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3ade8-115">-Context</span></span>
<span data-ttu-id="3ade8-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3ade8-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ade8-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3ade8-117">This parameter is required.</span></span>

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

### <span data-ttu-id="3ade8-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="3ade8-118">-Credential</span></span>
<span data-ttu-id="3ade8-119">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="3ade8-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ade8-121">-DefaultProfile</span></span>
<span data-ttu-id="3ade8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ade8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3ade8-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3ade8-123">-Description</span></span>
<span data-ttu-id="3ade8-124">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="3ade8-124">Backend Description.</span></span>
<span data-ttu-id="3ade8-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3ade8-126">-Protocol</span></span>
<span data-ttu-id="3ade8-127">Backend-kommunikations protokoll.</span><span class="sxs-lookup"><span data-stu-id="3ade8-127">Backend Communication protocol.</span></span>
<span data-ttu-id="3ade8-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3ade8-128">This parameter is required.</span></span>
<span data-ttu-id="3ade8-129">Giltiga värden är "http" och "SOAP".</span><span class="sxs-lookup"><span data-stu-id="3ade8-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ade8-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="3ade8-130">-Proxy</span></span>
<span data-ttu-id="3ade8-131">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="3ade8-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ade8-133">-ResourceId</span></span>
<span data-ttu-id="3ade8-134">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="3ade8-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="3ade8-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-135">This parameter is optional.</span></span>
<span data-ttu-id="3ade8-136">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="3ade8-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="3ade8-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="3ade8-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="3ade8-138">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="3ade8-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="3ade8-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="3ade8-141">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="3ade8-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-143">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="3ade8-143">-Title</span></span>
<span data-ttu-id="3ade8-144">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-144">Backend Title.</span></span>
<span data-ttu-id="3ade8-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3ade8-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ade8-146">-URL</span><span class="sxs-lookup"><span data-stu-id="3ade8-146">-Url</span></span>
<span data-ttu-id="3ade8-147">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="3ade8-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="3ade8-148">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3ade8-148">This parameter is required.</span></span>

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

### <span data-ttu-id="3ade8-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ade8-149">-Confirm</span></span>
<span data-ttu-id="3ade8-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ade8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ade8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ade8-151">-WhatIf</span></span>
<span data-ttu-id="3ade8-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ade8-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ade8-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ade8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ade8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ade8-154">CommonParameters</span></span>
<span data-ttu-id="3ade8-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ade8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ade8-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ade8-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ade8-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ade8-157">INPUTS</span></span>

### <span data-ttu-id="3ade8-158">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ade8-158">None</span></span>
<span data-ttu-id="3ade8-159">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3ade8-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ade8-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ade8-160">OUTPUTS</span></span>

### <span data-ttu-id="3ade8-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ade8-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="3ade8-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ade8-162">NOTES</span></span>

## <span data-ttu-id="3ade8-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ade8-163">RELATED LINKS</span></span>

[<span data-ttu-id="3ade8-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ade8-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="3ade8-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3ade8-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="3ade8-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3ade8-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="3ade8-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ade8-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3ade8-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ade8-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

