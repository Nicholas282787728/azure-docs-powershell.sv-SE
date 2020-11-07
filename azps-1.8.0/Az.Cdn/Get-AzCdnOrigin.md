---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f770d50675cf853d84a5b1ea741d4972aaaeeca4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754644"
---
# <span data-ttu-id="7bc76-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7bc76-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="7bc76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bc76-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc76-103">Hämtar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="7bc76-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="7bc76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bc76-104">SYNTAX</span></span>

### <span data-ttu-id="7bc76-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7bc76-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bc76-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bc76-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bc76-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bc76-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc76-108">Cmdleten **Get-AzCdnOrigin** hämtar en Origine-Server och dess konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="7bc76-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="7bc76-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bc76-109">EXAMPLES</span></span>

## <span data-ttu-id="7bc76-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bc76-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc76-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc76-111">-CdnEndpoint</span></span>
<span data-ttu-id="7bc76-112">Anger det CDN-slutobjekt som ursprunget tillhör.</span><span class="sxs-lookup"><span data-stu-id="7bc76-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="7bc76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc76-113">-DefaultProfile</span></span>
<span data-ttu-id="7bc76-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7bc76-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bc76-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7bc76-115">-EndpointName</span></span>
<span data-ttu-id="7bc76-116">Anger namnet på den slut punkt som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="7bc76-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="7bc76-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="7bc76-117">-OriginName</span></span>
<span data-ttu-id="7bc76-118">Anger namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="7bc76-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="7bc76-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="7bc76-119">-ProfileName</span></span>
<span data-ttu-id="7bc76-120">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="7bc76-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="7bc76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc76-121">-ResourceGroupName</span></span>
<span data-ttu-id="7bc76-122">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="7bc76-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="7bc76-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc76-123">CommonParameters</span></span>
<span data-ttu-id="7bc76-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc76-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc76-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc76-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc76-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bc76-126">INPUTS</span></span>

### <span data-ttu-id="7bc76-127">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc76-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7bc76-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bc76-128">OUTPUTS</span></span>

### <span data-ttu-id="7bc76-129">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="7bc76-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="7bc76-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bc76-130">NOTES</span></span>

## <span data-ttu-id="7bc76-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bc76-131">RELATED LINKS</span></span>

[<span data-ttu-id="7bc76-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7bc76-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)

