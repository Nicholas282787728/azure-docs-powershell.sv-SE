---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757517"
---
# <span data-ttu-id="543b2-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="543b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="543b2-102">SYNOPSIS</span></span>
<span data-ttu-id="543b2-103">Hämtar ett API.</span><span class="sxs-lookup"><span data-stu-id="543b2-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="543b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="543b2-104">SYNTAX</span></span>

### <span data-ttu-id="543b2-105">Alla API: er (standard)</span><span class="sxs-lookup"><span data-stu-id="543b2-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="543b2-106">Sök efter ID</span><span class="sxs-lookup"><span data-stu-id="543b2-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="543b2-107">Sök efter namn</span><span class="sxs-lookup"><span data-stu-id="543b2-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="543b2-108">Sök efter produkt-ID</span><span class="sxs-lookup"><span data-stu-id="543b2-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="543b2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="543b2-109">DESCRIPTION</span></span>
<span data-ttu-id="543b2-110">Cmdleten **Get-AzureRmApiManagementApi** har en eller flera API: er för Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="543b2-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="543b2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="543b2-111">EXAMPLES</span></span>

### <span data-ttu-id="543b2-112">Exempel 1: Hämta alla hanterings-API: er</span><span class="sxs-lookup"><span data-stu-id="543b2-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="543b2-113">Det här kommandot får alla API: er för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="543b2-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="543b2-114">Exempel 2: Hämta ett Management API efter ID</span><span class="sxs-lookup"><span data-stu-id="543b2-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="543b2-115">Det här kommandot får API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="543b2-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="543b2-116">Exempel 3: Hämta ett Management API efter namn</span><span class="sxs-lookup"><span data-stu-id="543b2-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="543b2-117">Det här kommandot får API: t med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="543b2-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="543b2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="543b2-118">PARAMETERS</span></span>

### <span data-ttu-id="543b2-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="543b2-119">-ApiId</span></span>
<span data-ttu-id="543b2-120">Anger ID för det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="543b2-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="543b2-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="543b2-121">-Context</span></span>
<span data-ttu-id="543b2-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="543b2-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="543b2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="543b2-123">-Name</span></span>
<span data-ttu-id="543b2-124">Anger namnet på det API som ska visas.</span><span class="sxs-lookup"><span data-stu-id="543b2-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="543b2-125">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="543b2-125">-ProductId</span></span>
<span data-ttu-id="543b2-126">Anger ID för den produkt som du vill hämta API för.</span><span class="sxs-lookup"><span data-stu-id="543b2-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="543b2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="543b2-127">-DefaultProfile</span></span>
<span data-ttu-id="543b2-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="543b2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="543b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="543b2-129">CommonParameters</span></span>
<span data-ttu-id="543b2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="543b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="543b2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="543b2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="543b2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="543b2-132">INPUTS</span></span>

## <span data-ttu-id="543b2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="543b2-133">OUTPUTS</span></span>

### <span data-ttu-id="543b2-134">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="543b2-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="543b2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="543b2-135">NOTES</span></span>

## <span data-ttu-id="543b2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="543b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="543b2-137">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="543b2-138">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="543b2-139">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="543b2-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="543b2-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="543b2-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


