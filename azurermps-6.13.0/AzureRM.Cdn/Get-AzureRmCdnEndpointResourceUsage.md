---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578107"
---
# <span data-ttu-id="917ce-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="917ce-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="917ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="917ce-102">SYNOPSIS</span></span>
<span data-ttu-id="917ce-103">Hämtar resursanvändningen för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="917ce-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="917ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="917ce-104">SYNTAX</span></span>

### <span data-ttu-id="917ce-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="917ce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="917ce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="917ce-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="917ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="917ce-107">DESCRIPTION</span></span>
<span data-ttu-id="917ce-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="917ce-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="917ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="917ce-109">EXAMPLES</span></span>

### <span data-ttu-id="917ce-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="917ce-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="917ce-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="917ce-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="917ce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="917ce-112">PARAMETERS</span></span>

### <span data-ttu-id="917ce-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="917ce-113">-CdnEndpoint</span></span>
<span data-ttu-id="917ce-114">Objektet CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="917ce-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="917ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917ce-115">-DefaultProfile</span></span>
<span data-ttu-id="917ce-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="917ce-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="917ce-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="917ce-117">-EndpointName</span></span>
<span data-ttu-id="917ce-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="917ce-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="917ce-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="917ce-119">-ProfileName</span></span>
<span data-ttu-id="917ce-120">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="917ce-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="917ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="917ce-122">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="917ce-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="917ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917ce-123">CommonParameters</span></span>
<span data-ttu-id="917ce-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917ce-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917ce-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="917ce-126">INPUTS</span></span>

### <span data-ttu-id="917ce-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="917ce-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="917ce-128">Parametrar: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="917ce-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="917ce-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="917ce-129">OUTPUTS</span></span>

### <span data-ttu-id="917ce-130">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="917ce-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="917ce-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="917ce-131">NOTES</span></span>

## <span data-ttu-id="917ce-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="917ce-132">RELATED LINKS</span></span>
