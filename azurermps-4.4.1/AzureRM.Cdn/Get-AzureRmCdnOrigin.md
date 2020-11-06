---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586223"
---
# <span data-ttu-id="a8b7f-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a8b7f-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="a8b7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b7f-103">Hämtar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8b7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8b7f-104">SYNTAX</span></span>

### <span data-ttu-id="a8b7f-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="a8b7f-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8b7f-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="a8b7f-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8b7f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="a8b7f-108">Cmdleten **Get-AzureRmCdnOrigin** hämtar en Origine-Server och dess konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="a8b7f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8b7f-109">EXAMPLES</span></span>

## <span data-ttu-id="a8b7f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="a8b7f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8b7f-111">-CdnEndpoint</span></span>
<span data-ttu-id="a8b7f-112">Anger det CDN-slutobjekt som ursprunget tillhör.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="a8b7f-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a8b7f-113">-EndpointName</span></span>
<span data-ttu-id="a8b7f-114">Anger namnet på den slut punkt som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a8b7f-115">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a8b7f-115">-OriginName</span></span>
<span data-ttu-id="a8b7f-116">Anger namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-116">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="a8b7f-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="a8b7f-117">-ProfileName</span></span>
<span data-ttu-id="a8b7f-118">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-118">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a8b7f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b7f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8b7f-120">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a8b7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b7f-121">-DefaultProfile</span></span>
<span data-ttu-id="a8b7f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8b7f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b7f-123">CommonParameters</span></span>
<span data-ttu-id="a8b7f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b7f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b7f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b7f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8b7f-126">INPUTS</span></span>

### <span data-ttu-id="a8b7f-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8b7f-127">PSEndpoint</span></span>
<span data-ttu-id="a8b7f-128">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a8b7f-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a8b7f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8b7f-129">OUTPUTS</span></span>

###  
<span data-ttu-id="a8b7f-130">Denna cmdlet returnerar ett Origine Server-objekt.</span><span class="sxs-lookup"><span data-stu-id="a8b7f-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="a8b7f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8b7f-131">NOTES</span></span>

## <span data-ttu-id="a8b7f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8b7f-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8b7f-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a8b7f-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


