---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581808"
---
# <span data-ttu-id="d72c0-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d72c0-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="d72c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d72c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d72c0-103">Ändrar en API-revision</span><span class="sxs-lookup"><span data-stu-id="d72c0-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d72c0-104">SYNTAX</span></span>

### <span data-ttu-id="d72c0-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="d72c0-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72c0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d72c0-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72c0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d72c0-107">DESCRIPTION</span></span>
<span data-ttu-id="d72c0-108">Cmdleten **set-AzureRmApiManagementApiRevision** ändrar en Azure API-revision för API.</span><span class="sxs-lookup"><span data-stu-id="d72c0-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="d72c0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d72c0-109">EXAMPLES</span></span>

### <span data-ttu-id="d72c0-110">Exempel 1 ändra en API-revision</span><span class="sxs-lookup"><span data-stu-id="d72c0-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="d72c0-111">Cmdleten uppdaterar `2` ändringen av API: t `echo-api` med en ny beskrivning, protokoll och sökväg.</span><span class="sxs-lookup"><span data-stu-id="d72c0-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="d72c0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d72c0-112">PARAMETERS</span></span>

### <span data-ttu-id="d72c0-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d72c0-113">-ApiId</span></span>
<span data-ttu-id="d72c0-114">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="d72c0-114">Identifier of existing API.</span></span>
<span data-ttu-id="d72c0-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72c0-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d72c0-116">-ApiRevision</span></span>
<span data-ttu-id="d72c0-117">Identifierare för befintlig API-revision.</span><span class="sxs-lookup"><span data-stu-id="d72c0-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="d72c0-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72c0-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d72c0-119">-AuthorizationScope</span></span>
<span data-ttu-id="d72c0-120">Scope för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d72c0-120">OAuth operations scope.</span></span>
<span data-ttu-id="d72c0-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-121">This parameter is optional.</span></span>
<span data-ttu-id="d72c0-122">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-122">Default value is $null.</span></span>

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

### <span data-ttu-id="d72c0-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="d72c0-123">-AuthorizationServerId</span></span>
<span data-ttu-id="d72c0-124">ID för OAuth-Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="d72c0-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="d72c0-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-125">This parameter is optional.</span></span>
<span data-ttu-id="d72c0-126">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-126">Default value is $null.</span></span>
<span data-ttu-id="d72c0-127">Måste anges om AuthorizationScope har angetts.</span><span class="sxs-lookup"><span data-stu-id="d72c0-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="d72c0-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d72c0-128">-Context</span></span>
<span data-ttu-id="d72c0-129">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d72c0-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d72c0-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-130">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72c0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72c0-131">-DefaultProfile</span></span>
<span data-ttu-id="d72c0-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d72c0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72c0-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d72c0-133">-Description</span></span>
<span data-ttu-id="d72c0-134">Beskrivning av Web API.</span><span class="sxs-lookup"><span data-stu-id="d72c0-134">Web API description.</span></span>
<span data-ttu-id="d72c0-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="d72c0-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d72c0-136">-InputObject</span></span>
<span data-ttu-id="d72c0-137">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="d72c0-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="d72c0-138">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72c0-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="d72c0-139">-Name</span></span>
<span data-ttu-id="d72c0-140">Webb-API-namn.</span><span class="sxs-lookup"><span data-stu-id="d72c0-140">Web API name.</span></span>
<span data-ttu-id="d72c0-141">Det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="d72c0-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="d72c0-142">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-142">This parameter is required.</span></span>

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

### <span data-ttu-id="d72c0-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d72c0-143">-PassThru</span></span>
<span data-ttu-id="d72c0-144">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi typ som representerar set API.</span><span class="sxs-lookup"><span data-stu-id="d72c0-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="d72c0-145">-Path</span><span class="sxs-lookup"><span data-stu-id="d72c0-145">-Path</span></span>
<span data-ttu-id="d72c0-146">Web API Path.</span><span class="sxs-lookup"><span data-stu-id="d72c0-146">Web API Path.</span></span>
<span data-ttu-id="d72c0-147">Sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="d72c0-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="d72c0-148">Denna URL kommer att användas av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d72c0-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="d72c0-149">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="d72c0-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="d72c0-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-150">This parameter is optional.</span></span>
<span data-ttu-id="d72c0-151">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-151">Default value is $null.</span></span>

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

### <span data-ttu-id="d72c0-152">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d72c0-152">-Protocols</span></span>
<span data-ttu-id="d72c0-153">Webb-API-protokoll (http, https).</span><span class="sxs-lookup"><span data-stu-id="d72c0-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="d72c0-154">Protokoll som finns tillgängliga för API.</span><span class="sxs-lookup"><span data-stu-id="d72c0-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="d72c0-155">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-155">This parameter is required.</span></span>
<span data-ttu-id="d72c0-156">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-156">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72c0-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d72c0-157">-ServiceUrl</span></span>
<span data-ttu-id="d72c0-158">En URL för webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="d72c0-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="d72c0-159">Denna URL kommer endast att användas av Azure API Management och blir inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="d72c0-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="d72c0-160">Måste vara 1 till 2000 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="d72c0-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="d72c0-161">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d72c0-161">This parameter is required.</span></span>

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

### <span data-ttu-id="d72c0-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d72c0-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d72c0-163">Rubrik namn för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d72c0-163">Subscription key header name.</span></span>
<span data-ttu-id="d72c0-164">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-164">This parameter is optional.</span></span>
<span data-ttu-id="d72c0-165">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-165">Default value is $null.</span></span>

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

### <span data-ttu-id="d72c0-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d72c0-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d72c0-167">Namn på frågesträng för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="d72c0-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="d72c0-168">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d72c0-168">This parameter is optional.</span></span>
<span data-ttu-id="d72c0-169">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="d72c0-169">Default value is $null.</span></span>

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

### <span data-ttu-id="d72c0-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d72c0-170">-Confirm</span></span>
<span data-ttu-id="d72c0-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d72c0-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72c0-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72c0-172">-WhatIf</span></span>
<span data-ttu-id="d72c0-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d72c0-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72c0-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d72c0-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72c0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72c0-175">CommonParameters</span></span>
<span data-ttu-id="d72c0-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72c0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72c0-177">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72c0-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72c0-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d72c0-178">INPUTS</span></span>

### <span data-ttu-id="d72c0-179">System. String</span><span class="sxs-lookup"><span data-stu-id="d72c0-179">System.String</span></span>

### <span data-ttu-id="d72c0-180">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d72c0-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d72c0-181">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d72c0-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="d72c0-182">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d72c0-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d72c0-183">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="d72c0-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="d72c0-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d72c0-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d72c0-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d72c0-185">OUTPUTS</span></span>

### <span data-ttu-id="d72c0-186">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d72c0-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d72c0-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d72c0-187">NOTES</span></span>

## <span data-ttu-id="d72c0-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d72c0-188">RELATED LINKS</span></span>

[<span data-ttu-id="d72c0-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d72c0-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="d72c0-190">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d72c0-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="d72c0-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d72c0-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
