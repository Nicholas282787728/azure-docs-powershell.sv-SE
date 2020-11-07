---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756296"
---
# <span data-ttu-id="ab3d3-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="ab3d3-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="ab3d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3d3-103">Lägger till ett API till en produkt.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab3d3-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab3d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3d3-106">Cmdleten **Add-AzureRmApiManagementApiToProduct** lägger till ett API för Azure API-hantering till en produkt.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="ab3d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab3d3-107">EXAMPLES</span></span>

### <span data-ttu-id="ab3d3-108">Exempel 1: lägga till ett API till en produkt</span><span class="sxs-lookup"><span data-stu-id="ab3d3-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="ab3d3-109">Det här kommandot lägger till angivet API till den angivna produkten.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="ab3d3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab3d3-110">PARAMETERS</span></span>

### <span data-ttu-id="ab3d3-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ab3d3-111">-ApiId</span></span>
<span data-ttu-id="ab3d3-112">Anger ID för ett API att lägga till i en produkt.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3d3-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ab3d3-113">-Context</span></span>
<span data-ttu-id="ab3d3-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab3d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3d3-115">-DefaultProfile</span></span>
<span data-ttu-id="ab3d3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab3d3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab3d3-117">-PassThru</span></span>
<span data-ttu-id="ab3d3-118">passthru</span><span class="sxs-lookup"><span data-stu-id="ab3d3-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3d3-119">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="ab3d3-119">-ProductId</span></span>
<span data-ttu-id="ab3d3-120">Anger ID: t för den produkt som du vill lägga till API: t.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3d3-121">CommonParameters</span></span>
<span data-ttu-id="ab3d3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3d3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3d3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3d3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab3d3-124">INPUTS</span></span>

### <span data-ttu-id="ab3d3-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="ab3d3-125">None</span></span>
<span data-ttu-id="ab3d3-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ab3d3-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab3d3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab3d3-127">OUTPUTS</span></span>

### <span data-ttu-id="ab3d3-128">Returtyp</span><span class="sxs-lookup"><span data-stu-id="ab3d3-128">Boolean</span></span>

## <span data-ttu-id="ab3d3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab3d3-129">NOTES</span></span>

## <span data-ttu-id="ab3d3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab3d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab3d3-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="ab3d3-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


