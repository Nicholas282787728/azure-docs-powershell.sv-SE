---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 623b7c84b29e5e64a47beeff6c9f7dba88edf32b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745887"
---
# <span data-ttu-id="d836f-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="d836f-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="d836f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d836f-102">SYNOPSIS</span></span>
<span data-ttu-id="d836f-103">Startar om en instans av Analysis Services-servern i den aktuella inloggade miljön som angivet i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="d836f-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d836f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d836f-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d836f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d836f-105">DESCRIPTION</span></span>
<span data-ttu-id="d836f-106">Restart-AzAnalysisServicesInstance cmdlet startar om en instans av Azure Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="d836f-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="d836f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d836f-107">EXAMPLES</span></span>

### <span data-ttu-id="d836f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d836f-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="d836f-109">Det här kommandot startar om servern ' testserver ' i miljön som anges i kommandot Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d836f-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d836f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d836f-110">PARAMETERS</span></span>

### <span data-ttu-id="d836f-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="d836f-111">-Instance</span></span>
<span data-ttu-id="d836f-112">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="d836f-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d836f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d836f-113">-PassThru</span></span>
<span data-ttu-id="d836f-114">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="d836f-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d836f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d836f-115">-Confirm</span></span>
<span data-ttu-id="d836f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d836f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d836f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d836f-117">-WhatIf</span></span>
<span data-ttu-id="d836f-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d836f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d836f-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d836f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d836f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d836f-120">CommonParameters</span></span>
<span data-ttu-id="d836f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d836f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d836f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d836f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d836f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d836f-123">INPUTS</span></span>

### <span data-ttu-id="d836f-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="d836f-124">None</span></span>

## <span data-ttu-id="d836f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d836f-125">OUTPUTS</span></span>

### <span data-ttu-id="d836f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d836f-126">System.Boolean</span></span>

## <span data-ttu-id="d836f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d836f-127">NOTES</span></span>
<span data-ttu-id="d836f-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="d836f-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="d836f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d836f-129">RELATED LINKS</span></span>
