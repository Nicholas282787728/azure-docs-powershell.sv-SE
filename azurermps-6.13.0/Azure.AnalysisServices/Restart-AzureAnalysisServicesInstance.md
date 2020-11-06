---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 496c0410808604303ab60d8ad4d989e838828bf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574109"
---
# <span data-ttu-id="4a744-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="4a744-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="4a744-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a744-102">SYNOPSIS</span></span>
<span data-ttu-id="4a744-103">Startar om en instans av Analysis Services-servern i den aktuella inloggade miljön som angivet i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="4a744-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a744-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a744-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance -Instance <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a744-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a744-105">DESCRIPTION</span></span>
<span data-ttu-id="4a744-106">Restart-AzureAnalysisServicesInstance cmdlet startar om en instans av Azure Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="4a744-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="4a744-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a744-107">EXAMPLES</span></span>

### <span data-ttu-id="4a744-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a744-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="4a744-109">Det här kommandot startar om servern ' testserver ' i miljön som anges i kommandot Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4a744-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="4a744-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a744-110">PARAMETERS</span></span>

### <span data-ttu-id="4a744-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="4a744-111">-Instance</span></span>
<span data-ttu-id="4a744-112">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="4a744-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="4a744-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a744-113">-PassThru</span></span>
<span data-ttu-id="4a744-114">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="4a744-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4a744-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a744-115">-Confirm</span></span>
<span data-ttu-id="4a744-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a744-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a744-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a744-117">-WhatIf</span></span>
<span data-ttu-id="4a744-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a744-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a744-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a744-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a744-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a744-120">CommonParameters</span></span>
<span data-ttu-id="4a744-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a744-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a744-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a744-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a744-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a744-123">INPUTS</span></span>

### <span data-ttu-id="4a744-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="4a744-124">None</span></span>

## <span data-ttu-id="4a744-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a744-125">OUTPUTS</span></span>

### <span data-ttu-id="4a744-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a744-126">System.Boolean</span></span>

## <span data-ttu-id="4a744-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a744-127">NOTES</span></span>
<span data-ttu-id="4a744-128">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="4a744-128">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="4a744-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a744-129">RELATED LINKS</span></span>
