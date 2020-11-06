---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: c605921d56cb9fd70005c290d696e5f50b0d4175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581047"
---
# <span data-ttu-id="6bf55-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6bf55-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="6bf55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bf55-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf55-103">Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="6bf55-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bf55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bf55-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bf55-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bf55-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf55-106">Save-AzureRmContext cmdlet sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="6bf55-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="6bf55-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bf55-107">EXAMPLES</span></span>

### <span data-ttu-id="6bf55-108">Exempel 1: Spara den aktuella sessionens kontext</span><span class="sxs-lookup"><span data-stu-id="6bf55-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="6bf55-109">I det här exemplet sparas den aktuella sessionens Azure-kontext till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="6bf55-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="6bf55-110">Exempel 2: Spara en given kontext</span><span class="sxs-lookup"><span data-stu-id="6bf55-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="6bf55-111">I det här exemplet sparas Azure-kontexten som skickas till cmdleten till den JSON-fil som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="6bf55-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="6bf55-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bf55-112">PARAMETERS</span></span>

### <span data-ttu-id="6bf55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf55-113">-DefaultProfile</span></span>
<span data-ttu-id="6bf55-114">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6bf55-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf55-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6bf55-115">-Force</span></span>
<span data-ttu-id="6bf55-116">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="6bf55-116">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf55-117">-Path</span><span class="sxs-lookup"><span data-stu-id="6bf55-117">-Path</span></span>
<span data-ttu-id="6bf55-118">Anger sökvägen till filen där autentiseringsinformationen ska sparas.</span><span class="sxs-lookup"><span data-stu-id="6bf55-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="6bf55-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="6bf55-119">-Profile</span></span>
<span data-ttu-id="6bf55-120">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6bf55-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="6bf55-121">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="6bf55-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="6bf55-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bf55-122">-Confirm</span></span>
<span data-ttu-id="6bf55-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bf55-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf55-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf55-124">-WhatIf</span></span>
<span data-ttu-id="6bf55-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bf55-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf55-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bf55-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf55-127">CommonParameters</span></span>
<span data-ttu-id="6bf55-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf55-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf55-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf55-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bf55-130">INPUTS</span></span>

### <span data-ttu-id="6bf55-131">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="6bf55-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="6bf55-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bf55-132">OUTPUTS</span></span>

### <span data-ttu-id="6bf55-133">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="6bf55-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="6bf55-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bf55-134">NOTES</span></span>

## <span data-ttu-id="6bf55-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bf55-135">RELATED LINKS</span></span>

