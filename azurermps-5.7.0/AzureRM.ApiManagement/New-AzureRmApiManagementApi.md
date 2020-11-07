---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757724"
---
# <span data-ttu-id="a1c66-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a1c66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1c66-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c66-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="a1c66-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1c66-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1c66-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c66-106">Cmdleten **New-AzureRmApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="a1c66-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="a1c66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1c66-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c66-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="a1c66-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="a1c66-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="a1c66-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="a1c66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1c66-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c66-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1c66-111">-ApiId</span></span>
<span data-ttu-id="a1c66-112">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a1c66-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="a1c66-113">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="a1c66-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="a1c66-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a1c66-114">-AuthorizationScope</span></span>
<span data-ttu-id="a1c66-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a1c66-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="a1c66-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="a1c66-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="a1c66-117">-AuthorizationServerId</span></span>
<span data-ttu-id="a1c66-118">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="a1c66-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="a1c66-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-119">The default value is $Null.</span></span>
<span data-ttu-id="a1c66-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="a1c66-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="a1c66-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a1c66-121">-Context</span></span>
<span data-ttu-id="a1c66-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a1c66-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a1c66-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c66-123">-DefaultProfile</span></span>
<span data-ttu-id="a1c66-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c66-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a1c66-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a1c66-125">-Description</span></span>
<span data-ttu-id="a1c66-126">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="a1c66-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="a1c66-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1c66-127">-Name</span></span>
<span data-ttu-id="a1c66-128">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="a1c66-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="a1c66-129">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="a1c66-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="a1c66-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a1c66-130">-Path</span></span>
<span data-ttu-id="a1c66-131">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="a1c66-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="a1c66-132">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="a1c66-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="a1c66-133">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="a1c66-134">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="a1c66-134">-ProductIds</span></span>
<span data-ttu-id="a1c66-135">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="a1c66-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c66-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a1c66-136">-Protocols</span></span>
<span data-ttu-id="a1c66-137">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="a1c66-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="a1c66-138">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="a1c66-138">Valid values are http, https.</span></span>
<span data-ttu-id="a1c66-139">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="a1c66-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="a1c66-140">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-140">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c66-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a1c66-141">-ServiceUrl</span></span>
<span data-ttu-id="a1c66-142">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="a1c66-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="a1c66-143">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="a1c66-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="a1c66-144">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="a1c66-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="a1c66-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a1c66-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a1c66-146">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a1c66-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="a1c66-147">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="a1c66-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a1c66-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a1c66-149">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a1c66-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="a1c66-150">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="a1c66-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="a1c66-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c66-151">CommonParameters</span></span>
<span data-ttu-id="a1c66-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c66-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c66-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c66-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c66-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1c66-154">INPUTS</span></span>

### <span data-ttu-id="a1c66-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="a1c66-155">None</span></span>
<span data-ttu-id="a1c66-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a1c66-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1c66-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1c66-157">OUTPUTS</span></span>

### <span data-ttu-id="a1c66-158">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a1c66-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1c66-159">NOTES</span></span>

## <span data-ttu-id="a1c66-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1c66-160">RELATED LINKS</span></span>

[<span data-ttu-id="a1c66-161">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1c66-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1c66-163">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1c66-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a1c66-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a1c66-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


