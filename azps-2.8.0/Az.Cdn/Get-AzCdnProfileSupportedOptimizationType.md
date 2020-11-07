---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: 141f5b87807d2ad60f1dbe8555629bc3e117605d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745322"
---
# <span data-ttu-id="f6f6f-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="f6f6f-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="f6f6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f6f-103">Hämtar optimerings typerna som stöds för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="f6f6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6f6f-104">SYNTAX</span></span>

### <span data-ttu-id="f6f6f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f6f6f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6f6f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6f6f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f6f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6f6f-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f6f-108">Cmdleten **Get-AzCdnProfileSupportedOptimizationType** får optimerings typerna som stöds för den aktuella profilen.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="f6f6f-109">En användare kan skapa en slut punkt med en optimerings typ från värdena i listan.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="f6f6f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6f6f-110">EXAMPLES</span></span>

### <span data-ttu-id="f6f6f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6f6f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="f6f6f-112">Få optimerings typer som stöds för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="f6f6f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6f6f-113">PARAMETERS</span></span>

### <span data-ttu-id="f6f6f-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f6f6f-114">-CdnProfile</span></span>
<span data-ttu-id="f6f6f-115">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="f6f6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f6f-116">-DefaultProfile</span></span>
<span data-ttu-id="f6f6f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f6f-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="f6f6f-118">-ProfileName</span></span>
<span data-ttu-id="f6f6f-119">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-119">The name of the profile.</span></span>

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

### <span data-ttu-id="f6f6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6f6f-121">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f6f6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f6f-122">CommonParameters</span></span>
<span data-ttu-id="f6f6f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f6f-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f6f-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f6f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6f6f-125">INPUTS</span></span>

### <span data-ttu-id="f6f6f-126">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f6f6f-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f6f6f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6f6f-127">OUTPUTS</span></span>

### <span data-ttu-id="f6f6f-128">Microsoft. Azure. commands. CDN. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="f6f6f-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="f6f6f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6f6f-129">NOTES</span></span>

## <span data-ttu-id="f6f6f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6f6f-130">RELATED LINKS</span></span>
