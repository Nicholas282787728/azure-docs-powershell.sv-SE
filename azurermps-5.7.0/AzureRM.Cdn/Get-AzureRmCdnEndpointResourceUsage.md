---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584456"
---
# <span data-ttu-id="6e9e2-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="6e9e2-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="6e9e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9e2-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="6e9e2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e9e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e9e2-104">SYNTAX</span></span>

### <span data-ttu-id="6e9e2-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6e9e2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9e2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e9e2-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e9e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e9e2-107">DESCRIPTION</span></span>
<span data-ttu-id="6e9e2-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="6e9e2-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6e9e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e9e2-109">EXAMPLES</span></span>

### <span data-ttu-id="6e9e2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e9e2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6e9e2-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="6e9e2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="6e9e2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e9e2-112">PARAMETERS</span></span>

### <span data-ttu-id="6e9e2-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e9e2-113">-CdnEndpoint</span></span>
<span data-ttu-id="6e9e2-114">Objektet CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-114">The CDN endpoint object.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9e2-115">-DefaultProfile</span></span>
<span data-ttu-id="6e9e2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6e9e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e9e2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6e9e2-117">-EndpointName</span></span>
<span data-ttu-id="6e9e2-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-118">Azure CDN endpoint name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9e2-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="6e9e2-119">-ProfileName</span></span>
<span data-ttu-id="6e9e2-120">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-120">Azure CDN profile name.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e9e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e9e2-122">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9e2-123">CommonParameters</span></span>
<span data-ttu-id="6e9e2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9e2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9e2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e9e2-126">INPUTS</span></span>

### <span data-ttu-id="6e9e2-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e9e2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6e9e2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e9e2-128">OUTPUTS</span></span>

### <span data-ttu-id="6e9e2-129">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="6e9e2-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="6e9e2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e9e2-130">NOTES</span></span>

## <span data-ttu-id="6e9e2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e9e2-131">RELATED LINKS</span></span>

