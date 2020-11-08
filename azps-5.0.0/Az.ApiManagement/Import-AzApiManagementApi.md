---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269692"
---
# <span data-ttu-id="2f62f-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="2f62f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f62f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f62f-103">Importerar ett API från en fil eller webb adress.</span><span class="sxs-lookup"><span data-stu-id="2f62f-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="2f62f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f62f-104">SYNTAX</span></span>

### <span data-ttu-id="2f62f-105">ImportFromLocalFile (standard)</span><span class="sxs-lookup"><span data-stu-id="2f62f-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f62f-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="2f62f-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f62f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f62f-107">DESCRIPTION</span></span>
<span data-ttu-id="2f62f-108">Cmdleten **import-AzApiManagementApi** importerar ett API för Azure API-hantering från en fil eller en URL-adress (Web Application Description Language), WSDL-eller Swagger-format.</span><span class="sxs-lookup"><span data-stu-id="2f62f-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="2f62f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f62f-109">EXAMPLES</span></span>

### <span data-ttu-id="2f62f-110">Exempel 1: importera ett API från en WADL-fil</span><span class="sxs-lookup"><span data-stu-id="2f62f-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="2f62f-111">Det här kommandot importerar ett API från den angivna WADL-filen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="2f62f-112">Exempel 2: importera ett API från en Swagger-fil</span><span class="sxs-lookup"><span data-stu-id="2f62f-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="2f62f-113">Det här kommandot importerar ett API från den angivna Swagger-filen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="2f62f-114">Exempel 3: importera ett API från en WADL-länk</span><span class="sxs-lookup"><span data-stu-id="2f62f-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="2f62f-115">Det här kommandot importerar ett API från den angivna WADL-länken.</span><span class="sxs-lookup"><span data-stu-id="2f62f-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="2f62f-116">Exempel 4: importera ett API från en öppen API-länk</span><span class="sxs-lookup"><span data-stu-id="2f62f-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="2f62f-117">Det här kommandot importerar ett API från den angivna länken för Open 3,0-specifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="2f62f-118">Exempel 5: importera ett API från en öppen API-länk till en ApiVersion-uppsättning</span><span class="sxs-lookup"><span data-stu-id="2f62f-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="2f62f-119">Det här kommandot importerar ett API från det angivna Open 3,0 Specification-dokumentet och skapar ett nytt ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="2f62f-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="2f62f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f62f-120">PARAMETERS</span></span>

