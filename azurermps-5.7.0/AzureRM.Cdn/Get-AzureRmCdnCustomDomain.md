---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574398"
---
# <span data-ttu-id="548a2-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="548a2-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="548a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="548a2-102">SYNOPSIS</span></span>
<span data-ttu-id="548a2-103">Hämtar en anpassad CDN-domän.</span><span class="sxs-lookup"><span data-stu-id="548a2-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="548a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="548a2-104">SYNTAX</span></span>

### <span data-ttu-id="548a2-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="548a2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="548a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="548a2-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="548a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="548a2-107">DESCRIPTION</span></span>
<span data-ttu-id="548a2-108">Cmdleten **Get-AzureRmCdnCustomDomain** hämtar en anpassad domän för Azure Content Delivery Network (CDN) och dess relaterade inställningar.</span><span class="sxs-lookup"><span data-stu-id="548a2-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="548a2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="548a2-109">EXAMPLES</span></span>

## <span data-ttu-id="548a2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="548a2-110">PARAMETERS</span></span>

### <span data-ttu-id="548a2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="548a2-111">-CdnEndpoint</span></span>
<span data-ttu-id="548a2-112">Anger det CDN-slutpunkt-objekt som den anpassade domänen är medlem i.</span><span class="sxs-lookup"><span data-stu-id="548a2-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="548a2-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="548a2-113">-CustomDomainName</span></span>
<span data-ttu-id="548a2-114">Anger namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="548a2-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="548a2-115">Namnet på den anpassade domänen skiljer sig från värd namnet på den anpassade domänen.</span><span class="sxs-lookup"><span data-stu-id="548a2-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="548a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548a2-116">-DefaultProfile</span></span>
<span data-ttu-id="548a2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="548a2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="548a2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="548a2-118">-EndpointName</span></span>
<span data-ttu-id="548a2-119">Anger namnet på den slut punkt som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="548a2-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="548a2-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="548a2-120">-ProfileName</span></span>
<span data-ttu-id="548a2-121">Anger namnet på den profil som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="548a2-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="548a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="548a2-123">Anger namnet på den resurs grupp som den anpassade domänen tillhör.</span><span class="sxs-lookup"><span data-stu-id="548a2-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="548a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548a2-124">CommonParameters</span></span>
<span data-ttu-id="548a2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548a2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548a2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="548a2-127">INPUTS</span></span>

### <span data-ttu-id="548a2-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="548a2-128">PSEndpoint</span></span>
<span data-ttu-id="548a2-129">Parametern ' CdnEndpoint ' godkänner värdet av typen ' PSEndpoint ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="548a2-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="548a2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="548a2-130">OUTPUTS</span></span>

###  
<span data-ttu-id="548a2-131">Denna cmdlet returnerar ett anpassat domän objekt.</span><span class="sxs-lookup"><span data-stu-id="548a2-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="548a2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="548a2-132">NOTES</span></span>

## <span data-ttu-id="548a2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="548a2-133">RELATED LINKS</span></span>

[<span data-ttu-id="548a2-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="548a2-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="548a2-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="548a2-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


