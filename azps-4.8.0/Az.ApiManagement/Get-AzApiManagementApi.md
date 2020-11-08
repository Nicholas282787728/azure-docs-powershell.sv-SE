---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261934"
---
# <span data-ttu-id="b0b02-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="b0b02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0b02-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b02-103">Hämtar ett API.</span><span class="sxs-lookup"><span data-stu-id="b0b02-103">Gets an API.</span></span>

## <span data-ttu-id="b0b02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0b02-104">SYNTAX</span></span>

### <span data-ttu-id="b0b02-105">GetAllApis (standard)</span><span class="sxs-lookup"><span data-stu-id="b0b02-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0b02-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="b0b02-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b02-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="b0b02-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b02-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="b0b02-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b02-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="b0b02-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b02-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0b02-110">DESCRIPTION</span></span>
<span data-ttu-id="b0b02-111">Cmdleten **Get-AzApiManagementApi** har en eller flera API: er för Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="b0b02-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="b0b02-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0b02-112">EXAMPLES</span></span>

### <span data-ttu-id="b0b02-113">Exempel 1: Hämta alla hanterings-API: er</span><span class="sxs-lookup"><span data-stu-id="b0b02-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="b0b02-114">Det här kommandot får alla API: er för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="b0b02-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="b0b02-115">Exempel 2: Hämta ett Management API efter ID</span><span class="sxs-lookup"><span data-stu-id="b0b02-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="b0b02-116">Det här kommandot får API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="b0b02-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="b0b02-117">Exempel 3: Hämta ett Management API efter namn</span><span class="sxs-lookup"><span data-stu-id="b0b02-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="b0b02-118">Det här kommandot får API: t med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="b0b02-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="b0b02-119">Exempel 4: skaffa ett Management API genom GatewayId</span><span class="sxs-lookup"><span data-stu-id="b0b02-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="b0b02-120">Det här kommandot får API: t för angiven GatewayId.</span><span class="sxs-lookup"><span data-stu-id="b0b02-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="b0b02-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0b02-121">PARAMETERS</span></span>

### <span data-ttu-id="b0b02-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b0b02-122">-ApiId</span></span>
<span data-ttu-id="b0b02-123">Anger ID för det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="b0b02-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b0b02-124">-ApiRevision</span></span>
<span data-ttu-id="b0b02-125">Revisions-ID för den speciella API-revision.</span><span class="sxs-lookup"><span data-stu-id="b0b02-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="b0b02-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b0b02-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="b0b02-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b0b02-127">-Context</span></span>
<span data-ttu-id="b0b02-128">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b0b02-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b0b02-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b02-129">-DefaultProfile</span></span>
<span data-ttu-id="b0b02-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b02-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0b02-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b0b02-131">-GatewayId</span></span>
<span data-ttu-id="b0b02-132">Om det här är angivet försöker alla gateway API: er.</span><span class="sxs-lookup"><span data-stu-id="b0b02-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b02-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0b02-133">-Name</span></span>
<span data-ttu-id="b0b02-134">Anger namnet på det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="b0b02-135">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="b0b02-135">-ProductId</span></span>
<span data-ttu-id="b0b02-136">Anger ID för den produkt som du vill hämta API för.</span><span class="sxs-lookup"><span data-stu-id="b0b02-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="b0b02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b02-137">CommonParameters</span></span>
<span data-ttu-id="b0b02-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b02-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0b02-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b02-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0b02-140">INPUTS</span></span>

### <span data-ttu-id="b0b02-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0b02-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0b02-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0b02-142">System.String</span></span>

## <span data-ttu-id="b0b02-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0b02-143">OUTPUTS</span></span>

### <span data-ttu-id="b0b02-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="b0b02-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0b02-145">NOTES</span></span>

## <span data-ttu-id="b0b02-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0b02-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0b02-147">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="b0b02-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="b0b02-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="b0b02-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="b0b02-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b0b02-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


