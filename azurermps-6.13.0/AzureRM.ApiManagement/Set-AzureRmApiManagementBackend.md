---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573039"
---
# <span data-ttu-id="fff41-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fff41-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="fff41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fff41-102">SYNOPSIS</span></span>
<span data-ttu-id="fff41-103">Uppdaterar en server del.</span><span class="sxs-lookup"><span data-stu-id="fff41-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fff41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fff41-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fff41-105">DESCRIPTION</span></span>
<span data-ttu-id="fff41-106">Uppdaterar en befintlig server del i API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="fff41-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="fff41-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fff41-107">EXAMPLES</span></span>

### <span data-ttu-id="fff41-108">Uppdaterar beskrivningen av Server delen 123</span><span class="sxs-lookup"><span data-stu-id="fff41-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="fff41-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fff41-109">PARAMETERS</span></span>

### <span data-ttu-id="fff41-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="fff41-110">-BackendId</span></span>
<span data-ttu-id="fff41-111">Identifierare för ny server.</span><span class="sxs-lookup"><span data-stu-id="fff41-111">Identifier of new backend.</span></span>
<span data-ttu-id="fff41-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fff41-112">This parameter is required.</span></span>

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

### <span data-ttu-id="fff41-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fff41-113">-Context</span></span>
<span data-ttu-id="fff41-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fff41-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fff41-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fff41-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fff41-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="fff41-116">-Credential</span></span>
<span data-ttu-id="fff41-117">Autentiseringsuppgifter som ska användas när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="fff41-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff41-119">-DefaultProfile</span></span>
<span data-ttu-id="fff41-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fff41-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff41-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fff41-121">-Description</span></span>
<span data-ttu-id="fff41-122">Server delens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="fff41-122">Backend Description.</span></span>
<span data-ttu-id="fff41-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fff41-124">-PassThru</span></span>
<span data-ttu-id="fff41-125">Anger att denna cmdlet returnerar  **PsApiManagementBackend** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="fff41-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fff41-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fff41-126">-Protocol</span></span>
<span data-ttu-id="fff41-127">Backend Communication Protocol (http eller SOAP).</span><span class="sxs-lookup"><span data-stu-id="fff41-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="fff41-128">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="fff41-128">This parameter is optional</span></span>

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

### <span data-ttu-id="fff41-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="fff41-129">-Proxy</span></span>
<span data-ttu-id="fff41-130">Information om proxyserver för användning när du skickar begäran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="fff41-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff41-132">-ResourceId</span></span>
<span data-ttu-id="fff41-133">Hanterings-URI för resursen i det externa systemet.</span><span class="sxs-lookup"><span data-stu-id="fff41-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="fff41-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-134">This parameter is optional.</span></span>
<span data-ttu-id="fff41-135">URL-adressen kan vara resurs-ID för logiska appar, Function-appar eller API-appar.</span><span class="sxs-lookup"><span data-stu-id="fff41-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="fff41-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fff41-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="fff41-137">Information om tjänstens infrastruktur Server.</span><span class="sxs-lookup"><span data-stu-id="fff41-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="fff41-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="fff41-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="fff41-140">Om du vill hoppa över verifiering av certifikat kedjan när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="fff41-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="fff41-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="fff41-143">Om du vill hoppa över verifiering av certifikat namn när du pratar med Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="fff41-144">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-145">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="fff41-145">-Title</span></span>
<span data-ttu-id="fff41-146">Rubrik på Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-146">Backend Title.</span></span>
<span data-ttu-id="fff41-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-148">-URL</span><span class="sxs-lookup"><span data-stu-id="fff41-148">-Url</span></span>
<span data-ttu-id="fff41-149">Runtime-URL för Server delen.</span><span class="sxs-lookup"><span data-stu-id="fff41-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="fff41-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fff41-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="fff41-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fff41-151">-Confirm</span></span>
<span data-ttu-id="fff41-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fff41-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff41-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff41-153">-WhatIf</span></span>
<span data-ttu-id="fff41-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fff41-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fff41-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fff41-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff41-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff41-156">CommonParameters</span></span>
<span data-ttu-id="fff41-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff41-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff41-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fff41-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff41-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fff41-159">INPUTS</span></span>

### <span data-ttu-id="fff41-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fff41-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fff41-161">System. String</span><span class="sxs-lookup"><span data-stu-id="fff41-161">System.String</span></span>

### <span data-ttu-id="fff41-162">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fff41-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fff41-163">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fff41-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="fff41-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fff41-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="fff41-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fff41-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="fff41-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fff41-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fff41-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fff41-167">OUTPUTS</span></span>

### <span data-ttu-id="fff41-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fff41-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="fff41-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fff41-169">NOTES</span></span>

## <span data-ttu-id="fff41-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fff41-170">RELATED LINKS</span></span>

[<span data-ttu-id="fff41-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fff41-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="fff41-172">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fff41-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="fff41-173">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fff41-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="fff41-174">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fff41-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="fff41-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fff41-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
