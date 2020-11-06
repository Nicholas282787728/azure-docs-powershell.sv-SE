---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 7eb2e25f137abb303e1c9fa5b4ebe8b932346871
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576353"
---
# <span data-ttu-id="e7d87-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="e7d87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7d87-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d87-103">Importerar ett API från en fil eller webb adress.</span><span class="sxs-lookup"><span data-stu-id="e7d87-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7d87-104">SYNTAX</span></span>

### <span data-ttu-id="e7d87-105">ImportFromLocalFile (standard)</span><span class="sxs-lookup"><span data-stu-id="e7d87-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7d87-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="e7d87-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7d87-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7d87-107">DESCRIPTION</span></span>
<span data-ttu-id="e7d87-108">Cmdleten **import-AzureRmApiManagementApi** importerar ett API för Azure API-hantering från en fil eller en URL-adress (Web Application Description Language), WSDL-eller Swagger-format.</span><span class="sxs-lookup"><span data-stu-id="e7d87-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="e7d87-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7d87-109">EXAMPLES</span></span>

### <span data-ttu-id="e7d87-110">Exempel 1 importera ett API från en WADL-fil</span><span class="sxs-lookup"><span data-stu-id="e7d87-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="e7d87-111">Det här kommandot importerar ett API från den angivna WADL-filen.</span><span class="sxs-lookup"><span data-stu-id="e7d87-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="e7d87-112">Exempel 2 importera ett API från en Swagger-fil</span><span class="sxs-lookup"><span data-stu-id="e7d87-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="e7d87-113">Det här kommandot importerar ett API från den angivna Swagger-filen.</span><span class="sxs-lookup"><span data-stu-id="e7d87-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="e7d87-114">Exempel 3: importera ett API från en WADL-länk</span><span class="sxs-lookup"><span data-stu-id="e7d87-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="e7d87-115">Det här kommandot importerar ett API från den angivna WADL-länken.</span><span class="sxs-lookup"><span data-stu-id="e7d87-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="e7d87-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7d87-116">PARAMETERS</span></span>

### <span data-ttu-id="e7d87-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e7d87-117">-ApiId</span></span>
<span data-ttu-id="e7d87-118">Anger ID för det API som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="e7d87-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="e7d87-119">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="e7d87-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="e7d87-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e7d87-120">-ApiRevision</span></span>
<span data-ttu-id="e7d87-121">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="e7d87-121">Identifier of API Revision.</span></span> <span data-ttu-id="e7d87-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e7d87-122">This parameter is optional.</span></span> <span data-ttu-id="e7d87-123">Om det inte anges görs importen till den aktuella aktiva versionen eller ett nytt API.</span><span class="sxs-lookup"><span data-stu-id="e7d87-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="e7d87-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="e7d87-124">-ApiType</span></span>
<span data-ttu-id="e7d87-125">Den här parametern är valfri med standardvärdet för http.</span><span class="sxs-lookup"><span data-stu-id="e7d87-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="e7d87-126">SOAP-alternativet är endast tillämpligt när WSDL importeras och skapar ett SOAP passthrough API.</span><span class="sxs-lookup"><span data-stu-id="e7d87-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="e7d87-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e7d87-127">-Context</span></span>
<span data-ttu-id="e7d87-128">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e7d87-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e7d87-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d87-129">-DefaultProfile</span></span>
<span data-ttu-id="e7d87-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d87-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d87-131">-Path</span><span class="sxs-lookup"><span data-stu-id="e7d87-131">-Path</span></span>
<span data-ttu-id="e7d87-132">Anger en Web API-sökväg som den sista delen av API: s offentliga webb adress.</span><span class="sxs-lookup"><span data-stu-id="e7d87-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="e7d87-133">Denna URL används av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e7d87-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="e7d87-134">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="e7d87-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="e7d87-135">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="e7d87-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="e7d87-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="e7d87-136">-SpecificationFormat</span></span>
<span data-ttu-id="e7d87-137">Anger Specifikations format.</span><span class="sxs-lookup"><span data-stu-id="e7d87-137">Specifies the specification format.</span></span>
<span data-ttu-id="e7d87-138">psdx_paramvalues Wadl, WSDL och swagger.</span><span class="sxs-lookup"><span data-stu-id="e7d87-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="e7d87-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="e7d87-139">-SpecificationPath</span></span>
<span data-ttu-id="e7d87-140">Anger sökvägen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="e7d87-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="e7d87-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="e7d87-141">-SpecificationUrl</span></span>
<span data-ttu-id="e7d87-142">Anger URL-adressen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="e7d87-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="e7d87-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="e7d87-143">-WsdlEndpointName</span></span>
<span data-ttu-id="e7d87-144">Det lokala namnet på den WSDL-slutpunkt (port) som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="e7d87-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="e7d87-145">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="e7d87-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="e7d87-146">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="e7d87-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="e7d87-147">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="e7d87-147">Default value is $null.</span></span>

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

### <span data-ttu-id="e7d87-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="e7d87-148">-WsdlServiceName</span></span>
<span data-ttu-id="e7d87-149">Det lokala namnet på WSDL-tjänsten som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="e7d87-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="e7d87-150">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="e7d87-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="e7d87-151">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="e7d87-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="e7d87-152">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="e7d87-152">Default value is $null.</span></span>

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

### <span data-ttu-id="e7d87-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d87-153">CommonParameters</span></span>
<span data-ttu-id="e7d87-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d87-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d87-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d87-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d87-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7d87-156">INPUTS</span></span>

### <span data-ttu-id="e7d87-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e7d87-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e7d87-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e7d87-158">System.String</span></span>

### <span data-ttu-id="e7d87-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="e7d87-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="e7d87-160">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e7d87-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e7d87-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7d87-161">OUTPUTS</span></span>

### <span data-ttu-id="e7d87-162">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e7d87-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7d87-163">NOTES</span></span>

## <span data-ttu-id="e7d87-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7d87-164">RELATED LINKS</span></span>

[<span data-ttu-id="e7d87-165">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-165">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="e7d87-166">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-166">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="e7d87-167">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-167">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="e7d87-168">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-168">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="e7d87-169">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e7d87-169">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


