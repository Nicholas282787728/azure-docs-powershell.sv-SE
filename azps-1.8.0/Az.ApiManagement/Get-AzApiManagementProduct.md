---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743400"
---
# <span data-ttu-id="17679-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="17679-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="17679-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17679-102">SYNOPSIS</span></span>
<span data-ttu-id="17679-103">Hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="17679-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="17679-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17679-104">SYNTAX</span></span>

### <span data-ttu-id="17679-105">GetAllProducts (standard)</span><span class="sxs-lookup"><span data-stu-id="17679-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17679-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="17679-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17679-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="17679-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17679-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17679-108">DESCRIPTION</span></span>
<span data-ttu-id="17679-109">Cmdleten **Get-AzApiManagementProduct** hämtar en lista eller en viss produkt.</span><span class="sxs-lookup"><span data-stu-id="17679-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="17679-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17679-110">EXAMPLES</span></span>

### <span data-ttu-id="17679-111">Exempel 1: Hämta alla produkter</span><span class="sxs-lookup"><span data-stu-id="17679-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="17679-112">Det här kommandot får alla API-hanterings produkter.</span><span class="sxs-lookup"><span data-stu-id="17679-112">This command get all API Management products.</span></span>

### <span data-ttu-id="17679-113">Exempel 2: skaffa en produkt utifrån ID</span><span class="sxs-lookup"><span data-stu-id="17679-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="17679-114">Det här kommandot hämtar en API-hanterings produkt utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="17679-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="17679-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17679-115">PARAMETERS</span></span>

### <span data-ttu-id="17679-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="17679-116">-Context</span></span>
<span data-ttu-id="17679-117">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="17679-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="17679-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17679-118">-DefaultProfile</span></span>
<span data-ttu-id="17679-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17679-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17679-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="17679-120">-ProductId</span></span>
<span data-ttu-id="17679-121">Anger produktens identifierare att söka efter.</span><span class="sxs-lookup"><span data-stu-id="17679-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="17679-122">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="17679-122">-Title</span></span>
<span data-ttu-id="17679-123">Anger rubriken för produkten som du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="17679-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="17679-124">Om det här alternativet anges försöker cmdleten hämta produkten efter titel.</span><span class="sxs-lookup"><span data-stu-id="17679-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="17679-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17679-125">CommonParameters</span></span>
<span data-ttu-id="17679-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17679-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17679-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17679-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17679-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17679-128">INPUTS</span></span>

### <span data-ttu-id="17679-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17679-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17679-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17679-130">System.String</span></span>

## <span data-ttu-id="17679-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17679-131">OUTPUTS</span></span>

### <span data-ttu-id="17679-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="17679-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="17679-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17679-133">NOTES</span></span>

## <span data-ttu-id="17679-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17679-134">RELATED LINKS</span></span>

[<span data-ttu-id="17679-135">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="17679-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="17679-136">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="17679-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="17679-137">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="17679-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


