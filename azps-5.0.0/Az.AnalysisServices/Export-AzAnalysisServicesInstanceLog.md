---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324132"
---
# <span data-ttu-id="43342-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="43342-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="43342-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43342-102">SYNOPSIS</span></span>
<span data-ttu-id="43342-103">Exporterar en logg från en instans av Analysis Services-servern i den aktuella inloggade miljön som angiven i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="43342-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43342-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43342-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43342-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43342-105">DESCRIPTION</span></span>
<span data-ttu-id="43342-106">Export-AzAnalysisServicesInstance cmdlet exporterar loggen från en instans av Azure Analysis Services-servern till filen</span><span class="sxs-lookup"><span data-stu-id="43342-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="43342-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43342-107">EXAMPLES</span></span>

### <span data-ttu-id="43342-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43342-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="43342-109">Det här kommandot exporterar logg från servern ' testserver ' i den miljö som anges i kommandot Add-AzAnalysisServicesAccount och sparar den i filen som anges i OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="43342-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="43342-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43342-110">PARAMETERS</span></span>

### <span data-ttu-id="43342-111">-Force</span><span class="sxs-lookup"><span data-stu-id="43342-111">-Force</span></span>
<span data-ttu-id="43342-112">Skriv över filen om den finns utan att fråga</span><span class="sxs-lookup"><span data-stu-id="43342-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="43342-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="43342-113">-Instance</span></span>
<span data-ttu-id="43342-114">Namn på Analysis Services-serverinstansen</span><span class="sxs-lookup"><span data-stu-id="43342-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="43342-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="43342-115">-OutputPath</span></span>
<span data-ttu-id="43342-116">Sökväg till fil som ska exporteras</span><span class="sxs-lookup"><span data-stu-id="43342-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43342-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43342-117">-PassThru</span></span>
<span data-ttu-id="43342-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="43342-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="43342-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43342-119">-Confirm</span></span>
<span data-ttu-id="43342-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43342-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43342-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43342-121">-WhatIf</span></span>
<span data-ttu-id="43342-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43342-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43342-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43342-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43342-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43342-124">CommonParameters</span></span>
<span data-ttu-id="43342-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43342-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43342-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43342-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43342-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43342-127">INPUTS</span></span>

### <span data-ttu-id="43342-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="43342-128">None</span></span>

## <span data-ttu-id="43342-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43342-129">OUTPUTS</span></span>

### <span data-ttu-id="43342-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="43342-130">System.Void</span></span>

## <span data-ttu-id="43342-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43342-131">NOTES</span></span>
<span data-ttu-id="43342-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="43342-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="43342-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43342-133">RELATED LINKS</span></span>
