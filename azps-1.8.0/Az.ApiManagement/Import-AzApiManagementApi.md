---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743384"
---
# <span data-ttu-id="68006-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="68006-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68006-102">SYNOPSIS</span></span>
<span data-ttu-id="68006-103">Importerar ett API från en fil eller webb adress.</span><span class="sxs-lookup"><span data-stu-id="68006-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="68006-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68006-104">SYNTAX</span></span>

### <span data-ttu-id="68006-105">ImportFromLocalFile (standard)</span><span class="sxs-lookup"><span data-stu-id="68006-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68006-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="68006-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68006-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68006-107">DESCRIPTION</span></span>
<span data-ttu-id="68006-108">Cmdleten **import-AzApiManagementApi** importerar ett API för Azure API-hantering från en fil eller en URL-adress (Web Application Description Language), WSDL-eller Swagger-format.</span><span class="sxs-lookup"><span data-stu-id="68006-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="68006-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68006-109">EXAMPLES</span></span>

### <span data-ttu-id="68006-110">Exempel 1 importera ett API från en WADL-fil</span><span class="sxs-lookup"><span data-stu-id="68006-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="68006-111">Det här kommandot importerar ett API från den angivna WADL-filen.</span><span class="sxs-lookup"><span data-stu-id="68006-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="68006-112">Exempel 2 importera ett API från en Swagger-fil</span><span class="sxs-lookup"><span data-stu-id="68006-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="68006-113">Det här kommandot importerar ett API från den angivna Swagger-filen.</span><span class="sxs-lookup"><span data-stu-id="68006-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="68006-114">Exempel 3: importera ett API från en WADL-länk</span><span class="sxs-lookup"><span data-stu-id="68006-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="68006-115">Det här kommandot importerar ett API från den angivna WADL-länken.</span><span class="sxs-lookup"><span data-stu-id="68006-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="68006-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68006-116">PARAMETERS</span></span>

### <span data-ttu-id="68006-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68006-117">-ApiId</span></span>
<span data-ttu-id="68006-118">Anger ID för det API som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="68006-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="68006-119">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="68006-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="68006-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="68006-120">-ApiRevision</span></span>
<span data-ttu-id="68006-121">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="68006-121">Identifier of API Revision.</span></span> <span data-ttu-id="68006-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="68006-122">This parameter is optional.</span></span> <span data-ttu-id="68006-123">Om det inte anges görs importen till den aktuella aktiva versionen eller ett nytt API.</span><span class="sxs-lookup"><span data-stu-id="68006-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="68006-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="68006-124">-ApiType</span></span>
<span data-ttu-id="68006-125">Den här parametern är valfri med standardvärdet för http.</span><span class="sxs-lookup"><span data-stu-id="68006-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="68006-126">SOAP-alternativet är endast tillämpligt när WSDL importeras och skapar ett SOAP passthrough API.</span><span class="sxs-lookup"><span data-stu-id="68006-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="68006-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="68006-127">-Context</span></span>
<span data-ttu-id="68006-128">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="68006-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68006-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68006-129">-DefaultProfile</span></span>
<span data-ttu-id="68006-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68006-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68006-131">-Path</span><span class="sxs-lookup"><span data-stu-id="68006-131">-Path</span></span>
<span data-ttu-id="68006-132">Anger en Web API-sökväg som den sista delen av API: s offentliga webb adress.</span><span class="sxs-lookup"><span data-stu-id="68006-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="68006-133">Denna URL används av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="68006-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="68006-134">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="68006-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="68006-135">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="68006-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="68006-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="68006-136">-SpecificationFormat</span></span>
<span data-ttu-id="68006-137">Anger Specifikations format.</span><span class="sxs-lookup"><span data-stu-id="68006-137">Specifies the specification format.</span></span>
<span data-ttu-id="68006-138">psdx_paramvalues Wadl, WSDL och swagger.</span><span class="sxs-lookup"><span data-stu-id="68006-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68006-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="68006-139">-SpecificationPath</span></span>
<span data-ttu-id="68006-140">Anger sökvägen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="68006-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="68006-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="68006-141">-SpecificationUrl</span></span>
<span data-ttu-id="68006-142">Anger URL-adressen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="68006-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="68006-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="68006-143">-WsdlEndpointName</span></span>
<span data-ttu-id="68006-144">Det lokala namnet på den WSDL-slutpunkt (port) som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="68006-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="68006-145">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="68006-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="68006-146">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="68006-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="68006-147">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="68006-147">Default value is $null.</span></span>

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

### <span data-ttu-id="68006-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="68006-148">-WsdlServiceName</span></span>
<span data-ttu-id="68006-149">Det lokala namnet på WSDL-tjänsten som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="68006-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="68006-150">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="68006-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="68006-151">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="68006-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="68006-152">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="68006-152">Default value is $null.</span></span>

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

### <span data-ttu-id="68006-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68006-153">CommonParameters</span></span>
<span data-ttu-id="68006-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68006-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68006-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68006-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68006-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68006-156">INPUTS</span></span>

### <span data-ttu-id="68006-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68006-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68006-158">System. String</span><span class="sxs-lookup"><span data-stu-id="68006-158">System.String</span></span>

### <span data-ttu-id="68006-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="68006-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="68006-160">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="68006-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="68006-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68006-161">OUTPUTS</span></span>

### <span data-ttu-id="68006-162">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="68006-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68006-163">NOTES</span></span>

## <span data-ttu-id="68006-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68006-164">RELATED LINKS</span></span>

[<span data-ttu-id="68006-165">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="68006-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="68006-167">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="68006-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="68006-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68006-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


