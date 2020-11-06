---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586216"
---
# <span data-ttu-id="7e307-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7e307-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="7e307-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e307-102">SYNOPSIS</span></span>
<span data-ttu-id="7e307-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="7e307-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e307-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e307-104">SYNTAX</span></span>

### <span data-ttu-id="7e307-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="7e307-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e307-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="7e307-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e307-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e307-107">DESCRIPTION</span></span>
<span data-ttu-id="7e307-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="7e307-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7e307-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e307-109">EXAMPLES</span></span>

### <span data-ttu-id="7e307-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e307-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7e307-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="7e307-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7e307-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e307-112">PARAMETERS</span></span>

### <span data-ttu-id="7e307-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e307-113">-CdnEndpoint</span></span>
<span data-ttu-id="7e307-114">Objektet CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7e307-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e307-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7e307-115">-EndpointName</span></span>
<span data-ttu-id="7e307-116">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7e307-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e307-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7e307-117">-ProfileName</span></span>
<span data-ttu-id="7e307-118">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="7e307-118">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e307-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e307-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e307-120">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="7e307-120">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e307-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e307-121">-DefaultProfile</span></span>
<span data-ttu-id="7e307-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e307-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e307-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e307-123">CommonParameters</span></span>
<span data-ttu-id="7e307-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e307-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e307-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e307-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e307-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e307-126">INPUTS</span></span>

### <span data-ttu-id="7e307-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e307-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7e307-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e307-128">OUTPUTS</span></span>

### <span data-ttu-id="7e307-129">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7e307-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="7e307-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e307-130">NOTES</span></span>

## <span data-ttu-id="7e307-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e307-131">RELATED LINKS</span></span>

