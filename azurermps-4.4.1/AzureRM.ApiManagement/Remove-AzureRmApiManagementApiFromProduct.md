---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573771"
---
# <span data-ttu-id="2512d-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="2512d-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="2512d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2512d-102">SYNOPSIS</span></span>
<span data-ttu-id="2512d-103">Tar bort ett API från en produkt.</span><span class="sxs-lookup"><span data-stu-id="2512d-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2512d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2512d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2512d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2512d-105">DESCRIPTION</span></span>
<span data-ttu-id="2512d-106">Cmdleten **Remove-AzureRmApiManagementApiFromProduct** tar bort ett API för Azure API-hantering från en produkt.</span><span class="sxs-lookup"><span data-stu-id="2512d-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="2512d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2512d-107">EXAMPLES</span></span>

### <span data-ttu-id="2512d-108">Exempel 1: ta bort ett API från en produkt</span><span class="sxs-lookup"><span data-stu-id="2512d-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="2512d-109">Denna commnd tar bort det angivna API: t från en produkt.</span><span class="sxs-lookup"><span data-stu-id="2512d-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="2512d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2512d-110">PARAMETERS</span></span>

### <span data-ttu-id="2512d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2512d-111">-ApiId</span></span>
<span data-ttu-id="2512d-112">Anger ID för det API som ska tas bort från produkten.</span><span class="sxs-lookup"><span data-stu-id="2512d-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="2512d-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2512d-113">-Context</span></span>
<span data-ttu-id="2512d-114">Anger en **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="2512d-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="2512d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2512d-115">-PassThru</span></span>
<span data-ttu-id="2512d-116">Anger att denna cmdlet returnerar ett värde för $True om det lyckas eller $False.</span><span class="sxs-lookup"><span data-stu-id="2512d-116">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="2512d-117">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="2512d-117">-ProductId</span></span>
<span data-ttu-id="2512d-118">Anger ID för den produkt som API: t ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="2512d-118">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="2512d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2512d-119">-DefaultProfile</span></span>
<span data-ttu-id="2512d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2512d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2512d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2512d-121">CommonParameters</span></span>
<span data-ttu-id="2512d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2512d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2512d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2512d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2512d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2512d-124">INPUTS</span></span>

## <span data-ttu-id="2512d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2512d-125">OUTPUTS</span></span>

### <span data-ttu-id="2512d-126">bool</span><span class="sxs-lookup"><span data-stu-id="2512d-126">bool</span></span>

## <span data-ttu-id="2512d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2512d-127">NOTES</span></span>

## <span data-ttu-id="2512d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2512d-128">RELATED LINKS</span></span>

[<span data-ttu-id="2512d-129">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="2512d-129">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


