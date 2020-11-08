---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259659"
---
# <span data-ttu-id="962e6-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="962e6-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="962e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="962e6-102">SYNOPSIS</span></span>
<span data-ttu-id="962e6-103">Det går inte att samla in data för att förbättra Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="962e6-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="962e6-104">Data samlas in som standard om du inte uttryckligen avmarkerar dem.</span><span class="sxs-lookup"><span data-stu-id="962e6-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="962e6-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="962e6-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962e6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="962e6-106">DESCRIPTION</span></span>

<span data-ttu-id="962e6-107">`Disable-AzDataCollection`Cmdleten används för att välja bort insamling av data.</span><span class="sxs-lookup"><span data-stu-id="962e6-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="962e6-108">Azure PowerShell samlar automatiskt in telemetridata som standard.</span><span class="sxs-lookup"><span data-stu-id="962e6-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="962e6-109">Om du vill inaktivera data insamling måste du uttryckligen välja att avbryta. Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="962e6-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="962e6-110">Microsoft Azure PowerShell samlar inte in någon privat eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="962e6-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="962e6-111">Om du tidigare har valt att aktivera kör du `Enable-AzDataCollection` cmdleten för att återaktivera data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="962e6-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="962e6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="962e6-112">EXAMPLES</span></span>

### <span data-ttu-id="962e6-113">Exempel 1: inaktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="962e6-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="962e6-114">I följande exempel visas hur du inaktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="962e6-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="962e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="962e6-115">PARAMETERS</span></span>

### <span data-ttu-id="962e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962e6-116">-DefaultProfile</span></span>

<span data-ttu-id="962e6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="962e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962e6-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="962e6-118">-Confirm</span></span>

<span data-ttu-id="962e6-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="962e6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962e6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962e6-120">-WhatIf</span></span>

<span data-ttu-id="962e6-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="962e6-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="962e6-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="962e6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962e6-123">CommonParameters</span></span>

<span data-ttu-id="962e6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962e6-125">Mer information finns i [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="962e6-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="962e6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="962e6-126">INPUTS</span></span>

### <span data-ttu-id="962e6-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="962e6-127">None</span></span>

## <span data-ttu-id="962e6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="962e6-128">OUTPUTS</span></span>

### <span data-ttu-id="962e6-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="962e6-129">System.Void</span></span>

## <span data-ttu-id="962e6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="962e6-130">NOTES</span></span>

## <span data-ttu-id="962e6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="962e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="962e6-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="962e6-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
