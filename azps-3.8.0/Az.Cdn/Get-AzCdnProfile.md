---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091411"
---
# <span data-ttu-id="8d874-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="8d874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d874-102">SYNOPSIS</span></span>
<span data-ttu-id="8d874-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="8d874-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="8d874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d874-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d874-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d874-105">DESCRIPTION</span></span>
<span data-ttu-id="8d874-106">Cmdleten **Get-AzCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="8d874-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="8d874-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d874-107">EXAMPLES</span></span>

## <span data-ttu-id="8d874-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d874-108">PARAMETERS</span></span>

### <span data-ttu-id="8d874-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-109">-DefaultProfile</span></span>
<span data-ttu-id="8d874-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d874-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d874-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="8d874-111">-ProfileName</span></span>
<span data-ttu-id="8d874-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="8d874-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d874-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d874-113">-ResourceGroupName</span></span>
<span data-ttu-id="8d874-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8d874-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d874-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d874-115">CommonParameters</span></span>
<span data-ttu-id="8d874-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d874-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d874-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d874-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d874-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d874-118">INPUTS</span></span>

### <span data-ttu-id="8d874-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8d874-119">System.String</span></span>

## <span data-ttu-id="8d874-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d874-120">OUTPUTS</span></span>

### <span data-ttu-id="8d874-121">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8d874-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d874-122">NOTES</span></span>

## <span data-ttu-id="8d874-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d874-123">RELATED LINKS</span></span>

[<span data-ttu-id="8d874-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="8d874-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="8d874-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8d874-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)

