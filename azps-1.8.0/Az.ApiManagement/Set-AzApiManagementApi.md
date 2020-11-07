---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917725"
---
# <span data-ttu-id="2487e-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="2487e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2487e-102">SYNOPSIS</span></span>
<span data-ttu-id="2487e-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="2487e-103">Modifies an API.</span></span>

## <span data-ttu-id="2487e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2487e-104">SYNTAX</span></span>

### <span data-ttu-id="2487e-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="2487e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2487e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2487e-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2487e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2487e-107">DESCRIPTION</span></span>
<span data-ttu-id="2487e-108">Cmdleten **set-AzApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="2487e-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2487e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2487e-109">EXAMPLES</span></span>

### <span data-ttu-id="2487e-110">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="2487e-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="2487e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2487e-111">PARAMETERS</span></span>

### <span data-ttu-id="2487e-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2487e-112">-ApiId</span></span>
<span data-ttu-id="2487e-113">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="2487e-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="2487e-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2487e-114">-AuthorizationScope</span></span>
<span data-ttu-id="2487e-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2487e-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2487e-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="2487e-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2487e-117">-AuthorizationServerId</span></span>
<span data-ttu-id="2487e-118">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="2487e-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2487e-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-119">The default value is $Null.</span></span>
<span data-ttu-id="2487e-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="2487e-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2487e-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2487e-121">-Context</span></span>
<span data-ttu-id="2487e-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2487e-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2487e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2487e-123">-DefaultProfile</span></span>
<span data-ttu-id="2487e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2487e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2487e-125">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2487e-125">-Description</span></span>
<span data-ttu-id="2487e-126">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="2487e-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2487e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2487e-127">-InputObject</span></span>
<span data-ttu-id="2487e-128">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="2487e-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="2487e-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2487e-129">This parameter is required.</span></span>

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

### <span data-ttu-id="2487e-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="2487e-130">-Name</span></span>
<span data-ttu-id="2487e-131">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="2487e-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="2487e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2487e-132">-PassThru</span></span>
<span data-ttu-id="2487e-133">passthru</span><span class="sxs-lookup"><span data-stu-id="2487e-133">passthru</span></span>

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

### <span data-ttu-id="2487e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="2487e-134">-Path</span></span>
<span data-ttu-id="2487e-135">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="2487e-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2487e-136">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2487e-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2487e-137">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="2487e-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2487e-138">-Protocols</span></span>
<span data-ttu-id="2487e-139">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="2487e-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2487e-140">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="2487e-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2487e-141">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="2487e-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2487e-142">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="2487e-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2487e-143">-ServiceUrl</span></span>
<span data-ttu-id="2487e-144">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="2487e-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2487e-145">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="2487e-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2487e-146">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2487e-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2487e-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2487e-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2487e-148">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="2487e-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2487e-149">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="2487e-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2487e-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2487e-151">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="2487e-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2487e-152">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="2487e-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="2487e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2487e-153">CommonParameters</span></span>
<span data-ttu-id="2487e-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2487e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2487e-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2487e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2487e-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2487e-156">INPUTS</span></span>

### <span data-ttu-id="2487e-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2487e-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2487e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2487e-158">System.String</span></span>

### <span data-ttu-id="2487e-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="2487e-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="2487e-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2487e-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2487e-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2487e-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2487e-162">OUTPUTS</span></span>

### <span data-ttu-id="2487e-163">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2487e-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2487e-164">NOTES</span></span>

## <span data-ttu-id="2487e-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2487e-165">RELATED LINKS</span></span>

[<span data-ttu-id="2487e-166">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2487e-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2487e-168">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2487e-169">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2487e-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2487e-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


