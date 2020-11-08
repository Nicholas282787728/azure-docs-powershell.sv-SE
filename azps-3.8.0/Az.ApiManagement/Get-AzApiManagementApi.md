---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 7ec3eacc32157b833095522bbebc76f3838ae2a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089681"
---
# <span data-ttu-id="dd423-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="dd423-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd423-102">SYNOPSIS</span></span>
<span data-ttu-id="dd423-103">Hämtar ett API.</span><span class="sxs-lookup"><span data-stu-id="dd423-103">Gets an API.</span></span>

## <span data-ttu-id="dd423-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd423-104">SYNTAX</span></span>

### <span data-ttu-id="dd423-105">GetAllApis (standard)</span><span class="sxs-lookup"><span data-stu-id="dd423-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd423-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="dd423-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd423-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="dd423-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd423-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="dd423-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd423-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd423-109">DESCRIPTION</span></span>
<span data-ttu-id="dd423-110">Cmdleten **Get-AzApiManagementApi** har en eller flera API: er för Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="dd423-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="dd423-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd423-111">EXAMPLES</span></span>

### <span data-ttu-id="dd423-112">Exempel 1: Hämta alla hanterings-API: er</span><span class="sxs-lookup"><span data-stu-id="dd423-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="dd423-113">Det här kommandot får alla API: er för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="dd423-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="dd423-114">Exempel 2: Hämta ett Management API efter ID</span><span class="sxs-lookup"><span data-stu-id="dd423-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="dd423-115">Det här kommandot får API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="dd423-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="dd423-116">Exempel 3: Hämta ett Management API efter namn</span><span class="sxs-lookup"><span data-stu-id="dd423-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="dd423-117">Det här kommandot får API: t med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="dd423-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="dd423-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd423-118">PARAMETERS</span></span>

### <span data-ttu-id="dd423-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dd423-119">-ApiId</span></span>
<span data-ttu-id="dd423-120">Anger ID för det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dd423-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd423-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd423-121">-ApiRevision</span></span>
<span data-ttu-id="dd423-122">Revisions-ID för den speciella API-revision.</span><span class="sxs-lookup"><span data-stu-id="dd423-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="dd423-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="dd423-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd423-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="dd423-124">-Context</span></span>
<span data-ttu-id="dd423-125">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dd423-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dd423-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd423-126">-DefaultProfile</span></span>
<span data-ttu-id="dd423-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd423-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd423-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd423-128">-Name</span></span>
<span data-ttu-id="dd423-129">Anger namnet på det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dd423-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd423-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="dd423-130">-ProductId</span></span>
<span data-ttu-id="dd423-131">Anger ID för den produkt som du vill hämta API för.</span><span class="sxs-lookup"><span data-stu-id="dd423-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd423-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd423-132">CommonParameters</span></span>
<span data-ttu-id="dd423-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd423-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd423-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd423-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd423-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd423-135">INPUTS</span></span>

### <span data-ttu-id="dd423-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd423-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd423-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dd423-137">System.String</span></span>

## <span data-ttu-id="dd423-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd423-138">OUTPUTS</span></span>

### <span data-ttu-id="dd423-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="dd423-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd423-140">NOTES</span></span>

## <span data-ttu-id="dd423-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd423-141">RELATED LINKS</span></span>

[<span data-ttu-id="dd423-142">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="dd423-143">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dd423-144">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="dd423-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="dd423-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd423-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


