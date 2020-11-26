---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272768"
---
# <span data-ttu-id="5447c-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="5447c-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="5447c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5447c-102">SYNOPSIS</span></span>
<span data-ttu-id="5447c-103">Hämtar resursanvändningen för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5447c-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="5447c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5447c-104">SYNTAX</span></span>

### <span data-ttu-id="5447c-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5447c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5447c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5447c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5447c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5447c-107">DESCRIPTION</span></span>
<span data-ttu-id="5447c-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="5447c-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5447c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5447c-109">EXAMPLES</span></span>

### <span data-ttu-id="5447c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5447c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5447c-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="5447c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="5447c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5447c-112">PARAMETERS</span></span>

### <span data-ttu-id="5447c-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5447c-113">-CdnEndpoint</span></span>
<span data-ttu-id="5447c-114">Objektet CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5447c-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5447c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5447c-115">-DefaultProfile</span></span>
<span data-ttu-id="5447c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5447c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5447c-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5447c-117">-EndpointName</span></span>
<span data-ttu-id="5447c-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="5447c-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="5447c-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="5447c-119">-ProfileName</span></span>
<span data-ttu-id="5447c-120">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="5447c-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5447c-121">-ResourceGroupName</span></span>
<span data-ttu-id="5447c-122">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="5447c-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5447c-123">CommonParameters</span></span>
<span data-ttu-id="5447c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5447c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5447c-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5447c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5447c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5447c-126">INPUTS</span></span>

### <span data-ttu-id="5447c-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5447c-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5447c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5447c-128">OUTPUTS</span></span>

### <span data-ttu-id="5447c-129">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="5447c-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="5447c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5447c-130">NOTES</span></span>

## <span data-ttu-id="5447c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5447c-131">RELATED LINKS</span></span>