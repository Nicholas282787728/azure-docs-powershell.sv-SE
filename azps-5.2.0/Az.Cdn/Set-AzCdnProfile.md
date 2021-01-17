---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406395"
---
# <span data-ttu-id="168d4-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="168d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="168d4-102">SYNOPSIS</span></span>
<span data-ttu-id="168d4-103">Uppdaterar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="168d4-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="168d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="168d4-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="168d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="168d4-105">DESCRIPTION</span></span>
<span data-ttu-id="168d4-106">Cmdleten **set-AzCdnProfile** uppdaterar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="168d4-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="168d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="168d4-107">EXAMPLES</span></span>

## <span data-ttu-id="168d4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="168d4-108">PARAMETERS</span></span>

### <span data-ttu-id="168d4-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-109">-CdnProfile</span></span>
<span data-ttu-id="168d4-110">Anger den profil som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="168d4-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="168d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-111">-DefaultProfile</span></span>
<span data-ttu-id="168d4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="168d4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="168d4-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="168d4-113">-Confirm</span></span>
<span data-ttu-id="168d4-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="168d4-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d4-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168d4-115">-WhatIf</span></span>
<span data-ttu-id="168d4-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="168d4-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168d4-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="168d4-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168d4-118">CommonParameters</span></span>
<span data-ttu-id="168d4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168d4-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="168d4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168d4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="168d4-121">INPUTS</span></span>

### <span data-ttu-id="168d4-122">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="168d4-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="168d4-123">OUTPUTS</span></span>

### <span data-ttu-id="168d4-124">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="168d4-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="168d4-125">NOTES</span></span>

## <span data-ttu-id="168d4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="168d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="168d4-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="168d4-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="168d4-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="168d4-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


