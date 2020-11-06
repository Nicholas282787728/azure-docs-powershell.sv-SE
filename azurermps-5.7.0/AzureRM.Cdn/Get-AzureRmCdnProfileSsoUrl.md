---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: d93dadc062f2cc12ed363039d69266daf365920e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574391"
---
# <span data-ttu-id="92029-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="92029-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="92029-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92029-102">SYNOPSIS</span></span>
<span data-ttu-id="92029-103">Hämtar URL-adressen för enkel inloggning för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="92029-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92029-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92029-104">SYNTAX</span></span>

### <span data-ttu-id="92029-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="92029-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92029-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92029-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92029-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92029-107">DESCRIPTION</span></span>
<span data-ttu-id="92029-108">Cmdleten **Get-AzureRmCdnProfileSsoUrl** hämtar en enkel inloggnings-URL för Azure Content Delivery Network (CDN)-profilen.</span><span class="sxs-lookup"><span data-stu-id="92029-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="92029-109">Med den här webb adressen kan användarna Conntect till en extra Portal och använda ytterligare funktioner i CDN.</span><span class="sxs-lookup"><span data-stu-id="92029-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="92029-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92029-110">EXAMPLES</span></span>

## <span data-ttu-id="92029-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92029-111">PARAMETERS</span></span>

### <span data-ttu-id="92029-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="92029-112">-CdnProfile</span></span>
<span data-ttu-id="92029-113">Anger CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="92029-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="92029-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92029-114">-DefaultProfile</span></span>
<span data-ttu-id="92029-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="92029-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92029-116">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="92029-116">-ProfileName</span></span>
<span data-ttu-id="92029-117">Anger namnet på CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="92029-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="92029-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92029-118">-ResourceGroupName</span></span>
<span data-ttu-id="92029-119">Anger namnet på resurs grupp namnet som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="92029-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="92029-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92029-120">CommonParameters</span></span>
<span data-ttu-id="92029-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92029-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92029-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92029-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92029-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92029-123">INPUTS</span></span>

### <span data-ttu-id="92029-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="92029-124">PSProfile</span></span>
<span data-ttu-id="92029-125">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="92029-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="92029-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92029-126">OUTPUTS</span></span>

###  
<span data-ttu-id="92029-127">Denna cmdlet returnerar en URL.</span><span class="sxs-lookup"><span data-stu-id="92029-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="92029-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92029-128">NOTES</span></span>

## <span data-ttu-id="92029-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92029-129">RELATED LINKS</span></span>

[<span data-ttu-id="92029-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="92029-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


