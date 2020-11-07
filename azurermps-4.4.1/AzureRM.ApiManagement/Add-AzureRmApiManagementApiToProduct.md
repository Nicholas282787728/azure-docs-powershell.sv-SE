---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756645"
---
# <span data-ttu-id="0e8e8-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="0e8e8-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="0e8e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8e8-103">Lägger till ett API till en produkt.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e8e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e8e8-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e8e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e8e8-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8e8-106">Cmdleten **Add-AzureRmApiManagementApiToProduct** lägger till ett API för Azure API-hantering till en produkt.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="0e8e8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e8e8-107">EXAMPLES</span></span>

### <span data-ttu-id="0e8e8-108">Exempel 1: lägga till ett API till en produkt</span><span class="sxs-lookup"><span data-stu-id="0e8e8-108">Example 1: Add an API to a product</span></span>
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="0e8e8-109">Det här kommandot lägger till angivet API till den angivna produkten.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="0e8e8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e8e8-110">PARAMETERS</span></span>

### <span data-ttu-id="0e8e8-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0e8e8-111">-ApiId</span></span>
<span data-ttu-id="0e8e8-112">Anger ID för ett API att lägga till i en produkt.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e8-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0e8e8-113">-Context</span></span>
<span data-ttu-id="0e8e8-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0e8e8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e8e8-115">-PassThru</span></span>
<span data-ttu-id="0e8e8-116">passthru</span><span class="sxs-lookup"><span data-stu-id="0e8e8-116">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e8-117">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="0e8e8-117">-ProductId</span></span>
<span data-ttu-id="0e8e8-118">Anger ID: t för den produkt som du vill lägga till API: t.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-118">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8e8-119">-DefaultProfile</span></span>
<span data-ttu-id="0e8e8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e8e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8e8-121">CommonParameters</span></span>
<span data-ttu-id="0e8e8-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8e8-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8e8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8e8-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e8e8-124">INPUTS</span></span>

## <span data-ttu-id="0e8e8-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e8e8-125">OUTPUTS</span></span>

### <span data-ttu-id="0e8e8-126">Returtyp</span><span class="sxs-lookup"><span data-stu-id="0e8e8-126">Boolean</span></span>

## <span data-ttu-id="0e8e8-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e8e8-127">NOTES</span></span>

## <span data-ttu-id="0e8e8-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e8e8-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e8e8-129">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="0e8e8-129">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


