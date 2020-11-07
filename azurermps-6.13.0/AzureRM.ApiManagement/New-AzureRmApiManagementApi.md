---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 2601635bb3fc9ac1f6886adcb2cbb971a3cf0d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757152"
---
# <span data-ttu-id="d7ae2-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="d7ae2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ae2-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ae2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7ae2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7ae2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ae2-106">Cmdleten **New-AzureRmApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="d7ae2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="d7ae2-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="d7ae2-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="d7ae2-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="d7ae2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7ae2-110">PARAMETERS</span></span>

### <span data-ttu-id="d7ae2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7ae2-111">-ApiId</span></span>
<span data-ttu-id="d7ae2-112">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="d7ae2-113">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="d7ae2-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d7ae2-114">-AuthorizationScope</span></span>
<span data-ttu-id="d7ae2-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="d7ae2-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="d7ae2-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="d7ae2-117">-AuthorizationServerId</span></span>
<span data-ttu-id="d7ae2-118">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="d7ae2-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-119">The default value is $Null.</span></span>
<span data-ttu-id="d7ae2-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="d7ae2-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d7ae2-121">-Context</span></span>
<span data-ttu-id="d7ae2-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d7ae2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ae2-123">-DefaultProfile</span></span>
<span data-ttu-id="d7ae2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ae2-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d7ae2-125">-Description</span></span>
<span data-ttu-id="d7ae2-126">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="d7ae2-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7ae2-127">-Name</span></span>
<span data-ttu-id="d7ae2-128">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="d7ae2-129">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="d7ae2-130">-Path</span><span class="sxs-lookup"><span data-stu-id="d7ae2-130">-Path</span></span>
<span data-ttu-id="d7ae2-131">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="d7ae2-132">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="d7ae2-133">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="d7ae2-134">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="d7ae2-134">-ProductIds</span></span>
<span data-ttu-id="d7ae2-135">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="d7ae2-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d7ae2-136">-Protocols</span></span>
<span data-ttu-id="d7ae2-137">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="d7ae2-138">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-138">Valid values are http, https.</span></span>
<span data-ttu-id="d7ae2-139">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="d7ae2-140">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="d7ae2-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d7ae2-141">-ServiceUrl</span></span>
<span data-ttu-id="d7ae2-142">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="d7ae2-143">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="d7ae2-144">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="d7ae2-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d7ae2-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d7ae2-146">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="d7ae2-147">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="d7ae2-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d7ae2-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d7ae2-149">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="d7ae2-150">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="d7ae2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ae2-151">CommonParameters</span></span>
<span data-ttu-id="d7ae2-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ae2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ae2-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ae2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ae2-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7ae2-154">INPUTS</span></span>

### <span data-ttu-id="d7ae2-155">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7ae2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7ae2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="d7ae2-156">System.String</span></span>

### <span data-ttu-id="d7ae2-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="d7ae2-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="d7ae2-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="d7ae2-158">System.String[]</span></span>

## <span data-ttu-id="d7ae2-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7ae2-159">OUTPUTS</span></span>

### <span data-ttu-id="d7ae2-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d7ae2-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7ae2-161">NOTES</span></span>

## <span data-ttu-id="d7ae2-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7ae2-162">RELATED LINKS</span></span>

[<span data-ttu-id="d7ae2-163">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-163">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="d7ae2-164">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-164">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="d7ae2-165">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-165">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="d7ae2-166">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-166">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="d7ae2-167">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d7ae2-167">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


