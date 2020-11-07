---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 1c9e83e8181d716024ae993ba0c3f5a9f75c6ef1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754650"
---
# <span data-ttu-id="96bae-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="96bae-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="96bae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96bae-102">SYNOPSIS</span></span>
<span data-ttu-id="96bae-103">Hämtar resursanvändningen för en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="96bae-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="96bae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96bae-104">SYNTAX</span></span>

### <span data-ttu-id="96bae-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="96bae-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96bae-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96bae-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96bae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96bae-107">DESCRIPTION</span></span>
<span data-ttu-id="96bae-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="96bae-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="96bae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96bae-109">EXAMPLES</span></span>

### <span data-ttu-id="96bae-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96bae-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="96bae-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="96bae-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="96bae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96bae-112">PARAMETERS</span></span>

### <span data-ttu-id="96bae-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="96bae-113">-CdnEndpoint</span></span>
<span data-ttu-id="96bae-114">Objektet CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="96bae-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="96bae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bae-115">-DefaultProfile</span></span>
<span data-ttu-id="96bae-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="96bae-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96bae-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="96bae-117">-EndpointName</span></span>
<span data-ttu-id="96bae-118">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="96bae-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="96bae-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="96bae-119">-ProfileName</span></span>
<span data-ttu-id="96bae-120">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="96bae-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="96bae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96bae-121">-ResourceGroupName</span></span>
<span data-ttu-id="96bae-122">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="96bae-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="96bae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bae-123">CommonParameters</span></span>
<span data-ttu-id="96bae-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96bae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bae-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96bae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bae-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96bae-126">INPUTS</span></span>

### <span data-ttu-id="96bae-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="96bae-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="96bae-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96bae-128">OUTPUTS</span></span>

### <span data-ttu-id="96bae-129">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="96bae-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="96bae-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96bae-130">NOTES</span></span>

## <span data-ttu-id="96bae-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96bae-131">RELATED LINKS</span></span>