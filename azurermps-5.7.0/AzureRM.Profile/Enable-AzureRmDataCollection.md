---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756483"
---
# <span data-ttu-id="0c113-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="0c113-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="0c113-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c113-102">SYNOPSIS</span></span>
<span data-ttu-id="0c113-103">Gör att Azure PowerShell samlar in data för att förbättra användar upplevelsen med AzurePowerShell cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0c113-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="0c113-104">Kör den här cmdleten till data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0c113-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="0c113-105">Inga data samlas in om du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="0c113-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c113-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c113-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c113-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c113-107">DESCRIPTION</span></span>
<span data-ttu-id="0c113-108">Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.</span><span class="sxs-lookup"><span data-stu-id="0c113-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="0c113-109">Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzureRmDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c113-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="0c113-110">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c113-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="0c113-111">Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="0c113-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="0c113-112">Kör cmdleten Enable-AzureRMDataCollection för att aktivera data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0c113-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="0c113-113">Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.</span><span class="sxs-lookup"><span data-stu-id="0c113-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="0c113-114">Kör cmdleten Disable-AzureRmDataCollection om du vill inaktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="0c113-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="0c113-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c113-115">EXAMPLES</span></span>

### <span data-ttu-id="0c113-116">Exempel 1: Aktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="0c113-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="0c113-117">Det här exemplet visar hur du aktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="0c113-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="0c113-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c113-118">PARAMETERS</span></span>

### <span data-ttu-id="0c113-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c113-119">-DefaultProfile</span></span>
<span data-ttu-id="0c113-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c113-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c113-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c113-121">-Confirm</span></span>
<span data-ttu-id="0c113-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c113-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c113-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c113-123">-WhatIf</span></span>
<span data-ttu-id="0c113-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c113-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c113-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c113-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c113-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c113-126">CommonParameters</span></span>
<span data-ttu-id="0c113-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c113-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c113-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c113-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c113-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c113-129">INPUTS</span></span>

### <span data-ttu-id="0c113-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0c113-130">None</span></span>
<span data-ttu-id="0c113-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0c113-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c113-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c113-132">OUTPUTS</span></span>

### <span data-ttu-id="0c113-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="0c113-133">None</span></span>

## <span data-ttu-id="0c113-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c113-134">NOTES</span></span>

## <span data-ttu-id="0c113-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c113-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c113-136">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="0c113-136">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

