---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270157"
---
# <span data-ttu-id="c69b2-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c69b2-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="c69b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c69b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c69b2-103">Skapar en API-hanterings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c69b2-103">Creates an API management operation.</span></span>

## <span data-ttu-id="c69b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c69b2-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c69b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c69b2-106">**New-AzApiManagementOperation-** cmdleten skapa en API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c69b2-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="c69b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c69b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c69b2-108">Exempel 1: skapa en API-hanterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="c69b2-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="c69b2-109">Det här kommandot skapar en API-hanterings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="c69b2-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="c69b2-110">Exempel 2: skapa en API-hanterings åtgärd med förfrågnings-och svars uppgifter</span><span class="sxs-lookup"><span data-stu-id="c69b2-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="c69b2-111">I det här exemplet skapas en API-hanterings åtgärd med förfrågnings-och svars uppgifter.</span><span class="sxs-lookup"><span data-stu-id="c69b2-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="c69b2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c69b2-112">PARAMETERS</span></span>

### <span data-ttu-id="c69b2-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c69b2-113">-ApiId</span></span>
<span data-ttu-id="c69b2-114">Anger ID för API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="c69b2-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c69b2-115">-ApiRevision</span></span>
<span data-ttu-id="c69b2-116">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="c69b2-116">Identifier of API Revision.</span></span> <span data-ttu-id="c69b2-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c69b2-117">This parameter is optional.</span></span> <span data-ttu-id="c69b2-118">Om du inte anger den kopplas åtgärden till den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="c69b2-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="c69b2-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c69b2-119">-Context</span></span>
<span data-ttu-id="c69b2-120">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="c69b2-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c69b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69b2-121">-DefaultProfile</span></span>
<span data-ttu-id="c69b2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c69b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c69b2-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c69b2-123">-Description</span></span>
<span data-ttu-id="c69b2-124">Anger beskrivningen av den nya API-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="c69b2-125">-Metod</span><span class="sxs-lookup"><span data-stu-id="c69b2-125">-Method</span></span>
<span data-ttu-id="c69b2-126">Anger HTTP-metoden för den nya API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="c69b2-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="c69b2-127">-Name</span></span>
<span data-ttu-id="c69b2-128">Anger visnings namnet på den nya API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="c69b2-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c69b2-129">-OperationId</span></span>
<span data-ttu-id="c69b2-130">Anger ID för API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="c69b2-131">-Begäran</span><span class="sxs-lookup"><span data-stu-id="c69b2-131">-Request</span></span>
<span data-ttu-id="c69b2-132">Anger information om API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c69b2-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69b2-133">-Svar</span><span class="sxs-lookup"><span data-stu-id="c69b2-133">-Responses</span></span>
<span data-ttu-id="c69b2-134">Anger en matris med möjliga API-hanterings svar.</span><span class="sxs-lookup"><span data-stu-id="c69b2-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69b2-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="c69b2-135">-TemplateParameters</span></span>
<span data-ttu-id="c69b2-136">Anger en matris med parametrar som definierats i parametern *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="c69b2-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="c69b2-137">Om du inte anger den här parametern genereras ett standardvärde baserat på *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="c69b2-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69b2-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="c69b2-138">-UrlTemplate</span></span>
<span data-ttu-id="c69b2-139">Anger URL-mallen.</span><span class="sxs-lookup"><span data-stu-id="c69b2-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="c69b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69b2-140">CommonParameters</span></span>
<span data-ttu-id="c69b2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69b2-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c69b2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69b2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c69b2-143">INPUTS</span></span>

### <span data-ttu-id="c69b2-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c69b2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c69b2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c69b2-145">System.String</span></span>

### <span data-ttu-id="c69b2-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="c69b2-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="c69b2-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="c69b2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="c69b2-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="c69b2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="c69b2-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c69b2-149">OUTPUTS</span></span>

### <span data-ttu-id="c69b2-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c69b2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="c69b2-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c69b2-151">NOTES</span></span>

## <span data-ttu-id="c69b2-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c69b2-152">RELATED LINKS</span></span>

[<span data-ttu-id="c69b2-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c69b2-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="c69b2-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c69b2-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="c69b2-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c69b2-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


