---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403232"
---
# <span data-ttu-id="32df9-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="32df9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32df9-102">SYNOPSIS</span></span>
<span data-ttu-id="32df9-103">Hämtar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="32df9-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="32df9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32df9-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32df9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32df9-105">DESCRIPTION</span></span>
<span data-ttu-id="32df9-106">Cmdleten **Get-AzCdnProfile** får en CDN-profil (Content Delivery Network) och tillhör ande information.</span><span class="sxs-lookup"><span data-stu-id="32df9-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="32df9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32df9-107">EXAMPLES</span></span>

## <span data-ttu-id="32df9-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32df9-108">PARAMETERS</span></span>

### <span data-ttu-id="32df9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-109">-DefaultProfile</span></span>
<span data-ttu-id="32df9-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="32df9-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32df9-111">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="32df9-111">-ProfileName</span></span>
<span data-ttu-id="32df9-112">Anger namnet på profilen.</span><span class="sxs-lookup"><span data-stu-id="32df9-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="32df9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32df9-113">-ResourceGroupName</span></span>
<span data-ttu-id="32df9-114">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="32df9-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="32df9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32df9-115">CommonParameters</span></span>
<span data-ttu-id="32df9-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32df9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32df9-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32df9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32df9-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32df9-118">INPUTS</span></span>

### <span data-ttu-id="32df9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="32df9-119">System.String</span></span>

## <span data-ttu-id="32df9-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32df9-120">OUTPUTS</span></span>

### <span data-ttu-id="32df9-121">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="32df9-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32df9-122">NOTES</span></span>

## <span data-ttu-id="32df9-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32df9-123">RELATED LINKS</span></span>

[<span data-ttu-id="32df9-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="32df9-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="32df9-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="32df9-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


