---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579680"
---
# <span data-ttu-id="33bfc-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="33bfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="33bfc-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="33bfc-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33bfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33bfc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33bfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="33bfc-106">Cmdleten **set-AzureRmApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="33bfc-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="33bfc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33bfc-107">EXAMPLES</span></span>

### <span data-ttu-id="33bfc-108">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="33bfc-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="33bfc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33bfc-109">PARAMETERS</span></span>

### <span data-ttu-id="33bfc-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33bfc-110">-ApiId</span></span>
<span data-ttu-id="33bfc-111">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="33bfc-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="33bfc-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="33bfc-112">-AuthorizationScope</span></span>
<span data-ttu-id="33bfc-113">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="33bfc-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="33bfc-114">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="33bfc-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="33bfc-115">-AuthorizationServerId</span></span>
<span data-ttu-id="33bfc-116">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="33bfc-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="33bfc-117">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-117">The default value is $Null.</span></span>
<span data-ttu-id="33bfc-118">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="33bfc-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="33bfc-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="33bfc-119">-Context</span></span>
<span data-ttu-id="33bfc-120">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="33bfc-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="33bfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bfc-121">-DefaultProfile</span></span>
<span data-ttu-id="33bfc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33bfc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="33bfc-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="33bfc-123">-Description</span></span>
<span data-ttu-id="33bfc-124">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="33bfc-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="33bfc-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="33bfc-125">-Name</span></span>
<span data-ttu-id="33bfc-126">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="33bfc-126">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="33bfc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33bfc-127">-PassThru</span></span>
<span data-ttu-id="33bfc-128">passthru</span><span class="sxs-lookup"><span data-stu-id="33bfc-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33bfc-129">-Path</span><span class="sxs-lookup"><span data-stu-id="33bfc-129">-Path</span></span>
<span data-ttu-id="33bfc-130">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="33bfc-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="33bfc-131">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="33bfc-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="33bfc-132">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-132">The default value is $Null.</span></span>

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

### <span data-ttu-id="33bfc-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="33bfc-133">-Protocols</span></span>
<span data-ttu-id="33bfc-134">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="33bfc-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="33bfc-135">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="33bfc-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="33bfc-136">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="33bfc-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="33bfc-137">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="33bfc-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="33bfc-138">-ServiceUrl</span></span>
<span data-ttu-id="33bfc-139">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="33bfc-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="33bfc-140">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="33bfc-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="33bfc-141">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="33bfc-141">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="33bfc-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="33bfc-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="33bfc-143">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="33bfc-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="33bfc-144">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-144">The default value is $Null.</span></span>

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

### <span data-ttu-id="33bfc-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="33bfc-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="33bfc-146">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="33bfc-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="33bfc-147">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="33bfc-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="33bfc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bfc-148">CommonParameters</span></span>
<span data-ttu-id="33bfc-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33bfc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bfc-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33bfc-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bfc-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33bfc-151">INPUTS</span></span>

### <span data-ttu-id="33bfc-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="33bfc-152">None</span></span>
<span data-ttu-id="33bfc-153">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="33bfc-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33bfc-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33bfc-154">OUTPUTS</span></span>

### <span data-ttu-id="33bfc-155">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="33bfc-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33bfc-156">NOTES</span></span>

## <span data-ttu-id="33bfc-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33bfc-157">RELATED LINKS</span></span>

[<span data-ttu-id="33bfc-158">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="33bfc-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="33bfc-160">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="33bfc-161">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="33bfc-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33bfc-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


