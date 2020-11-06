---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575405"
---
# <span data-ttu-id="a9755-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a9755-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="a9755-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9755-102">SYNOPSIS</span></span>
<span data-ttu-id="a9755-103">Exporterar en logg från en instans av Analysis Services-servern i den aktuella inloggade miljön som angiven i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="a9755-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9755-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9755-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9755-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9755-105">DESCRIPTION</span></span>
<span data-ttu-id="a9755-106">Export-AzureAnalysisServicesInstance cmdlet exporterar loggen från en instans av Azure Analysis Services-servern till filen</span><span class="sxs-lookup"><span data-stu-id="a9755-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="a9755-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9755-107">EXAMPLES</span></span>

### <span data-ttu-id="a9755-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9755-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="a9755-109">Det här kommandot exporterar logg från servern ' testserver ' i den miljö som anges i kommandot Add-AzureAnalysisServicesAccount och sparar den i filen som anges i OutputPath ' C:\path\to\log\testserver.log '</span><span class="sxs-lookup"><span data-stu-id="a9755-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="a9755-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9755-110">PARAMETERS</span></span>

### <span data-ttu-id="a9755-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a9755-111">-Force</span></span>
<span data-ttu-id="a9755-112">Skriv över filen om den finns utan att fråga</span><span class="sxs-lookup"><span data-stu-id="a9755-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="a9755-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="a9755-113">-Instance</span></span>
<span data-ttu-id="a9755-114">Namn på Analysis Services-serverinstansen</span><span class="sxs-lookup"><span data-stu-id="a9755-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="a9755-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a9755-115">-OutputPath</span></span>
<span data-ttu-id="a9755-116">Sökväg till fil som ska exporteras</span><span class="sxs-lookup"><span data-stu-id="a9755-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="a9755-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9755-117">-Confirm</span></span>
<span data-ttu-id="a9755-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9755-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9755-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9755-119">-WhatIf</span></span>
<span data-ttu-id="a9755-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9755-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9755-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9755-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9755-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9755-122">CommonParameters</span></span>
<span data-ttu-id="a9755-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9755-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9755-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9755-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9755-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9755-125">INPUTS</span></span>

### <span data-ttu-id="a9755-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9755-126">None</span></span>

## <span data-ttu-id="a9755-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9755-127">OUTPUTS</span></span>

### <span data-ttu-id="a9755-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="a9755-128">System.Void</span></span>

## <span data-ttu-id="a9755-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9755-129">NOTES</span></span>
<span data-ttu-id="a9755-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a9755-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="a9755-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9755-131">RELATED LINKS</span></span>
