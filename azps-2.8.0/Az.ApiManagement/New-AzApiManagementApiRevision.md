---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 1a58c34aac272f6c8278833cd356de66774c5a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745798"
---
# <span data-ttu-id="cfc27-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="cfc27-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="cfc27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfc27-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc27-103">Skapar en ny version av ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="cfc27-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="cfc27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfc27-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfc27-105">DESCRIPTION</span></span>

<span data-ttu-id="cfc27-106">Cmdleten **New-AzApiManagementApiRevision** skapar en API-revision för en befintlig API i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="cfc27-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="cfc27-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfc27-107">EXAMPLES</span></span>

### <span data-ttu-id="cfc27-108">Exempel 1: skapa en tom API-revision för ett API</span><span class="sxs-lookup"><span data-stu-id="cfc27-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="cfc27-109">Det här kommandot skapar en API-revision `2` av `echo-api` API: t.</span><span class="sxs-lookup"><span data-stu-id="cfc27-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="cfc27-110">Exempel 2: skapa en API-revision från ett befintligt API och kopiera alla åtgärder, taggar och principer</span><span class="sxs-lookup"><span data-stu-id="cfc27-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="cfc27-111">Det här kommandot skapar en API-revision `5` av `echo-api` API: t.</span><span class="sxs-lookup"><span data-stu-id="cfc27-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="cfc27-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfc27-112">PARAMETERS</span></span>

### <span data-ttu-id="cfc27-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cfc27-113">-ApiId</span></span>
<span data-ttu-id="cfc27-114">ID för API vars ändring ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cfc27-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="cfc27-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cfc27-115">-ApiRevision</span></span>
<span data-ttu-id="cfc27-116">Revisions-ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="cfc27-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="cfc27-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="cfc27-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="cfc27-118">Beskrivning av API-revision.</span><span class="sxs-lookup"><span data-stu-id="cfc27-118">Api Revision Description.</span></span> <span data-ttu-id="cfc27-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cfc27-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfc27-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cfc27-120">-Context</span></span>
<span data-ttu-id="cfc27-121">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cfc27-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cfc27-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cfc27-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc27-123">-DefaultProfile</span></span>
<span data-ttu-id="cfc27-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc27-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc27-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="cfc27-125">-ServiceUrl</span></span>
<span data-ttu-id="cfc27-126">En URL för webb tjänsten som visar API i backend-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cfc27-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="cfc27-127">Denna URL kommer endast att användas av Azure API Management och blir inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="cfc27-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="cfc27-128">Måste vara 1 till 2000 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="cfc27-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="cfc27-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cfc27-129">This parameter is required.</span></span>

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

### <span data-ttu-id="cfc27-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="cfc27-130">-SourceApiRevision</span></span>
<span data-ttu-id="cfc27-131">API-version för käll-API.</span><span class="sxs-lookup"><span data-stu-id="cfc27-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="cfc27-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cfc27-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="cfc27-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfc27-133">-Confirm</span></span>
<span data-ttu-id="cfc27-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfc27-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc27-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc27-135">-WhatIf</span></span>
<span data-ttu-id="cfc27-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfc27-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfc27-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfc27-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc27-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc27-138">CommonParameters</span></span>
<span data-ttu-id="cfc27-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc27-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc27-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfc27-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc27-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfc27-141">INPUTS</span></span>

### <span data-ttu-id="cfc27-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cfc27-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cfc27-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc27-143">System.String</span></span>

## <span data-ttu-id="cfc27-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfc27-144">OUTPUTS</span></span>

### <span data-ttu-id="cfc27-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfc27-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cfc27-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfc27-146">NOTES</span></span>

## <span data-ttu-id="cfc27-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfc27-147">RELATED LINKS</span></span>

[<span data-ttu-id="cfc27-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfc27-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="cfc27-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfc27-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="cfc27-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cfc27-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
