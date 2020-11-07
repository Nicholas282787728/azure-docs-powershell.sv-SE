---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: e32d8312d0046786e6fd36ce30e525241fe78c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745323"
---
# <span data-ttu-id="bcaf0-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="bcaf0-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="bcaf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcaf0-103">Hämtar URL-adressen för enkel inloggning för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="bcaf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcaf0-104">SYNTAX</span></span>

### <span data-ttu-id="bcaf0-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bcaf0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcaf0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcaf0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcaf0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcaf0-107">DESCRIPTION</span></span>
<span data-ttu-id="bcaf0-108">Cmdleten **Get-AzCdnProfileSsoUrl** hämtar en enkel inloggnings-URL för Azure Content Delivery Network (CDN)-profilen.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="bcaf0-109">Med den här webb adressen kan användarna ansluta till en extra Portal och använda ytterligare funktioner i CDN.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="bcaf0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcaf0-110">EXAMPLES</span></span>

## <span data-ttu-id="bcaf0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcaf0-111">PARAMETERS</span></span>

### <span data-ttu-id="bcaf0-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="bcaf0-112">-CdnProfile</span></span>
<span data-ttu-id="bcaf0-113">Anger CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="bcaf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcaf0-114">-DefaultProfile</span></span>
<span data-ttu-id="bcaf0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bcaf0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcaf0-116">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="bcaf0-116">-ProfileName</span></span>
<span data-ttu-id="bcaf0-117">Anger namnet på CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="bcaf0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcaf0-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcaf0-119">Anger namnet på resurs grupp namnet som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="bcaf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcaf0-120">CommonParameters</span></span>
<span data-ttu-id="bcaf0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcaf0-122">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcaf0-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcaf0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcaf0-123">INPUTS</span></span>

### <span data-ttu-id="bcaf0-124">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="bcaf0-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="bcaf0-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcaf0-125">OUTPUTS</span></span>

### <span data-ttu-id="bcaf0-126">Microsoft. Azure. commands. CDN. Models. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="bcaf0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="bcaf0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcaf0-127">NOTES</span></span>

## <span data-ttu-id="bcaf0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcaf0-128">RELATED LINKS</span></span>

[<span data-ttu-id="bcaf0-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="bcaf0-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

