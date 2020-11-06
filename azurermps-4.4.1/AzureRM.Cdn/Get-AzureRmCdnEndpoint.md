---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581507"
---
# <span data-ttu-id="31b63-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="31b63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31b63-102">SYNOPSIS</span></span>
<span data-ttu-id="31b63-103">Hämtar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="31b63-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31b63-104">SYNTAX</span></span>

### <span data-ttu-id="31b63-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="31b63-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b63-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="31b63-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b63-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31b63-107">DESCRIPTION</span></span>
<span data-ttu-id="31b63-108">Cmdleten **Get-AzureRMCdnEndpoint** hämtar en CDN-slutpunkt (Azure Content Delivery Network) och dess tillhör ande konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="31b63-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="31b63-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31b63-109">EXAMPLES</span></span>

## <span data-ttu-id="31b63-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31b63-110">PARAMETERS</span></span>

### <span data-ttu-id="31b63-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="31b63-111">-CdnProfile</span></span>
<span data-ttu-id="31b63-112">Anger det CDN-profil objekt som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="31b63-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b63-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="31b63-113">-EndpointName</span></span>
<span data-ttu-id="31b63-114">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="31b63-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="31b63-115">Namnet på slut punkten är inte slut punktens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="31b63-115">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="31b63-116">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="31b63-116">-ProfileName</span></span>
<span data-ttu-id="31b63-117">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="31b63-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="31b63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b63-118">-ResourceGroupName</span></span>
<span data-ttu-id="31b63-119">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="31b63-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="31b63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b63-120">-DefaultProfile</span></span>
<span data-ttu-id="31b63-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31b63-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b63-122">CommonParameters</span></span>
<span data-ttu-id="31b63-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b63-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b63-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31b63-125">INPUTS</span></span>

### <span data-ttu-id="31b63-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="31b63-126">PSProfile</span></span>
<span data-ttu-id="31b63-127">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="31b63-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="31b63-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31b63-128">OUTPUTS</span></span>

###  
<span data-ttu-id="31b63-129">Denna cmdlet returnerar ett objekt av slut punkten.</span><span class="sxs-lookup"><span data-stu-id="31b63-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="31b63-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31b63-130">NOTES</span></span>

## <span data-ttu-id="31b63-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31b63-131">RELATED LINKS</span></span>

[<span data-ttu-id="31b63-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="31b63-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="31b63-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="31b63-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="31b63-136">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b63-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


