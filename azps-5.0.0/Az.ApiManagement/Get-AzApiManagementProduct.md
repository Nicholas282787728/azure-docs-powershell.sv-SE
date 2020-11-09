---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324822"
---
# <span data-ttu-id="ffaf7-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ffaf7-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="ffaf7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="ffaf7-103">Hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="ffaf7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffaf7-104">SYNTAX</span></span>

### <span data-ttu-id="ffaf7-105">GetAllProducts (standard)</span><span class="sxs-lookup"><span data-stu-id="ffaf7-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffaf7-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="ffaf7-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffaf7-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="ffaf7-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffaf7-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="ffaf7-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffaf7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffaf7-109">DESCRIPTION</span></span>
<span data-ttu-id="ffaf7-110">Cmdleten **Get-AzApiManagementProduct** hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="ffaf7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffaf7-111">EXAMPLES</span></span>

### <span data-ttu-id="ffaf7-112">Exempel 1: Hämta alla produkter</span><span class="sxs-lookup"><span data-stu-id="ffaf7-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="ffaf7-113">Det här kommandot får alla API-hanterings produkter.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-113">This command get all API Management products.</span></span>

### <span data-ttu-id="ffaf7-114">Exempel 2: skaffa en produkt utifrån ID</span><span class="sxs-lookup"><span data-stu-id="ffaf7-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="ffaf7-115">Det här kommandot hämtar en API-hanterings produkt utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="ffaf7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffaf7-116">PARAMETERS</span></span>

### <span data-ttu-id="ffaf7-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ffaf7-117">-ApiId</span></span>
<span data-ttu-id="ffaf7-118">ApiId av API för att hitta de korrelerade produkterna.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="ffaf7-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ffaf7-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ffaf7-120">-Context</span></span>
<span data-ttu-id="ffaf7-121">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ffaf7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffaf7-122">-DefaultProfile</span></span>
<span data-ttu-id="ffaf7-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffaf7-124">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="ffaf7-124">-ProductId</span></span>
<span data-ttu-id="ffaf7-125">Anger produktens identifierare att söka efter.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="ffaf7-126">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="ffaf7-126">-Title</span></span>
<span data-ttu-id="ffaf7-127">Anger rubriken för produkten som du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="ffaf7-128">Om det här alternativet anges försöker cmdleten hämta produkten efter titel.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffaf7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffaf7-129">CommonParameters</span></span>
<span data-ttu-id="ffaf7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffaf7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffaf7-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffaf7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffaf7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffaf7-132">INPUTS</span></span>

### <span data-ttu-id="ffaf7-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ffaf7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ffaf7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ffaf7-134">System.String</span></span>

## <span data-ttu-id="ffaf7-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffaf7-135">OUTPUTS</span></span>

### <span data-ttu-id="ffaf7-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ffaf7-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="ffaf7-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffaf7-137">NOTES</span></span>

## <span data-ttu-id="ffaf7-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffaf7-138">RELATED LINKS</span></span>

[<span data-ttu-id="ffaf7-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ffaf7-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="ffaf7-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ffaf7-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="ffaf7-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ffaf7-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


