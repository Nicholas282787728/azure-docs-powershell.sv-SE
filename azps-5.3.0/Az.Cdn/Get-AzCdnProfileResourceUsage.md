---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524626"
---
# <span data-ttu-id="b73bc-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b73bc-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="b73bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b73bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b73bc-103">Hämtar resursanvändningen för en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="b73bc-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="b73bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b73bc-104">SYNTAX</span></span>

### <span data-ttu-id="b73bc-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b73bc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b73bc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b73bc-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b73bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b73bc-107">DESCRIPTION</span></span>
<span data-ttu-id="b73bc-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="b73bc-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b73bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b73bc-109">EXAMPLES</span></span>

### <span data-ttu-id="b73bc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b73bc-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b73bc-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="b73bc-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="b73bc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b73bc-112">PARAMETERS</span></span>

### <span data-ttu-id="b73bc-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b73bc-113">-CdnProfile</span></span>
<span data-ttu-id="b73bc-114">Ett Azure CDN-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="b73bc-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="b73bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73bc-115">-DefaultProfile</span></span>
<span data-ttu-id="b73bc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b73bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b73bc-117">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="b73bc-117">-ProfileName</span></span>
<span data-ttu-id="b73bc-118">Namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="b73bc-118">The name of the profile.</span></span>

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

### <span data-ttu-id="b73bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="b73bc-120">Den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b73bc-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="b73bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73bc-121">CommonParameters</span></span>
<span data-ttu-id="b73bc-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73bc-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b73bc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73bc-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b73bc-124">INPUTS</span></span>

### <span data-ttu-id="b73bc-125">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b73bc-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b73bc-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b73bc-126">OUTPUTS</span></span>

### <span data-ttu-id="b73bc-127">Microsoft. Azure. commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b73bc-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="b73bc-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b73bc-128">NOTES</span></span>

## <span data-ttu-id="b73bc-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b73bc-129">RELATED LINKS</span></span>
