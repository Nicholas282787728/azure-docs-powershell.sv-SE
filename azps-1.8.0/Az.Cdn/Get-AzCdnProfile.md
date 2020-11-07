---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 110528c1e7a9891381ebc8182a1e0b45267d87b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754643"
---
# <span data-ttu-id="2eb82-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="2eb82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eb82-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb82-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="2eb82-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="2eb82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eb82-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eb82-105">DESCRIPTION</span></span>
<span data-ttu-id="2eb82-106">Cmdleten **Get-AzCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="2eb82-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="2eb82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eb82-107">EXAMPLES</span></span>

## <span data-ttu-id="2eb82-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eb82-108">PARAMETERS</span></span>

### <span data-ttu-id="2eb82-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-109">-DefaultProfile</span></span>
<span data-ttu-id="2eb82-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2eb82-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2eb82-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="2eb82-111">-ProfileName</span></span>
<span data-ttu-id="2eb82-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="2eb82-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="2eb82-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb82-113">-ResourceGroupName</span></span>
<span data-ttu-id="2eb82-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="2eb82-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="2eb82-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb82-115">CommonParameters</span></span>
<span data-ttu-id="2eb82-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb82-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb82-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb82-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb82-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eb82-118">INPUTS</span></span>

### <span data-ttu-id="2eb82-119">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb82-119">System.String</span></span>

## <span data-ttu-id="2eb82-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eb82-120">OUTPUTS</span></span>

### <span data-ttu-id="2eb82-121">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2eb82-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eb82-122">NOTES</span></span>

## <span data-ttu-id="2eb82-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eb82-123">RELATED LINKS</span></span>

[<span data-ttu-id="2eb82-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="2eb82-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="2eb82-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2eb82-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


