---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581811"
---
# <span data-ttu-id="8bac8-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="8bac8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bac8-102">SYNOPSIS</span></span>
<span data-ttu-id="8bac8-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="8bac8-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bac8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bac8-104">SYNTAX</span></span>

### <span data-ttu-id="8bac8-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="8bac8-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bac8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8bac8-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bac8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bac8-107">DESCRIPTION</span></span>
<span data-ttu-id="8bac8-108">Cmdleten **set-AzureRmApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="8bac8-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="8bac8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bac8-109">EXAMPLES</span></span>

### <span data-ttu-id="8bac8-110">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="8bac8-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="8bac8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bac8-111">PARAMETERS</span></span>

### <span data-ttu-id="8bac8-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8bac8-112">-ApiId</span></span>
<span data-ttu-id="8bac8-113">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="8bac8-113">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bac8-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8bac8-114">-AuthorizationScope</span></span>
<span data-ttu-id="8bac8-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="8bac8-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="8bac8-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="8bac8-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8bac8-117">-AuthorizationServerId</span></span>
<span data-ttu-id="8bac8-118">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="8bac8-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="8bac8-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-119">The default value is $Null.</span></span>
<span data-ttu-id="8bac8-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="8bac8-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="8bac8-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8bac8-121">-Context</span></span>
<span data-ttu-id="8bac8-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8bac8-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bac8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bac8-123">-DefaultProfile</span></span>
<span data-ttu-id="8bac8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8bac8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bac8-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8bac8-125">-Description</span></span>
<span data-ttu-id="8bac8-126">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="8bac8-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="8bac8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bac8-127">-InputObject</span></span>
<span data-ttu-id="8bac8-128">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="8bac8-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="8bac8-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8bac8-129">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bac8-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="8bac8-130">-Name</span></span>
<span data-ttu-id="8bac8-131">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="8bac8-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="8bac8-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bac8-132">-PassThru</span></span>
<span data-ttu-id="8bac8-133">passthru</span><span class="sxs-lookup"><span data-stu-id="8bac8-133">passthru</span></span>

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

### <span data-ttu-id="8bac8-134">-Path</span><span class="sxs-lookup"><span data-stu-id="8bac8-134">-Path</span></span>
<span data-ttu-id="8bac8-135">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="8bac8-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="8bac8-136">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="8bac8-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="8bac8-137">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="8bac8-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8bac8-138">-Protocols</span></span>
<span data-ttu-id="8bac8-139">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="8bac8-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="8bac8-140">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="8bac8-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="8bac8-141">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="8bac8-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="8bac8-142">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="8bac8-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8bac8-143">-ServiceUrl</span></span>
<span data-ttu-id="8bac8-144">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="8bac8-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="8bac8-145">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="8bac8-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="8bac8-146">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="8bac8-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="8bac8-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8bac8-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8bac8-148">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="8bac8-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="8bac8-149">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="8bac8-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8bac8-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8bac8-151">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="8bac8-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="8bac8-152">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="8bac8-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="8bac8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bac8-153">CommonParameters</span></span>
<span data-ttu-id="8bac8-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bac8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bac8-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bac8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bac8-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bac8-156">INPUTS</span></span>

### <span data-ttu-id="8bac8-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8bac8-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8bac8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8bac8-158">System.String</span></span>

### <span data-ttu-id="8bac8-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="8bac8-160">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8bac8-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8bac8-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="8bac8-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="8bac8-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8bac8-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8bac8-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bac8-163">OUTPUTS</span></span>

### <span data-ttu-id="8bac8-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8bac8-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bac8-165">NOTES</span></span>

## <span data-ttu-id="8bac8-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bac8-166">RELATED LINKS</span></span>

[<span data-ttu-id="8bac8-167">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="8bac8-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="8bac8-169">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="8bac8-170">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="8bac8-171">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bac8-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


