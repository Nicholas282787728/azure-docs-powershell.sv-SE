---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 689604037c709496f0ccc5208599f7151eaf2c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745324"
---
# <span data-ttu-id="fefdd-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fefdd-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="fefdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fefdd-102">SYNOPSIS</span></span>
<span data-ttu-id="fefdd-103">Hämtar resursanvändningen för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="fefdd-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="fefdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fefdd-104">SYNTAX</span></span>

### <span data-ttu-id="fefdd-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fefdd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fefdd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fefdd-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fefdd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fefdd-107">DESCRIPTION</span></span>
<span data-ttu-id="fefdd-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="fefdd-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="fefdd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fefdd-109">EXAMPLES</span></span>

### <span data-ttu-id="fefdd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fefdd-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fefdd-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="fefdd-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="fefdd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fefdd-112">PARAMETERS</span></span>

### <span data-ttu-id="fefdd-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fefdd-113">-CdnProfile</span></span>
<span data-ttu-id="fefdd-114">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="fefdd-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="fefdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefdd-115">-DefaultProfile</span></span>
<span data-ttu-id="fefdd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fefdd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fefdd-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="fefdd-117">-ProfileName</span></span>
<span data-ttu-id="fefdd-118">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="fefdd-118">The name of the profile.</span></span>

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

### <span data-ttu-id="fefdd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefdd-119">-ResourceGroupName</span></span>
<span data-ttu-id="fefdd-120">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="fefdd-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="fefdd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefdd-121">CommonParameters</span></span>
<span data-ttu-id="fefdd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fefdd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefdd-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fefdd-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefdd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fefdd-124">INPUTS</span></span>

### <span data-ttu-id="fefdd-125">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fefdd-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="fefdd-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fefdd-126">OUTPUTS</span></span>

### <span data-ttu-id="fefdd-127">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fefdd-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="fefdd-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fefdd-128">NOTES</span></span>

## <span data-ttu-id="fefdd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fefdd-129">RELATED LINKS</span></span>
