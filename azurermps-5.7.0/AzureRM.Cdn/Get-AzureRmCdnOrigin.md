---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755401"
---
# <span data-ttu-id="af2de-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af2de-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="af2de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af2de-102">SYNOPSIS</span></span>
<span data-ttu-id="af2de-103">Hämtar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="af2de-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af2de-104">SYNTAX</span></span>

### <span data-ttu-id="af2de-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="af2de-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af2de-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af2de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af2de-107">DESCRIPTION</span></span>
<span data-ttu-id="af2de-108">Cmdleten **Get-AzureRmCdnOrigin** hämtar en Origine-Server och dess konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="af2de-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="af2de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af2de-109">EXAMPLES</span></span>

## <span data-ttu-id="af2de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af2de-110">PARAMETERS</span></span>

### <span data-ttu-id="af2de-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af2de-111">-CdnEndpoint</span></span>
<span data-ttu-id="af2de-112">Anger det CDN-slutobjekt som ursprunget tillhör.</span><span class="sxs-lookup"><span data-stu-id="af2de-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="af2de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2de-113">-DefaultProfile</span></span>
<span data-ttu-id="af2de-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af2de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af2de-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af2de-115">-EndpointName</span></span>
<span data-ttu-id="af2de-116">Anger namnet på den slut punkt som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="af2de-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="af2de-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="af2de-117">-OriginName</span></span>
<span data-ttu-id="af2de-118">Anger namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="af2de-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="af2de-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="af2de-119">-ProfileName</span></span>
<span data-ttu-id="af2de-120">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="af2de-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="af2de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2de-121">-ResourceGroupName</span></span>
<span data-ttu-id="af2de-122">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="af2de-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="af2de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2de-123">CommonParameters</span></span>
<span data-ttu-id="af2de-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af2de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2de-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2de-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2de-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af2de-126">INPUTS</span></span>

### <span data-ttu-id="af2de-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="af2de-127">PSEndpoint</span></span>
<span data-ttu-id="af2de-128">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="af2de-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="af2de-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af2de-129">OUTPUTS</span></span>

###  
<span data-ttu-id="af2de-130">Denna cmdlet returnerar ett Origine Server-objekt.</span><span class="sxs-lookup"><span data-stu-id="af2de-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="af2de-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af2de-131">NOTES</span></span>

## <span data-ttu-id="af2de-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af2de-132">RELATED LINKS</span></span>

[<span data-ttu-id="af2de-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="af2de-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


