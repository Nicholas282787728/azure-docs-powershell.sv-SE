---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262123"
---
# <span data-ttu-id="65a3e-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="65a3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="65a3e-103">Skapar ett anpassat fel med HTTP-statuskod och URL-adressen för anpassad sida</span><span class="sxs-lookup"><span data-stu-id="65a3e-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="65a3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65a3e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="65a3e-106">Cmdleten **New-AzApplicationGatewayCustomError** skapar ett anpassat fel.</span><span class="sxs-lookup"><span data-stu-id="65a3e-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="65a3e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65a3e-107">EXAMPLES</span></span>

### <span data-ttu-id="65a3e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65a3e-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="65a3e-109">Det här kommandot skapar det anpassade felet hos HTTP-statuskod 403.</span><span class="sxs-lookup"><span data-stu-id="65a3e-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="65a3e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65a3e-110">PARAMETERS</span></span>

### <span data-ttu-id="65a3e-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="65a3e-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="65a3e-112">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="65a3e-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a3e-113">-DefaultProfile</span></span>
<span data-ttu-id="65a3e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65a3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65a3e-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="65a3e-115">-StatusCode</span></span>
<span data-ttu-id="65a3e-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="65a3e-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a3e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a3e-117">CommonParameters</span></span>
<span data-ttu-id="65a3e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a3e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a3e-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a3e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a3e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65a3e-120">INPUTS</span></span>

### <span data-ttu-id="65a3e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="65a3e-121">None</span></span>

## <span data-ttu-id="65a3e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65a3e-122">OUTPUTS</span></span>

### <span data-ttu-id="65a3e-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="65a3e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65a3e-124">NOTES</span></span>

## <span data-ttu-id="65a3e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65a3e-125">RELATED LINKS</span></span>

[<span data-ttu-id="65a3e-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="65a3e-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="65a3e-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="65a3e-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65a3e-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
