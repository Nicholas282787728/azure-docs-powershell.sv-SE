---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: d30b48a7e1860610dc772555bc7e7428ec1ee3f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917682"
---
# <span data-ttu-id="cb511-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="cb511-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="cb511-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb511-102">SYNOPSIS</span></span>
<span data-ttu-id="cb511-103">Anger information om API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="cb511-103">Sets API operation details.</span></span>

## <span data-ttu-id="cb511-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb511-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb511-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb511-105">DESCRIPTION</span></span>
<span data-ttu-id="cb511-106">Cmdleten **set-AzApiManagementOperation** anger API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="cb511-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="cb511-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb511-107">EXAMPLES</span></span>

### <span data-ttu-id="cb511-108">Exempel 1: Ange åtgärds uppgifter</span><span class="sxs-lookup"><span data-stu-id="cb511-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="cb511-109">Det här kommandot anger åtgärds informationen för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="cb511-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="cb511-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb511-110">PARAMETERS</span></span>

### <span data-ttu-id="cb511-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cb511-111">-ApiId</span></span>
<span data-ttu-id="cb511-112">Anger API-identifierare.</span><span class="sxs-lookup"><span data-stu-id="cb511-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="cb511-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cb511-113">-ApiRevision</span></span>
<span data-ttu-id="cb511-114">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="cb511-114">Identifier of API Revision.</span></span> <span data-ttu-id="cb511-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cb511-115">This parameter is optional.</span></span> <span data-ttu-id="cb511-116">Om det inte anges uppdateras åtgärden i den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="cb511-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="cb511-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cb511-117">-Context</span></span>
<span data-ttu-id="cb511-118">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="cb511-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="cb511-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb511-119">-DefaultProfile</span></span>
<span data-ttu-id="cb511-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb511-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb511-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cb511-121">-Description</span></span>
<span data-ttu-id="cb511-122">Anger beskrivningen för den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cb511-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="cb511-123">-Metod</span><span class="sxs-lookup"><span data-stu-id="cb511-123">-Method</span></span>
<span data-ttu-id="cb511-124">Anger HTTP-metoden för den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cb511-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="cb511-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb511-125">-Name</span></span>
<span data-ttu-id="cb511-126">Anger visnings namnet på den nya åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cb511-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="cb511-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="cb511-127">-OperationId</span></span>
<span data-ttu-id="cb511-128">Anger identifierare för den befintliga åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cb511-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="cb511-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb511-129">-PassThru</span></span>
<span data-ttu-id="cb511-130">passthru</span><span class="sxs-lookup"><span data-stu-id="cb511-130">passthru</span></span>

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

### <span data-ttu-id="cb511-131">-Begäran</span><span class="sxs-lookup"><span data-stu-id="cb511-131">-Request</span></span>
<span data-ttu-id="cb511-132">Anger information om betalningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="cb511-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="cb511-133">-Svar</span><span class="sxs-lookup"><span data-stu-id="cb511-133">-Responses</span></span>
<span data-ttu-id="cb511-134">Anger en matris med möjliga åtgärds svar.</span><span class="sxs-lookup"><span data-stu-id="cb511-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="cb511-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="cb511-135">-TemplateParameters</span></span>
<span data-ttu-id="cb511-136">Anger en matris eller parametrar som definierats i parameter *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="cb511-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="cb511-137">Om du inte anger något värde genereras ett standardvärde baserat på UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="cb511-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="cb511-138">Använd parametern för att ge mer information om parametrar som beskrivning, typ och andra möjliga värden.</span><span class="sxs-lookup"><span data-stu-id="cb511-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="cb511-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="cb511-139">-UrlTemplate</span></span>
<span data-ttu-id="cb511-140">Anger URL-mallen.</span><span class="sxs-lookup"><span data-stu-id="cb511-140">Specifies the URL template.</span></span>
<span data-ttu-id="cb511-141">Till exempel: kunder/{CID}/order/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="cb511-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="cb511-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb511-142">CommonParameters</span></span>
<span data-ttu-id="cb511-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb511-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb511-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb511-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb511-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb511-145">INPUTS</span></span>

### <span data-ttu-id="cb511-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb511-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb511-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cb511-147">System.String</span></span>

### <span data-ttu-id="cb511-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="cb511-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="cb511-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="cb511-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="cb511-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="cb511-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="cb511-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cb511-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cb511-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb511-152">OUTPUTS</span></span>

### <span data-ttu-id="cb511-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="cb511-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="cb511-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb511-154">NOTES</span></span>

## <span data-ttu-id="cb511-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb511-155">RELATED LINKS</span></span>

[<span data-ttu-id="cb511-156">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="cb511-156">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="cb511-157">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="cb511-157">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="cb511-158">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="cb511-158">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


