---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 3ad44ba1edcec844dcb542defb1baf294aeaa89b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574008"
---
# <span data-ttu-id="1c1cf-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="1c1cf-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="1c1cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1cf-103">Hämtar URL-adressen för enkel inloggning för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c1cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c1cf-104">SYNTAX</span></span>

### <span data-ttu-id="1c1cf-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1c1cf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c1cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c1cf-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c1cf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c1cf-107">DESCRIPTION</span></span>
<span data-ttu-id="1c1cf-108">Cmdleten **Get-AzureRmCdnProfileSsoUrl** hämtar en enkel inloggnings-URL för Azure Content Delivery Network (CDN)-profilen.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="1c1cf-109">Med den här webb adressen kan användarna Conntect till en extra Portal och använda ytterligare funktioner i CDN.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="1c1cf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c1cf-110">EXAMPLES</span></span>

## <span data-ttu-id="1c1cf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c1cf-111">PARAMETERS</span></span>

### <span data-ttu-id="1c1cf-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1c1cf-112">-CdnProfile</span></span>
<span data-ttu-id="1c1cf-113">Anger CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1cf-114">-DefaultProfile</span></span>
<span data-ttu-id="1c1cf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c1cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c1cf-116">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="1c1cf-116">-ProfileName</span></span>
<span data-ttu-id="1c1cf-117">Anger namnet på CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="1c1cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c1cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c1cf-119">Anger namnet på resurs grupp namnet som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="1c1cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1cf-120">CommonParameters</span></span>
<span data-ttu-id="1c1cf-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1cf-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c1cf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1cf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c1cf-123">INPUTS</span></span>

### <span data-ttu-id="1c1cf-124">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1c1cf-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="1c1cf-125">Parametrar: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c1cf-125">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="1c1cf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c1cf-126">OUTPUTS</span></span>

### <span data-ttu-id="1c1cf-127">Microsoft. Azure. commands. CDN. Models. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="1c1cf-127">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="1c1cf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c1cf-128">NOTES</span></span>

## <span data-ttu-id="1c1cf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c1cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="1c1cf-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1c1cf-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


