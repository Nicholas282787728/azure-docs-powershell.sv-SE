---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393264"
---
# <span data-ttu-id="23ef1-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="23ef1-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="23ef1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="23ef1-103">Gör att Azure PowerShell samlar in data för att förbättra användar upplevelsen med Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="23ef1-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="23ef1-104">Kör den här cmdleten till data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="23ef1-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="23ef1-105">Data samlas in som standard om du inte uttryckligen avmarkerar dem.</span><span class="sxs-lookup"><span data-stu-id="23ef1-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="23ef1-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23ef1-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ef1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23ef1-107">DESCRIPTION</span></span>

<span data-ttu-id="23ef1-108">`Enable-AzDataCollection`Cmdleten används för att välja data insamling.</span><span class="sxs-lookup"><span data-stu-id="23ef1-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="23ef1-109">Azure PowerShell samlar automatiskt in telemetridata som standard.</span><span class="sxs-lookup"><span data-stu-id="23ef1-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="23ef1-110">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="23ef1-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="23ef1-111">Microsoft Azure PowerShell samlar inte in någon privat eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="23ef1-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="23ef1-112">Om du vill inaktivera data insamling måste du uttryckligen välja att köra `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="23ef1-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="23ef1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23ef1-113">EXAMPLES</span></span>

### <span data-ttu-id="23ef1-114">Exempel 1: Aktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="23ef1-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="23ef1-115">I följande exempel visas hur du aktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="23ef1-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="23ef1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23ef1-116">PARAMETERS</span></span>

### <span data-ttu-id="23ef1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ef1-117">-DefaultProfile</span></span>

<span data-ttu-id="23ef1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23ef1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ef1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23ef1-119">-Confirm</span></span>

<span data-ttu-id="23ef1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23ef1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ef1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ef1-121">-WhatIf</span></span>

<span data-ttu-id="23ef1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23ef1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23ef1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23ef1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ef1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ef1-124">CommonParameters</span></span>

<span data-ttu-id="23ef1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ef1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ef1-126">Mer information finns i [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="23ef1-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="23ef1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23ef1-127">INPUTS</span></span>

### <span data-ttu-id="23ef1-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="23ef1-128">None</span></span>

## <span data-ttu-id="23ef1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23ef1-129">OUTPUTS</span></span>

### <span data-ttu-id="23ef1-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="23ef1-130">System.Void</span></span>

## <span data-ttu-id="23ef1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23ef1-131">NOTES</span></span>

## <span data-ttu-id="23ef1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23ef1-132">RELATED LINKS</span></span>

[<span data-ttu-id="23ef1-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="23ef1-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
