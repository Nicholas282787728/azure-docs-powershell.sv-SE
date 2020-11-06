---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 4c9dc60ad1c531a5da9f32abc0090475c32a7ad5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583875"
---
# <span data-ttu-id="c2a60-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="c2a60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2a60-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a60-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="c2a60-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2a60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2a60-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2a60-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a60-106">Cmdleten **set-AzureRmApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c2a60-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="c2a60-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2a60-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a60-108">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="c2a60-108">Example 1 Modify an API</span></span>
```
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="c2a60-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2a60-109">PARAMETERS</span></span>

### <span data-ttu-id="c2a60-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c2a60-110">-ApiId</span></span>
<span data-ttu-id="c2a60-111">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c2a60-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="c2a60-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="c2a60-112">-AuthorizationScope</span></span>
<span data-ttu-id="c2a60-113">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="c2a60-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="c2a60-114">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="c2a60-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="c2a60-115">-AuthorizationServerId</span></span>
<span data-ttu-id="c2a60-116">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="c2a60-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="c2a60-117">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-117">The default value is $Null.</span></span>
<span data-ttu-id="c2a60-118">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="c2a60-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="c2a60-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c2a60-119">-Context</span></span>
<span data-ttu-id="c2a60-120">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c2a60-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c2a60-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c2a60-121">-Description</span></span>
<span data-ttu-id="c2a60-122">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="c2a60-122">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="c2a60-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2a60-123">-Name</span></span>
<span data-ttu-id="c2a60-124">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="c2a60-124">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="c2a60-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2a60-125">-PassThru</span></span>
<span data-ttu-id="c2a60-126">passthru</span><span class="sxs-lookup"><span data-stu-id="c2a60-126">passthru</span></span>

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

### <span data-ttu-id="c2a60-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c2a60-127">-Path</span></span>
<span data-ttu-id="c2a60-128">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="c2a60-128">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="c2a60-129">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="c2a60-129">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="c2a60-130">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-130">The default value is $Null.</span></span>

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

### <span data-ttu-id="c2a60-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c2a60-131">-Protocols</span></span>
<span data-ttu-id="c2a60-132">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="c2a60-132">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="c2a60-133">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="c2a60-133">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="c2a60-134">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="c2a60-134">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="c2a60-135">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="c2a60-136">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="c2a60-136">-ServiceUrl</span></span>
<span data-ttu-id="c2a60-137">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="c2a60-137">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="c2a60-138">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="c2a60-138">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="c2a60-139">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="c2a60-139">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="c2a60-140">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="c2a60-140">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="c2a60-141">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="c2a60-141">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="c2a60-142">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="c2a60-143">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="c2a60-143">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="c2a60-144">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="c2a60-144">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="c2a60-145">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="c2a60-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="c2a60-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a60-146">-DefaultProfile</span></span>
<span data-ttu-id="c2a60-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a60-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2a60-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a60-148">CommonParameters</span></span>
<span data-ttu-id="c2a60-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a60-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a60-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a60-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a60-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2a60-151">INPUTS</span></span>

## <span data-ttu-id="c2a60-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2a60-152">OUTPUTS</span></span>

### <span data-ttu-id="c2a60-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c2a60-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2a60-154">NOTES</span></span>

## <span data-ttu-id="c2a60-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2a60-155">RELATED LINKS</span></span>

[<span data-ttu-id="c2a60-156">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-156">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="c2a60-157">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-157">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="c2a60-158">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-158">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="c2a60-159">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-159">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="c2a60-160">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2a60-160">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


