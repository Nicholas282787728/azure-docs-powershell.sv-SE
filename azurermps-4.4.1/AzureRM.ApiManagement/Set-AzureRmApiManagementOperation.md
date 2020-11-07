---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757506"
---
# <span data-ttu-id="f7513-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f7513-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f7513-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7513-102">SYNOPSIS</span></span>
<span data-ttu-id="f7513-103">Anger information om API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="f7513-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7513-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7513-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7513-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7513-105">DESCRIPTION</span></span>
<span data-ttu-id="f7513-106">Cmdleten **set-AzureRmApiManagementOperation** anger API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="f7513-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="f7513-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7513-107">EXAMPLES</span></span>

### <span data-ttu-id="f7513-108">Exempel 1: Ange åtgärds uppgifter</span><span class="sxs-lookup"><span data-stu-id="f7513-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="f7513-109">Det här kommandot anger åtgärds informationen för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="f7513-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="f7513-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7513-110">PARAMETERS</span></span>

### <span data-ttu-id="f7513-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f7513-111">-ApiId</span></span>
<span data-ttu-id="f7513-112">Anger API-identifierare.</span><span class="sxs-lookup"><span data-stu-id="f7513-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="f7513-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f7513-113">-Context</span></span>
<span data-ttu-id="f7513-114">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f7513-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f7513-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f7513-115">-Description</span></span>
<span data-ttu-id="f7513-116">Anger beskrivningen för den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f7513-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="f7513-117">-Metod</span><span class="sxs-lookup"><span data-stu-id="f7513-117">-Method</span></span>
<span data-ttu-id="f7513-118">Anger HTTP-metoden för den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f7513-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="f7513-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7513-119">-Name</span></span>
<span data-ttu-id="f7513-120">Anger visnings namnet på den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f7513-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="f7513-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f7513-121">-OperationId</span></span>
<span data-ttu-id="f7513-122">Anger identifierare för den befintliga åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f7513-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="f7513-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7513-123">-PassThru</span></span>
<span data-ttu-id="f7513-124">passthru</span><span class="sxs-lookup"><span data-stu-id="f7513-124">passthru</span></span>

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

### <span data-ttu-id="f7513-125">-Begäran</span><span class="sxs-lookup"><span data-stu-id="f7513-125">-Request</span></span>
<span data-ttu-id="f7513-126">Anger information om betalningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="f7513-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="f7513-127">-Svar</span><span class="sxs-lookup"><span data-stu-id="f7513-127">-Responses</span></span>
<span data-ttu-id="f7513-128">Anger en matris med möjliga åtgärds svar.</span><span class="sxs-lookup"><span data-stu-id="f7513-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="f7513-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="f7513-129">-TemplateParameters</span></span>
<span data-ttu-id="f7513-130">Anger en matris eller parametrar som definierats i parameter *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="f7513-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f7513-131">Om du inte anger något värde genereras ett standardvärde baserat på UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="f7513-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="f7513-132">Använd parametern för att ge mer information om parametrar som beskrivning, typ och andra möjliga värden.</span><span class="sxs-lookup"><span data-stu-id="f7513-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="f7513-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f7513-133">-UrlTemplate</span></span>
<span data-ttu-id="f7513-134">Anger URL-mallen.</span><span class="sxs-lookup"><span data-stu-id="f7513-134">Specifies the URL template.</span></span>
<span data-ttu-id="f7513-135">Till exempel: kunder/{CID}/order/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="f7513-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="f7513-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7513-136">-DefaultProfile</span></span>
<span data-ttu-id="f7513-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7513-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7513-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7513-138">CommonParameters</span></span>
<span data-ttu-id="f7513-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7513-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7513-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7513-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7513-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7513-141">INPUTS</span></span>

## <span data-ttu-id="f7513-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7513-142">OUTPUTS</span></span>

### <span data-ttu-id="f7513-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f7513-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f7513-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7513-144">NOTES</span></span>

## <span data-ttu-id="f7513-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7513-145">RELATED LINKS</span></span>

[<span data-ttu-id="f7513-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f7513-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f7513-147">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f7513-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f7513-148">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f7513-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


