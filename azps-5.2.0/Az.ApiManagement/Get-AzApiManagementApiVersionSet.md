---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414296"
---
# <span data-ttu-id="77e12-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="77e12-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="77e12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77e12-102">SYNOPSIS</span></span>
<span data-ttu-id="77e12-103">Få information om API-versions uppsättningarna</span><span class="sxs-lookup"><span data-stu-id="77e12-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="77e12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77e12-104">SYNTAX</span></span>

### <span data-ttu-id="77e12-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="77e12-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e12-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e12-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e12-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77e12-107">DESCRIPTION</span></span>
<span data-ttu-id="77e12-108">Cmdleten **Get-AzApiManagementApiVersionSet** hämtar information om API-versions uppsättningarna som kon figurer ATS i en API-hanterings kontext.</span><span class="sxs-lookup"><span data-stu-id="77e12-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="77e12-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77e12-109">EXAMPLES</span></span>

### <span data-ttu-id="77e12-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77e12-110">Example 1</span></span>

### <span data-ttu-id="77e12-111">Exempel 2: Hämta alla API-versioner</span><span class="sxs-lookup"><span data-stu-id="77e12-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="77e12-112">Det här kommandot får alla API-versioner för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="77e12-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="77e12-113">Exempel 3: Hämta en API-version utifrån ID</span><span class="sxs-lookup"><span data-stu-id="77e12-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="77e12-114">Det här kommandot får API-versionen inställd med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="77e12-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="77e12-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77e12-115">PARAMETERS</span></span>

### <span data-ttu-id="77e12-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="77e12-116">-ApiVersionSetId</span></span>
<span data-ttu-id="77e12-117">API-identifierare att leta efter.</span><span class="sxs-lookup"><span data-stu-id="77e12-117">API identifier to look for.</span></span>
<span data-ttu-id="77e12-118">Om det här alternativet anges kommer API: t att hämtas via ID.</span><span class="sxs-lookup"><span data-stu-id="77e12-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="77e12-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="77e12-119">-Context</span></span>
<span data-ttu-id="77e12-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="77e12-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="77e12-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="77e12-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e12-122">-DefaultProfile</span></span>
<span data-ttu-id="77e12-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77e12-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e12-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e12-124">-ResourceId</span></span>
<span data-ttu-id="77e12-125">Arm-resurs-ID för ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="77e12-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="77e12-126">Om det här alternativet är angivet försöker apiVersionSet efter ID.</span><span class="sxs-lookup"><span data-stu-id="77e12-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="77e12-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="77e12-127">This parameter is required.</span></span>

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

### <span data-ttu-id="77e12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e12-128">CommonParameters</span></span>
<span data-ttu-id="77e12-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e12-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e12-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e12-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77e12-131">INPUTS</span></span>

### <span data-ttu-id="77e12-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77e12-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="77e12-133">System. String</span><span class="sxs-lookup"><span data-stu-id="77e12-133">System.String</span></span>

## <span data-ttu-id="77e12-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77e12-134">OUTPUTS</span></span>

### <span data-ttu-id="77e12-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="77e12-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="77e12-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77e12-136">NOTES</span></span>

## <span data-ttu-id="77e12-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77e12-137">RELATED LINKS</span></span>

[<span data-ttu-id="77e12-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="77e12-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="77e12-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="77e12-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="77e12-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="77e12-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
