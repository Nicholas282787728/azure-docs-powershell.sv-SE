---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578679"
---
# <span data-ttu-id="7b450-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b450-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="7b450-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b450-102">SYNOPSIS</span></span>
<span data-ttu-id="7b450-103">Hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="7b450-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b450-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b450-104">SYNTAX</span></span>

### <span data-ttu-id="7b450-105">Hämta alla producst (standard)</span><span class="sxs-lookup"><span data-stu-id="7b450-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b450-106">Skaffa efter ID</span><span class="sxs-lookup"><span data-stu-id="7b450-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b450-107">Få med rubrik</span><span class="sxs-lookup"><span data-stu-id="7b450-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b450-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b450-108">DESCRIPTION</span></span>
<span data-ttu-id="7b450-109">Cmdleten **Get-AzureRmApiManagementProduct** hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="7b450-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="7b450-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b450-110">EXAMPLES</span></span>

### <span data-ttu-id="7b450-111">Exempel 1: Hämta alla produkter</span><span class="sxs-lookup"><span data-stu-id="7b450-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="7b450-112">Det här kommandot får alla API-hanterings produkter.</span><span class="sxs-lookup"><span data-stu-id="7b450-112">This command get all API Management products.</span></span>

### <span data-ttu-id="7b450-113">Exempel 2: skaffa en produkt utifrån ID</span><span class="sxs-lookup"><span data-stu-id="7b450-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="7b450-114">Det här kommandot hämtar en API-hanterings produkt utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="7b450-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="7b450-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b450-115">PARAMETERS</span></span>

### <span data-ttu-id="7b450-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7b450-116">-Context</span></span>
<span data-ttu-id="7b450-117">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7b450-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7b450-118">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="7b450-118">-ProductId</span></span>
<span data-ttu-id="7b450-119">Anger produktens identifierare att söka efter.</span><span class="sxs-lookup"><span data-stu-id="7b450-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b450-120">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="7b450-120">-Title</span></span>
<span data-ttu-id="7b450-121">Anger rubriken för produkten som du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="7b450-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="7b450-122">Om det här alternativet anges försöker cmdleten hämta produkten efter titel.</span><span class="sxs-lookup"><span data-stu-id="7b450-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b450-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b450-123">-DefaultProfile</span></span>
<span data-ttu-id="7b450-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b450-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b450-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b450-125">CommonParameters</span></span>
<span data-ttu-id="7b450-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b450-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b450-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b450-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b450-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b450-128">INPUTS</span></span>

## <span data-ttu-id="7b450-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b450-129">OUTPUTS</span></span>

### <span data-ttu-id="7b450-130">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="7b450-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="7b450-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b450-131">NOTES</span></span>

## <span data-ttu-id="7b450-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b450-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b450-133">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b450-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7b450-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b450-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7b450-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b450-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


