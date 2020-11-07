---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 64e9c4bc8f279858c4c889c00eee058aab0cad4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917573"
---
# <span data-ttu-id="69d65-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="69d65-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="69d65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69d65-102">SYNOPSIS</span></span>
<span data-ttu-id="69d65-103">Hämtar URL-adressen för enkel inloggning för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="69d65-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="69d65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69d65-104">SYNTAX</span></span>

### <span data-ttu-id="69d65-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="69d65-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69d65-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69d65-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d65-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69d65-107">DESCRIPTION</span></span>
<span data-ttu-id="69d65-108">Cmdleten **Get-AzCdnProfileSsoUrl** hämtar en enkel inloggnings-URL för Azure Content Delivery Network (CDN)-profilen.</span><span class="sxs-lookup"><span data-stu-id="69d65-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="69d65-109">Med den här webb adressen kan användarna Conntect till en extra Portal och använda ytterligare funktioner i CDN.</span><span class="sxs-lookup"><span data-stu-id="69d65-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="69d65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69d65-110">EXAMPLES</span></span>

## <span data-ttu-id="69d65-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69d65-111">PARAMETERS</span></span>

### <span data-ttu-id="69d65-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="69d65-112">-CdnProfile</span></span>
<span data-ttu-id="69d65-113">Anger CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="69d65-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="69d65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d65-114">-DefaultProfile</span></span>
<span data-ttu-id="69d65-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69d65-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69d65-116">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="69d65-116">-ProfileName</span></span>
<span data-ttu-id="69d65-117">Anger namnet på CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="69d65-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="69d65-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69d65-118">-ResourceGroupName</span></span>
<span data-ttu-id="69d65-119">Anger namnet på resurs grupp namnet som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="69d65-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="69d65-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d65-120">CommonParameters</span></span>
<span data-ttu-id="69d65-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d65-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d65-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d65-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d65-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69d65-123">INPUTS</span></span>

### <span data-ttu-id="69d65-124">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="69d65-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="69d65-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69d65-125">OUTPUTS</span></span>

### <span data-ttu-id="69d65-126">Microsoft. Azure. commands. CDN. Models. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="69d65-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="69d65-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69d65-127">NOTES</span></span>

## <span data-ttu-id="69d65-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69d65-128">RELATED LINKS</span></span>

[<span data-ttu-id="69d65-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69d65-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


