---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571032"
---
# <span data-ttu-id="f142f-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f142f-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="f142f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f142f-102">SYNOPSIS</span></span>
<span data-ttu-id="f142f-103">Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="f142f-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f142f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f142f-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f142f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f142f-105">DESCRIPTION</span></span>
<span data-ttu-id="f142f-106">Save-AzureRmContext cmdlet sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="f142f-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f142f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f142f-107">EXAMPLES</span></span>

### <span data-ttu-id="f142f-108">Exempel 1: Spara den aktuella sessionens kontext</span><span class="sxs-lookup"><span data-stu-id="f142f-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="f142f-109">I det här exemplet sparas den aktuella sessionens Azure-kontext till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="f142f-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="f142f-110">Exempel 2: Spara en given kontext</span><span class="sxs-lookup"><span data-stu-id="f142f-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="f142f-111">I det här exemplet sparas Azure-kontexten som skickas till cmdleten till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="f142f-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="f142f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f142f-112">PARAMETERS</span></span>

### <span data-ttu-id="f142f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f142f-113">-Force</span></span>
<span data-ttu-id="f142f-114">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="f142f-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="f142f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f142f-115">-Path</span></span>
<span data-ttu-id="f142f-116">Anger sökvägen till filen där autentiseringsinformationen ska sparas.</span><span class="sxs-lookup"><span data-stu-id="f142f-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f142f-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="f142f-117">-Profile</span></span>
<span data-ttu-id="f142f-118">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f142f-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="f142f-119">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="f142f-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f142f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f142f-120">-Confirm</span></span>
<span data-ttu-id="f142f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f142f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f142f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f142f-122">-WhatIf</span></span>
<span data-ttu-id="f142f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f142f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f142f-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f142f-124">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f142f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f142f-125">INPUTS</span></span>

### <span data-ttu-id="f142f-126">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="f142f-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="f142f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f142f-127">OUTPUTS</span></span>

### <span data-ttu-id="f142f-128">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f142f-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="f142f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f142f-129">NOTES</span></span>

## <span data-ttu-id="f142f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f142f-130">RELATED LINKS</span></span>

