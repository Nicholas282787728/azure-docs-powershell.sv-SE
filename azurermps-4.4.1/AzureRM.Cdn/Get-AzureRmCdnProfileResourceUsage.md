---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586220"
---
# <span data-ttu-id="ebf2c-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ebf2c-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="ebf2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf2c-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="ebf2c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebf2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebf2c-104">SYNTAX</span></span>

### <span data-ttu-id="ebf2c-105">Parameter uppsättning för fält parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="ebf2c-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebf2c-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="ebf2c-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebf2c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebf2c-107">DESCRIPTION</span></span>
<span data-ttu-id="ebf2c-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="ebf2c-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ebf2c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebf2c-109">EXAMPLES</span></span>

### <span data-ttu-id="ebf2c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ebf2c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ebf2c-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="ebf2c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ebf2c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebf2c-112">PARAMETERS</span></span>

### <span data-ttu-id="ebf2c-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2c-113">-CdnProfile</span></span>
<span data-ttu-id="ebf2c-114">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf2c-115">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="ebf2c-115">-ProfileName</span></span>
<span data-ttu-id="ebf2c-116">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-116">The name of the profile.</span></span>

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

### <span data-ttu-id="ebf2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebf2c-118">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-118">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ebf2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2c-119">-DefaultProfile</span></span>
<span data-ttu-id="ebf2c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf2c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf2c-121">CommonParameters</span></span>
<span data-ttu-id="ebf2c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf2c-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf2c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf2c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebf2c-124">INPUTS</span></span>

### <span data-ttu-id="ebf2c-125">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2c-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ebf2c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebf2c-126">OUTPUTS</span></span>

### <span data-ttu-id="ebf2c-127">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ebf2c-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="ebf2c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebf2c-128">NOTES</span></span>

## <span data-ttu-id="ebf2c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebf2c-129">RELATED LINKS</span></span>

