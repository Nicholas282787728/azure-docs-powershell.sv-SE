---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574083"
---
# <span data-ttu-id="2a9a5-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2a9a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9a5-103">Hämtar ett API.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a9a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a9a5-104">SYNTAX</span></span>

### <span data-ttu-id="2a9a5-105">GetAllApis (standard)</span><span class="sxs-lookup"><span data-stu-id="2a9a5-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9a5-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="2a9a5-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a9a5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="2a9a5-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a9a5-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="2a9a5-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a9a5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a9a5-109">DESCRIPTION</span></span>
<span data-ttu-id="2a9a5-110">Cmdleten **Get-AzureRmApiManagementApi** har en eller flera API: er för Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="2a9a5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a9a5-111">EXAMPLES</span></span>

### <span data-ttu-id="2a9a5-112">Exempel 1: Hämta alla hanterings-API: er</span><span class="sxs-lookup"><span data-stu-id="2a9a5-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="2a9a5-113">Det här kommandot får alla API: er för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="2a9a5-114">Exempel 2: Hämta ett Management API efter ID</span><span class="sxs-lookup"><span data-stu-id="2a9a5-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="2a9a5-115">Det här kommandot får API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="2a9a5-116">Exempel 3: Hämta ett Management API efter namn</span><span class="sxs-lookup"><span data-stu-id="2a9a5-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="2a9a5-117">Det här kommandot får API: t med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="2a9a5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a9a5-118">PARAMETERS</span></span>

### <span data-ttu-id="2a9a5-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2a9a5-119">-ApiId</span></span>
<span data-ttu-id="2a9a5-120">Anger ID för det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="2a9a5-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2a9a5-121">-ApiRevision</span></span>
<span data-ttu-id="2a9a5-122">Revisions-ID för den speciella API-revision.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="2a9a5-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a9a5-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2a9a5-124">-Context</span></span>
<span data-ttu-id="2a9a5-125">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a9a5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9a5-126">-DefaultProfile</span></span>
<span data-ttu-id="2a9a5-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a9a5-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a9a5-128">-Name</span></span>
<span data-ttu-id="2a9a5-129">Anger namnet på det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="2a9a5-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="2a9a5-130">-ProductId</span></span>
<span data-ttu-id="2a9a5-131">Anger ID för den produkt som du vill hämta API för.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="2a9a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9a5-132">CommonParameters</span></span>
<span data-ttu-id="2a9a5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9a5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a9a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9a5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a9a5-135">INPUTS</span></span>

### <span data-ttu-id="2a9a5-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a9a5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a9a5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2a9a5-137">System.String</span></span>

## <span data-ttu-id="2a9a5-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a9a5-138">OUTPUTS</span></span>

### <span data-ttu-id="2a9a5-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2a9a5-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a9a5-140">NOTES</span></span>

## <span data-ttu-id="2a9a5-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a9a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="2a9a5-142">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a9a5-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a9a5-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a9a5-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a9a5-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a9a5-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


