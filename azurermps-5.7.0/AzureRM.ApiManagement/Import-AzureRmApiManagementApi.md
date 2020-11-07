---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757727"
---
# <span data-ttu-id="174aa-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="174aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="174aa-102">SYNOPSIS</span></span>
<span data-ttu-id="174aa-103">Importerar ett API från en fil eller webb adress.</span><span class="sxs-lookup"><span data-stu-id="174aa-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="174aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="174aa-104">SYNTAX</span></span>

### <span data-ttu-id="174aa-105">ImportFromLocalFile (standard)</span><span class="sxs-lookup"><span data-stu-id="174aa-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="174aa-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="174aa-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="174aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="174aa-107">DESCRIPTION</span></span>
<span data-ttu-id="174aa-108">Cmdleten **import-AzureRmApiManagementApi** importerar ett API för Azure API-hantering från en fil eller en URL-adress (Web Application Description Language), WSDL-eller Swagger-format.</span><span class="sxs-lookup"><span data-stu-id="174aa-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="174aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="174aa-109">EXAMPLES</span></span>

### <span data-ttu-id="174aa-110">Exempel 1 importera ett API från en WADL-fil</span><span class="sxs-lookup"><span data-stu-id="174aa-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="174aa-111">Det här kommandot importerar ett API från den angivna WADL-filen.</span><span class="sxs-lookup"><span data-stu-id="174aa-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="174aa-112">Exempel 2 importera ett API från en Swagger-fil</span><span class="sxs-lookup"><span data-stu-id="174aa-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="174aa-113">Det här kommandot importerar ett API från den angivna Swagger-filen.</span><span class="sxs-lookup"><span data-stu-id="174aa-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="174aa-114">Exempel 3: importera ett API från en WADL-länk</span><span class="sxs-lookup"><span data-stu-id="174aa-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="174aa-115">Det här kommandot importerar ett API från den angivna WADL-länken.</span><span class="sxs-lookup"><span data-stu-id="174aa-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="174aa-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="174aa-116">PARAMETERS</span></span>

### <span data-ttu-id="174aa-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="174aa-117">-ApiId</span></span>
<span data-ttu-id="174aa-118">Anger ID för det API som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="174aa-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="174aa-119">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="174aa-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="174aa-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="174aa-120">-ApiType</span></span>
<span data-ttu-id="174aa-121">Den här parametern är valfri med standardvärdet för http.</span><span class="sxs-lookup"><span data-stu-id="174aa-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="174aa-122">SOAP-alternativet är endast tillämpligt när WSDL importeras och skapar ett SOAP passthrough API.</span><span class="sxs-lookup"><span data-stu-id="174aa-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174aa-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="174aa-123">-Context</span></span>
<span data-ttu-id="174aa-124">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="174aa-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="174aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174aa-125">-DefaultProfile</span></span>
<span data-ttu-id="174aa-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="174aa-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="174aa-127">-Path</span><span class="sxs-lookup"><span data-stu-id="174aa-127">-Path</span></span>
<span data-ttu-id="174aa-128">Anger en Web API-sökväg som den sista delen av API: s offentliga webb adress.</span><span class="sxs-lookup"><span data-stu-id="174aa-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="174aa-129">Denna URL används av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="174aa-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="174aa-130">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="174aa-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="174aa-131">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="174aa-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="174aa-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="174aa-132">-SpecificationFormat</span></span>
<span data-ttu-id="174aa-133">Anger Specifikations format.</span><span class="sxs-lookup"><span data-stu-id="174aa-133">Specifies the specification format.</span></span>
<span data-ttu-id="174aa-134">psdx_paramvalues Wadl, WSDL och swagger.</span><span class="sxs-lookup"><span data-stu-id="174aa-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174aa-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="174aa-135">-SpecificationPath</span></span>
<span data-ttu-id="174aa-136">Anger sökvägen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="174aa-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174aa-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="174aa-137">-SpecificationUrl</span></span>
<span data-ttu-id="174aa-138">Anger URL-adressen till specifikationen.</span><span class="sxs-lookup"><span data-stu-id="174aa-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="174aa-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="174aa-139">-WsdlEndpointName</span></span>
<span data-ttu-id="174aa-140">Det lokala namnet på den WSDL-slutpunkt (port) som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="174aa-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="174aa-141">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="174aa-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="174aa-142">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="174aa-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="174aa-143">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="174aa-143">Default value is $null.</span></span>

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

### <span data-ttu-id="174aa-144">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="174aa-144">-WsdlServiceName</span></span>
<span data-ttu-id="174aa-145">Det lokala namnet på WSDL-tjänsten som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="174aa-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="174aa-146">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="174aa-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="174aa-147">Den här parametern är valfri och krävs bara för att importera WSDL.</span><span class="sxs-lookup"><span data-stu-id="174aa-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="174aa-148">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="174aa-148">Default value is $null.</span></span>

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

### <span data-ttu-id="174aa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174aa-149">CommonParameters</span></span>
<span data-ttu-id="174aa-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174aa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174aa-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174aa-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174aa-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="174aa-152">INPUTS</span></span>

### <span data-ttu-id="174aa-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="174aa-153">None</span></span>
<span data-ttu-id="174aa-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="174aa-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="174aa-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="174aa-155">OUTPUTS</span></span>

### <span data-ttu-id="174aa-156">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="174aa-157">Denna cmdlet returnerar det importerade API: t som ett **PsApiManagementApi** -objekt.</span><span class="sxs-lookup"><span data-stu-id="174aa-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="174aa-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="174aa-158">NOTES</span></span>

## <span data-ttu-id="174aa-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="174aa-159">RELATED LINKS</span></span>

[<span data-ttu-id="174aa-160">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="174aa-161">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="174aa-162">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="174aa-163">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="174aa-164">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="174aa-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


