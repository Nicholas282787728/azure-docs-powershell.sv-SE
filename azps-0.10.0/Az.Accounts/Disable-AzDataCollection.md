---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922005"
---
# <span data-ttu-id="8f7ce-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="8f7ce-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="8f7ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7ce-103">Det går inte att samla in data för att förbättra AzurePowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="8f7ce-104">Data samlas in såvida du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="8f7ce-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f7ce-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7ce-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f7ce-106">DESCRIPTION</span></span>
<span data-ttu-id="8f7ce-107">Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="8f7ce-108">Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="8f7ce-109">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="8f7ce-110">Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="8f7ce-111">Kör cmdleten Disable-AzDataCollection för att inaktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="8f7ce-112">Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="8f7ce-113">Kör cmdleten Enable-AzDataCollection om du vill aktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="8f7ce-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f7ce-114">EXAMPLES</span></span>

### <span data-ttu-id="8f7ce-115">Exempel 1: inaktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="8f7ce-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="8f7ce-116">Det här exemplet visar hur du inaktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="8f7ce-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f7ce-117">PARAMETERS</span></span>

### <span data-ttu-id="8f7ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7ce-118">-DefaultProfile</span></span>
<span data-ttu-id="8f7ce-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7ce-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f7ce-120">-Confirm</span></span>
<span data-ttu-id="8f7ce-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7ce-122">-WhatIf</span></span>
<span data-ttu-id="8f7ce-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f7ce-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7ce-125">CommonParameters</span></span>
<span data-ttu-id="8f7ce-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7ce-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f7ce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7ce-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f7ce-128">INPUTS</span></span>

### <span data-ttu-id="8f7ce-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="8f7ce-129">None</span></span>

## <span data-ttu-id="8f7ce-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f7ce-130">OUTPUTS</span></span>

### <span data-ttu-id="8f7ce-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="8f7ce-131">System.Void</span></span>

## <span data-ttu-id="8f7ce-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f7ce-132">NOTES</span></span>

## <span data-ttu-id="8f7ce-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f7ce-133">RELATED LINKS</span></span>

[<span data-ttu-id="8f7ce-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="8f7ce-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