### <span data-ttu-id="2f62f-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f62f-121">-ApiId</span></span>
<span data-ttu-id="2f62f-122">Anger ID för det API som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="2f62f-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="2f62f-123">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="2f62f-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="2f62f-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2f62f-124">-ApiRevision</span></span>
<span data-ttu-id="2f62f-125">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="2f62f-125">Identifier of API Revision.</span></span> <span data-ttu-id="2f62f-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2f62f-126">This parameter is optional.</span></span> <span data-ttu-id="2f62f-127">Om det inte anges görs importen till den aktuella aktiva versionen eller ett nytt API.</span><span class="sxs-lookup"><span data-stu-id="2f62f-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="2f62f-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="2f62f-128">-ApiType</span></span>
<span data-ttu-id="2f62f-129">Den här parametern är valfri med standardvärdet för http.</span><span class="sxs-lookup"><span data-stu-id="2f62f-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="2f62f-130">SOAP-alternativet är endast tillämpligt när WSDL importeras och skapar ett SOAP passthrough API.</span><span class="sxs-lookup"><span data-stu-id="2f62f-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f62f-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f62f-131">-ApiVersion</span></span>
<span data-ttu-id="2f62f-132">API-version av API för att skapa.</span><span class="sxs-lookup"><span data-stu-id="2f62f-132">Api Version of the Api to create.</span></span> <span data-ttu-id="2f62f-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2f62f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f62f-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2f62f-134">-ApiVersionSetId</span></span>
<span data-ttu-id="2f62f-135">En resurs-ID för den relaterade API-versionen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="2f62f-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2f62f-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f62f-137">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2f62f-137">-Context</span></span>
<span data-ttu-id="2f62f-138">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2f62f-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2f62f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f62f-139">-DefaultProfile</span></span>
<span data-ttu-id="2f62f-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f62f-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f62f-141">-Path</span><span class="sxs-lookup"><span data-stu-id="2f62f-141">-Path</span></span>
<span data-ttu-id="2f62f-142">Anger en Web API-sökväg som den sista delen av API: s offentliga webb adress.</span><span class="sxs-lookup"><span data-stu-id="2f62f-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="2f62f-143">Denna URL används av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2f62f-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="2f62f-144">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="2f62f-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="2f62f-145">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2f62f-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f62f-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2f62f-146">-Protocol</span></span>
<span data-ttu-id="2f62f-147">Webb-API-protokoll (http, https).</span><span class="sxs-lookup"><span data-stu-id="2f62f-147">Web API protocols (http, https).</span></span> <span data-ttu-id="2f62f-148">Protokoll som finns tillgängliga för API.</span><span class="sxs-lookup"><span data-stu-id="2f62f-148">Protocols over which API is made available.</span></span> <span data-ttu-id="2f62f-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2f62f-149">This parameter is optional.</span></span> <span data-ttu-id="2f62f-150">Om den anges åsidosätts de protokoll som anges i förfrågnings dokumentet.</span><span class="sxs-lookup"><span data-stu-id="2f62f-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f62f-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2f62f-151">-ServiceUrl</span></span>
<span data-ttu-id="2f62f-152">En URL för webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="2f62f-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="2f62f-153">Denna URL kommer endast att användas av Azure API Management och blir inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="2f62f-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="2f62f-154">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2f62f-154">This parameter is optional.</span></span> <span data-ttu-id="2f62f-155">Om den anges åsidosätter den ServiceUrl som anges i förfrågnings dokumentet.</span><span class="sxs-lookup"><span data-stu-id="2f62f-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="2f62f-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="2f62f-156">-SpecificationFormat</span></span>
<span data-ttu-id="2f62f-157">Anger Specifikations format.</span><span class="sxs-lookup"><span data-stu-id="2f62f-157">Specifies the specification format.</span></span>
<span data-ttu-id="2f62f-158">psdx_paramvalues Wadl, WSDL och swagger.</span><span class="sxs-lookup"><span data-stu-id="2f62f-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f62f-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="2f62f-159">-SpecificationPath</span></span>
<span data-ttu-id="2f62f-160">Anger sökvägen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f62f-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="2f62f-161">-SpecificationUrl</span></span>
<span data-ttu-id="2f62f-162">Anger URL-adressen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f62f-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f62f-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f62f-163">-WsdlEndpointName</span></span>
<span data-ttu-id="2f62f-164">Det lokala namnet på den WSDL-slutpunkt (port) som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="2f62f-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="2f62f-165">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="2f62f-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="2f62f-166">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="2f62f-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="2f62f-167">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="2f62f-167">Default value is $null.</span></span>

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

### <span data-ttu-id="2f62f-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="2f62f-168">-WsdlServiceName</span></span>
<span data-ttu-id="2f62f-169">Det lokala namnet på WSDL-tjänsten som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="2f62f-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="2f62f-170">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="2f62f-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="2f62f-171">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="2f62f-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="2f62f-172">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="2f62f-172">Default value is $null.</span></span>

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

### <span data-ttu-id="2f62f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f62f-173">CommonParameters</span></span>
<span data-ttu-id="2f62f-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f62f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f62f-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f62f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f62f-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f62f-176">INPUTS</span></span>

### <span data-ttu-id="2f62f-177">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f62f-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f62f-178">System. String</span><span class="sxs-lookup"><span data-stu-id="2f62f-178">System.String</span></span>

### <span data-ttu-id="2f62f-179">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="2f62f-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="2f62f-180">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2f62f-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2f62f-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f62f-181">OUTPUTS</span></span>

### <span data-ttu-id="2f62f-182">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2f62f-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f62f-183">NOTES</span></span>

## <span data-ttu-id="2f62f-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f62f-184">RELATED LINKS</span></span>

[<span data-ttu-id="2f62f-185">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2f62f-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2f62f-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2f62f-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="2f62f-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f62f-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


