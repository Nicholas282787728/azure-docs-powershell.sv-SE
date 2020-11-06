---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571900"
---
# <span data-ttu-id="68a43-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="68a43-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="68a43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68a43-102">SYNOPSIS</span></span>
<span data-ttu-id="68a43-103">Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="68a43-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="68a43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68a43-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68a43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68a43-105">DESCRIPTION</span></span>
<span data-ttu-id="68a43-106">Save-AzureRmProfile cmdlet sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="68a43-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="68a43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68a43-107">EXAMPLES</span></span>

### <span data-ttu-id="68a43-108">Exempel 1: Spara den aktuella sessionens profil</span><span class="sxs-lookup"><span data-stu-id="68a43-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="68a43-109">I det här exemplet sparas den aktuella sessionens Azure-profil till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="68a43-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="68a43-110">Exempel 2: Spara en profil</span><span class="sxs-lookup"><span data-stu-id="68a43-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="68a43-111">I det här exemplet sparas den Azure-profil som skickas till cmdleten till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="68a43-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="68a43-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68a43-112">PARAMETERS</span></span>

### <span data-ttu-id="68a43-113">-Force</span><span class="sxs-lookup"><span data-stu-id="68a43-113">-Force</span></span>
<span data-ttu-id="68a43-114">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="68a43-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a43-115">-Path</span><span class="sxs-lookup"><span data-stu-id="68a43-115">-Path</span></span>
<span data-ttu-id="68a43-116">Anger sökvägen till filen där autentiseringsinformationen ska sparas.</span><span class="sxs-lookup"><span data-stu-id="68a43-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a43-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="68a43-117">-Profile</span></span>
<span data-ttu-id="68a43-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="68a43-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="68a43-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="68a43-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68a43-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68a43-120">-Confirm</span></span>
<span data-ttu-id="68a43-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68a43-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a43-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a43-122">-WhatIf</span></span>
<span data-ttu-id="68a43-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68a43-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68a43-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68a43-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a43-125">CommonParameters</span></span>
<span data-ttu-id="68a43-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a43-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a43-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a43-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68a43-128">INPUTS</span></span>

## <span data-ttu-id="68a43-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68a43-129">OUTPUTS</span></span>

### <span data-ttu-id="68a43-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="68a43-130">PSAzureProfile</span></span>

## <span data-ttu-id="68a43-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68a43-131">NOTES</span></span>

## <span data-ttu-id="68a43-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68a43-132">RELATED LINKS</span></span>

[<span data-ttu-id="68a43-133">Select-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="68a43-133">Select-AzureRMProfile</span></span>]()

