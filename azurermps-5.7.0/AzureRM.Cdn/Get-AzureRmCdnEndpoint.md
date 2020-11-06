---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574394"
---
# <span data-ttu-id="57748-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="57748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57748-102">SYNOPSIS</span></span>
<span data-ttu-id="57748-103">Hämtar en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="57748-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57748-104">SYNTAX</span></span>

### <span data-ttu-id="57748-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="57748-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57748-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57748-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57748-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57748-107">DESCRIPTION</span></span>
<span data-ttu-id="57748-108">Cmdleten **Get-AzureRMCdnEndpoint** hämtar en CDN-slutpunkt (Azure Content Delivery Network) och dess tillhör ande konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="57748-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="57748-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57748-109">EXAMPLES</span></span>

## <span data-ttu-id="57748-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57748-110">PARAMETERS</span></span>

### <span data-ttu-id="57748-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="57748-111">-CdnProfile</span></span>
<span data-ttu-id="57748-112">Anger det CDN-profil objekt som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="57748-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57748-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57748-113">-DefaultProfile</span></span>
<span data-ttu-id="57748-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57748-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57748-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="57748-115">-EndpointName</span></span>
<span data-ttu-id="57748-116">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="57748-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="57748-117">Namnet på slut punkten är inte slut punktens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="57748-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="57748-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="57748-118">-ProfileName</span></span>
<span data-ttu-id="57748-119">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="57748-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="57748-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57748-120">-ResourceGroupName</span></span>
<span data-ttu-id="57748-121">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="57748-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="57748-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57748-122">CommonParameters</span></span>
<span data-ttu-id="57748-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57748-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57748-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57748-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57748-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57748-125">INPUTS</span></span>

### <span data-ttu-id="57748-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="57748-126">PSProfile</span></span>
<span data-ttu-id="57748-127">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="57748-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="57748-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57748-128">OUTPUTS</span></span>

###  
<span data-ttu-id="57748-129">Denna cmdlet returnerar ett objekt av slut punkten.</span><span class="sxs-lookup"><span data-stu-id="57748-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="57748-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57748-130">NOTES</span></span>

## <span data-ttu-id="57748-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57748-131">RELATED LINKS</span></span>

[<span data-ttu-id="57748-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="57748-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="57748-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="57748-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="57748-136">Stopp-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="57748-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


