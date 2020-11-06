---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 6cc9b19f892ed15caf675b22935328354fa47dcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584452"
---
# <span data-ttu-id="e0ce5-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e0ce5-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="e0ce5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ce5-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="e0ce5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ce5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0ce5-104">SYNTAX</span></span>

### <span data-ttu-id="e0ce5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e0ce5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ce5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ce5-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ce5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0ce5-107">DESCRIPTION</span></span>
<span data-ttu-id="e0ce5-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="e0ce5-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e0ce5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0ce5-109">EXAMPLES</span></span>

### <span data-ttu-id="e0ce5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0ce5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e0ce5-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="e0ce5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e0ce5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0ce5-112">PARAMETERS</span></span>

### <span data-ttu-id="e0ce5-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0ce5-113">-CdnProfile</span></span>
<span data-ttu-id="e0ce5-114">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="e0ce5-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="e0ce5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ce5-115">-DefaultProfile</span></span>
<span data-ttu-id="e0ce5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0ce5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0ce5-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="e0ce5-117">-ProfileName</span></span>
<span data-ttu-id="e0ce5-118">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="e0ce5-118">The name of the profile.</span></span>

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

### <span data-ttu-id="e0ce5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ce5-119">-ResourceGroupName</span></span>
<span data-ttu-id="e0ce5-120">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e0ce5-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e0ce5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ce5-121">CommonParameters</span></span>
<span data-ttu-id="e0ce5-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ce5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ce5-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ce5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ce5-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0ce5-124">INPUTS</span></span>

### <span data-ttu-id="e0ce5-125">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e0ce5-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e0ce5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0ce5-126">OUTPUTS</span></span>

### <span data-ttu-id="e0ce5-127">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e0ce5-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e0ce5-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0ce5-128">NOTES</span></span>

## <span data-ttu-id="e0ce5-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0ce5-129">RELATED LINKS</span></span>

