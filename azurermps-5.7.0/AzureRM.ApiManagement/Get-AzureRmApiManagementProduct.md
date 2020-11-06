---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576662"
---
# <span data-ttu-id="86916-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="86916-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="86916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86916-102">SYNOPSIS</span></span>
<span data-ttu-id="86916-103">Hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="86916-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86916-104">SYNTAX</span></span>

### <span data-ttu-id="86916-105">GetAllProducts (standard)</span><span class="sxs-lookup"><span data-stu-id="86916-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86916-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="86916-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86916-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="86916-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86916-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86916-108">DESCRIPTION</span></span>
<span data-ttu-id="86916-109">Cmdleten **Get-AzureRmApiManagementProduct** hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="86916-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="86916-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86916-110">EXAMPLES</span></span>

### <span data-ttu-id="86916-111">Exempel 1: Hämta alla produkter</span><span class="sxs-lookup"><span data-stu-id="86916-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="86916-112">Det här kommandot får alla API-hanterings produkter.</span><span class="sxs-lookup"><span data-stu-id="86916-112">This command get all API Management products.</span></span>

### <span data-ttu-id="86916-113">Exempel 2: skaffa en produkt utifrån ID</span><span class="sxs-lookup"><span data-stu-id="86916-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="86916-114">Det här kommandot hämtar en API-hanterings produkt utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="86916-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="86916-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86916-115">PARAMETERS</span></span>

### <span data-ttu-id="86916-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="86916-116">-Context</span></span>
<span data-ttu-id="86916-117">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="86916-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86916-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86916-118">-DefaultProfile</span></span>
<span data-ttu-id="86916-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86916-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86916-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="86916-120">-ProductId</span></span>
<span data-ttu-id="86916-121">Anger produktens identifierare att söka efter.</span><span class="sxs-lookup"><span data-stu-id="86916-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86916-122">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="86916-122">-Title</span></span>
<span data-ttu-id="86916-123">Anger rubriken för produkten som du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="86916-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="86916-124">Om det här alternativet anges försöker cmdleten hämta produkten efter titel.</span><span class="sxs-lookup"><span data-stu-id="86916-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86916-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86916-125">CommonParameters</span></span>
<span data-ttu-id="86916-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86916-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86916-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86916-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86916-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86916-128">INPUTS</span></span>

### <span data-ttu-id="86916-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="86916-129">None</span></span>
<span data-ttu-id="86916-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="86916-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86916-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86916-131">OUTPUTS</span></span>

### <span data-ttu-id="86916-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="86916-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="86916-133">Information om produkten i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="86916-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="86916-134">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="86916-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="86916-135">Listan med produkt i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="86916-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="86916-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86916-136">NOTES</span></span>

## <span data-ttu-id="86916-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86916-137">RELATED LINKS</span></span>

[<span data-ttu-id="86916-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="86916-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="86916-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="86916-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="86916-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="86916-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


