---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578943"
---
# <span data-ttu-id="4ce39-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="4ce39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ce39-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce39-103">Uppdaterar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="4ce39-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ce39-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ce39-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce39-106">Cmdleten **set-AzureRmCdnProfile** uppdaterar en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="4ce39-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4ce39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ce39-107">EXAMPLES</span></span>

## <span data-ttu-id="4ce39-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ce39-108">PARAMETERS</span></span>

### <span data-ttu-id="4ce39-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-109">-CdnProfile</span></span>
<span data-ttu-id="4ce39-110">Anger den profil som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="4ce39-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4ce39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-111">-DefaultProfile</span></span>
<span data-ttu-id="4ce39-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ce39-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ce39-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ce39-113">-Confirm</span></span>
<span data-ttu-id="4ce39-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ce39-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce39-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce39-115">-WhatIf</span></span>
<span data-ttu-id="4ce39-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ce39-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce39-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ce39-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce39-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce39-118">CommonParameters</span></span>
<span data-ttu-id="4ce39-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce39-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce39-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce39-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce39-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ce39-121">INPUTS</span></span>

### <span data-ttu-id="4ce39-122">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="4ce39-123">Parametrar: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ce39-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="4ce39-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ce39-124">OUTPUTS</span></span>

### <span data-ttu-id="4ce39-125">Microsoft. Azure. commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4ce39-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ce39-126">NOTES</span></span>

## <span data-ttu-id="4ce39-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ce39-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ce39-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="4ce39-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="4ce39-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4ce39-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


