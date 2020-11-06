---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 36560b23d9108ff1f8cd981abdb44a3c24f25402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573581"
---
# <span data-ttu-id="5fd90-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5fd90-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="5fd90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fd90-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd90-103">Skapar en API-hanterings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5fd90-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fd90-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fd90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fd90-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd90-106">**New-AzureRmApiManagementOperation-** cmdleten skapa en API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5fd90-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="5fd90-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fd90-107">EXAMPLES</span></span>

### <span data-ttu-id="5fd90-108">Exempel 1: skapa en API-hanterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="5fd90-108">Example 1: Create an API management operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="5fd90-109">Det här kommandot skapar en API-hanterings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="5fd90-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="5fd90-110">Exempel 2: skapa en API-hanterings åtgärd med förfrågnings-och svars uppgifter</span><span class="sxs-lookup"><span data-stu-id="5fd90-110">Example 2: Create an API management operation with request and response details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="5fd90-111">I det här exemplet skapas en API-hanterings åtgärd med förfrågnings-och svars uppgifter.</span><span class="sxs-lookup"><span data-stu-id="5fd90-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="5fd90-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fd90-112">PARAMETERS</span></span>

### <span data-ttu-id="5fd90-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5fd90-113">-ApiId</span></span>
<span data-ttu-id="5fd90-114">Anger ID för API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="5fd90-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5fd90-115">-Context</span></span>
<span data-ttu-id="5fd90-116">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="5fd90-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5fd90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd90-117">-DefaultProfile</span></span>
<span data-ttu-id="5fd90-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5fd90-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5fd90-119">-Description</span></span>
<span data-ttu-id="5fd90-120">Anger beskrivningen av den nya API-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-120">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="5fd90-121">-Metod</span><span class="sxs-lookup"><span data-stu-id="5fd90-121">-Method</span></span>
<span data-ttu-id="5fd90-122">Anger HTTP-metoden för den nya API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-122">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="5fd90-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fd90-123">-Name</span></span>
<span data-ttu-id="5fd90-124">Anger visnings namnet på den nya API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-124">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="5fd90-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5fd90-125">-OperationId</span></span>
<span data-ttu-id="5fd90-126">Anger ID för API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-126">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="5fd90-127">-Begäran</span><span class="sxs-lookup"><span data-stu-id="5fd90-127">-Request</span></span>
<span data-ttu-id="5fd90-128">Anger information om API-hanterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5fd90-128">Specifies the details of the API management operation.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd90-129">-Svar</span><span class="sxs-lookup"><span data-stu-id="5fd90-129">-Responses</span></span>
<span data-ttu-id="5fd90-130">Anger en matris med möjliga API-hanterings svar.</span><span class="sxs-lookup"><span data-stu-id="5fd90-130">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd90-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="5fd90-131">-TemplateParameters</span></span>
<span data-ttu-id="5fd90-132">Anger en matris med parametrar som definierats i parametern *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="5fd90-132">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="5fd90-133">Om du inte anger den här parametern genereras ett standardvärde baserat på *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="5fd90-133">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd90-134">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="5fd90-134">-UrlTemplate</span></span>
<span data-ttu-id="5fd90-135">Anger URL-mallen.</span><span class="sxs-lookup"><span data-stu-id="5fd90-135">Specifies the URL template.</span></span>

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

### <span data-ttu-id="5fd90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd90-136">CommonParameters</span></span>
<span data-ttu-id="5fd90-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd90-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd90-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd90-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fd90-139">INPUTS</span></span>

### <span data-ttu-id="5fd90-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="5fd90-140">None</span></span>
<span data-ttu-id="5fd90-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5fd90-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fd90-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fd90-142">OUTPUTS</span></span>

### <span data-ttu-id="5fd90-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5fd90-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="5fd90-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fd90-144">NOTES</span></span>

## <span data-ttu-id="5fd90-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fd90-145">RELATED LINKS</span></span>

[<span data-ttu-id="5fd90-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5fd90-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5fd90-147">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5fd90-147">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5fd90-148">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5fd90-148">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


