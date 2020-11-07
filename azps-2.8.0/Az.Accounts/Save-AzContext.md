---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 337fbe8fbfd11fdedad3fa13279dac60bac08455
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745960"
---
# <span data-ttu-id="1d7b2-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="1d7b2-101">Save-AzContext</span></span>

## <span data-ttu-id="1d7b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7b2-103">Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1d7b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d7b2-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d7b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d7b2-105">DESCRIPTION</span></span>
<span data-ttu-id="1d7b2-106">Save-AzContext cmdlet sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1d7b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d7b2-107">EXAMPLES</span></span>

### <span data-ttu-id="1d7b2-108">Exempel 1: Spara den aktuella sessionens kontext</span><span class="sxs-lookup"><span data-stu-id="1d7b2-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="1d7b2-109">I det här exemplet sparas den aktuella sessionens Azure-kontext till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="1d7b2-110">Exempel 2: Spara en given kontext</span><span class="sxs-lookup"><span data-stu-id="1d7b2-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="1d7b2-111">I det här exemplet sparas Azure-kontexten som skickas till cmdleten till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="1d7b2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d7b2-112">PARAMETERS</span></span>

### <span data-ttu-id="1d7b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7b2-113">-DefaultProfile</span></span>
<span data-ttu-id="1d7b2-114">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d7b2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1d7b2-115">-Force</span></span>
<span data-ttu-id="1d7b2-116">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="1d7b2-116">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7b2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="1d7b2-117">-Path</span></span>
<span data-ttu-id="1d7b2-118">Anger sökvägen till filen där autentiseringsinformationen ska sparas.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7b2-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="1d7b2-119">-Profile</span></span>
<span data-ttu-id="1d7b2-120">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="1d7b2-121">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7b2-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d7b2-122">-Confirm</span></span>
<span data-ttu-id="1d7b2-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7b2-124">-WhatIf</span></span>
<span data-ttu-id="1d7b2-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7b2-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7b2-127">CommonParameters</span></span>
<span data-ttu-id="1d7b2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d7b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7b2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d7b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7b2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d7b2-130">INPUTS</span></span>

### <span data-ttu-id="1d7b2-131">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="1d7b2-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="1d7b2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d7b2-132">OUTPUTS</span></span>

### <span data-ttu-id="1d7b2-133">Microsoft. Azure. commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="1d7b2-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="1d7b2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d7b2-134">NOTES</span></span>

## <span data-ttu-id="1d7b2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d7b2-135">RELATED LINKS</span></span>