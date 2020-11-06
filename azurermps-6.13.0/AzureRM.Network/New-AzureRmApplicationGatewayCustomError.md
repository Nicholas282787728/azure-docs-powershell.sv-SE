---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582591"
---
# <span data-ttu-id="53ca7-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="53ca7-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="53ca7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="53ca7-103">Skapar ett anpassat fel med HTTP-statuskod och URL-adressen för anpassad sida</span><span class="sxs-lookup"><span data-stu-id="53ca7-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53ca7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53ca7-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ca7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53ca7-105">DESCRIPTION</span></span>
<span data-ttu-id="53ca7-106">Cmdleten **New-AzureRmApplicationGatewayCustomError** skapar ett anpassat fel.</span><span class="sxs-lookup"><span data-stu-id="53ca7-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="53ca7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53ca7-107">EXAMPLES</span></span>

### <span data-ttu-id="53ca7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53ca7-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="53ca7-109">Det här kommandot skapar det anpassade felet hos HTTP-statuskod 403.</span><span class="sxs-lookup"><span data-stu-id="53ca7-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="53ca7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="53ca7-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="53ca7-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="53ca7-112">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="53ca7-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ca7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ca7-113">-DefaultProfile</span></span>
<span data-ttu-id="53ca7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53ca7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53ca7-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="53ca7-115">-StatusCode</span></span>
<span data-ttu-id="53ca7-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="53ca7-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ca7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ca7-117">CommonParameters</span></span>
<span data-ttu-id="53ca7-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ca7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53ca7-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ca7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ca7-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53ca7-120">INPUTS</span></span>

### <span data-ttu-id="53ca7-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="53ca7-121">None</span></span>

## <span data-ttu-id="53ca7-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53ca7-122">OUTPUTS</span></span>

### <span data-ttu-id="53ca7-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="53ca7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="53ca7-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53ca7-124">NOTES</span></span>

## <span data-ttu-id="53ca7-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53ca7-125">RELATED LINKS</span></span>
