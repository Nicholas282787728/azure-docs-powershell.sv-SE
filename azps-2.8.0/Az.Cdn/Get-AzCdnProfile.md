---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: a833d542bd72392ef56e5a8bde086247f1f2c299
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745326"
---
# <span data-ttu-id="c8d28-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="c8d28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8d28-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d28-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="c8d28-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="c8d28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8d28-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d28-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8d28-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d28-106">Cmdleten **Get-AzCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="c8d28-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="c8d28-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8d28-107">EXAMPLES</span></span>

## <span data-ttu-id="c8d28-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8d28-108">PARAMETERS</span></span>

### <span data-ttu-id="c8d28-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-109">-DefaultProfile</span></span>
<span data-ttu-id="c8d28-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8d28-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8d28-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="c8d28-111">-ProfileName</span></span>
<span data-ttu-id="c8d28-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="c8d28-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="c8d28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d28-113">-ResourceGroupName</span></span>
<span data-ttu-id="c8d28-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="c8d28-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c8d28-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d28-115">CommonParameters</span></span>
<span data-ttu-id="c8d28-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d28-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d28-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8d28-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d28-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8d28-118">INPUTS</span></span>

### <span data-ttu-id="c8d28-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d28-119">System.String</span></span>

## <span data-ttu-id="c8d28-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8d28-120">OUTPUTS</span></span>

### <span data-ttu-id="c8d28-121">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c8d28-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8d28-122">NOTES</span></span>

## <span data-ttu-id="c8d28-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8d28-123">RELATED LINKS</span></span>

[<span data-ttu-id="c8d28-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="c8d28-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="c8d28-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8d28-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


