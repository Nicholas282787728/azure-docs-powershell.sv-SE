---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743376"
---
# <span data-ttu-id="1b272-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="1b272-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b272-102">SYNOPSIS</span></span>
<span data-ttu-id="1b272-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="1b272-103">Creates an API.</span></span>

## <span data-ttu-id="1b272-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b272-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b272-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b272-105">DESCRIPTION</span></span>
<span data-ttu-id="1b272-106">Cmdleten **New-AzApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="1b272-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="1b272-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b272-107">EXAMPLES</span></span>

### <span data-ttu-id="1b272-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="1b272-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="1b272-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="1b272-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="1b272-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b272-110">PARAMETERS</span></span>

### <span data-ttu-id="1b272-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1b272-111">-ApiId</span></span>
<span data-ttu-id="1b272-112">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1b272-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="1b272-113">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="1b272-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="1b272-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1b272-114">-AuthorizationScope</span></span>
<span data-ttu-id="1b272-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="1b272-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="1b272-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b272-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1b272-117">-AuthorizationServerId</span></span>
<span data-ttu-id="1b272-118">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="1b272-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="1b272-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-119">The default value is $Null.</span></span>
<span data-ttu-id="1b272-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="1b272-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="1b272-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1b272-121">-Context</span></span>
<span data-ttu-id="1b272-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1b272-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b272-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b272-123">-DefaultProfile</span></span>
<span data-ttu-id="1b272-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b272-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b272-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1b272-125">-Description</span></span>
<span data-ttu-id="1b272-126">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="1b272-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="1b272-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b272-127">-Name</span></span>
<span data-ttu-id="1b272-128">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="1b272-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="1b272-129">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="1b272-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="1b272-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1b272-130">-Path</span></span>
<span data-ttu-id="1b272-131">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="1b272-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="1b272-132">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="1b272-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="1b272-133">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b272-134">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="1b272-134">-ProductIds</span></span>
<span data-ttu-id="1b272-135">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="1b272-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b272-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1b272-136">-Protocols</span></span>
<span data-ttu-id="1b272-137">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="1b272-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="1b272-138">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="1b272-138">Valid values are http, https.</span></span>
<span data-ttu-id="1b272-139">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="1b272-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="1b272-140">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b272-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1b272-141">-ServiceUrl</span></span>
<span data-ttu-id="1b272-142">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="1b272-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="1b272-143">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="1b272-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="1b272-144">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="1b272-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="1b272-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1b272-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1b272-146">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1b272-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="1b272-147">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b272-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1b272-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1b272-149">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1b272-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="1b272-150">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="1b272-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b272-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b272-151">CommonParameters</span></span>
<span data-ttu-id="1b272-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b272-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b272-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b272-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b272-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b272-154">INPUTS</span></span>

### <span data-ttu-id="1b272-155">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b272-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1b272-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1b272-156">System.String</span></span>

### <span data-ttu-id="1b272-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="1b272-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="1b272-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="1b272-158">System.String[]</span></span>

## <span data-ttu-id="1b272-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b272-159">OUTPUTS</span></span>

### <span data-ttu-id="1b272-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1b272-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b272-161">NOTES</span></span>

## <span data-ttu-id="1b272-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b272-162">RELATED LINKS</span></span>

[<span data-ttu-id="1b272-163">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="1b272-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="1b272-165">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="1b272-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="1b272-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b272-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


