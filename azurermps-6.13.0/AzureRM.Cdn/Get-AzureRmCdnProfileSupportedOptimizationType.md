---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581771"
---
# <span data-ttu-id="79a0b-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="79a0b-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="79a0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="79a0b-103">Hämtar optimerings typerna som stöds för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="79a0b-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79a0b-104">SYNTAX</span></span>

### <span data-ttu-id="79a0b-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="79a0b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79a0b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a0b-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79a0b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79a0b-107">DESCRIPTION</span></span>
<span data-ttu-id="79a0b-108">Cmdleten **Get-AzureRmCdnProfileSupportedOptimizationType** får optimerings typerna som stöds för den aktuella profilen.</span><span class="sxs-lookup"><span data-stu-id="79a0b-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="79a0b-109">En användare kan skapa en slut punkt med en optimerings typ från värdena i listan.</span><span class="sxs-lookup"><span data-stu-id="79a0b-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="79a0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79a0b-110">EXAMPLES</span></span>

### <span data-ttu-id="79a0b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79a0b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="79a0b-112">Få optimerings typer som stöds för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="79a0b-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="79a0b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79a0b-113">PARAMETERS</span></span>

### <span data-ttu-id="79a0b-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="79a0b-114">-CdnProfile</span></span>
<span data-ttu-id="79a0b-115">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="79a0b-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="79a0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a0b-116">-DefaultProfile</span></span>
<span data-ttu-id="79a0b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79a0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a0b-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="79a0b-118">-ProfileName</span></span>
<span data-ttu-id="79a0b-119">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="79a0b-119">The name of the profile.</span></span>

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

### <span data-ttu-id="79a0b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a0b-120">-ResourceGroupName</span></span>
<span data-ttu-id="79a0b-121">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="79a0b-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="79a0b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a0b-122">CommonParameters</span></span>
<span data-ttu-id="79a0b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a0b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a0b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a0b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a0b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79a0b-125">INPUTS</span></span>

### <span data-ttu-id="79a0b-126">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="79a0b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="79a0b-127">Parametrar: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79a0b-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="79a0b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79a0b-128">OUTPUTS</span></span>

### <span data-ttu-id="79a0b-129">Microsoft. Azure. commands. CDN. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="79a0b-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="79a0b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79a0b-130">NOTES</span></span>

## <span data-ttu-id="79a0b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79a0b-131">RELATED LINKS</span></span>
