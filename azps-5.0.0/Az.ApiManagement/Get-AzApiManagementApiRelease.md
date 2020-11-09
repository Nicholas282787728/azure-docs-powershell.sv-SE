---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324095"
---
# <span data-ttu-id="cd626-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd626-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="cd626-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd626-102">SYNOPSIS</span></span>
<span data-ttu-id="cd626-103">Hämta API-versionen.</span><span class="sxs-lookup"><span data-stu-id="cd626-103">Get the API Release.</span></span>

## <span data-ttu-id="cd626-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd626-104">SYNTAX</span></span>

### <span data-ttu-id="cd626-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd626-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd626-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd626-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd626-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd626-107">DESCRIPTION</span></span>
<span data-ttu-id="cd626-108">Cmdleten **Get-AzApiManagementApiRelease** får en eller flera versioner av API: et för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="cd626-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="cd626-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd626-109">EXAMPLES</span></span>

### <span data-ttu-id="cd626-110">Exempel 1: få alla utgåvor av API: t</span><span class="sxs-lookup"><span data-stu-id="cd626-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="cd626-111">Det här kommandot får alla utgåvor av `echo-api` API: t för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="cd626-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="cd626-112">Exempel 2: Hämta utgivnings information för den aktuella API-versionen</span><span class="sxs-lookup"><span data-stu-id="cd626-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="cd626-113">Det här kommandot hämtar information om ett visst API med den angivna releaseId.</span><span class="sxs-lookup"><span data-stu-id="cd626-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="cd626-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd626-114">PARAMETERS</span></span>

### <span data-ttu-id="cd626-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cd626-115">-ApiId</span></span>
<span data-ttu-id="cd626-116">API-identifierare att leta efter.</span><span class="sxs-lookup"><span data-stu-id="cd626-116">API identifier to look for.</span></span>
<span data-ttu-id="cd626-117">Om det här alternativet anges kommer API: t att hämtas via ID.</span><span class="sxs-lookup"><span data-stu-id="cd626-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd626-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cd626-118">-Context</span></span>
<span data-ttu-id="cd626-119">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cd626-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cd626-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cd626-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd626-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd626-121">-DefaultProfile</span></span>
<span data-ttu-id="cd626-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd626-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd626-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="cd626-123">-ReleaseId</span></span>
<span data-ttu-id="cd626-124">ID för versionen.</span><span class="sxs-lookup"><span data-stu-id="cd626-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd626-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd626-125">-ResourceId</span></span>
<span data-ttu-id="cd626-126">Arm-resurs-ID för en API-version.</span><span class="sxs-lookup"><span data-stu-id="cd626-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="cd626-127">Om det anges försöker hitta API-utgivningen med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="cd626-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="cd626-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cd626-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd626-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd626-129">CommonParameters</span></span>
<span data-ttu-id="cd626-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd626-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd626-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd626-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd626-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd626-132">INPUTS</span></span>

### <span data-ttu-id="cd626-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd626-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd626-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd626-134">System.String</span></span>

## <span data-ttu-id="cd626-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd626-135">OUTPUTS</span></span>

### <span data-ttu-id="cd626-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd626-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cd626-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd626-137">NOTES</span></span>

## <span data-ttu-id="cd626-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd626-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd626-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd626-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="cd626-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd626-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="cd626-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd626-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)