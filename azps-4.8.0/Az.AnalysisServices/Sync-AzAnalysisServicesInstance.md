---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102502"
---
# <span data-ttu-id="8a89f-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8a89f-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8a89f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a89f-102">SYNOPSIS</span></span>

<span data-ttu-id="8a89f-103">Synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla instanser av den aktuella inloggade miljön enligt vad som anges i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="8a89f-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8a89f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a89f-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a89f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a89f-105">DESCRIPTION</span></span>

<span data-ttu-id="8a89f-106">Sync-AzAnalysisServicesInstance-cmdleten synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla förekomster av den aktuella inloggade miljön enligt vad som anges i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="8a89f-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8a89f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a89f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a89f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a89f-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8a89f-109">Det här kommandot synkroniserar databasen med namnet SalesOrders i servern med namnet "contoso" i miljön westus.asazure.windows.net förutsatt att användaren har loggat in på den här miljön med kommandot Add-AzAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="8a89f-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8a89f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a89f-110">PARAMETERS</span></span>

### <span data-ttu-id="8a89f-111">-Databas</span><span class="sxs-lookup"><span data-stu-id="8a89f-111">-Database</span></span>

<span data-ttu-id="8a89f-112">Identitet för databasen som ska synkroniseras</span><span class="sxs-lookup"><span data-stu-id="8a89f-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89f-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="8a89f-113">-Instance</span></span>

<span data-ttu-id="8a89f-114">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="8a89f-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8a89f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a89f-115">-PassThru</span></span>

<span data-ttu-id="8a89f-116">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="8a89f-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8a89f-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a89f-117">-Confirm</span></span>
<span data-ttu-id="8a89f-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a89f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a89f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a89f-119">-WhatIf</span></span>
<span data-ttu-id="8a89f-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a89f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a89f-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a89f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a89f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a89f-122">CommonParameters</span></span>
<span data-ttu-id="8a89f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a89f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a89f-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a89f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a89f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a89f-125">INPUTS</span></span>

### <span data-ttu-id="8a89f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a89f-126">System.String</span></span>

## <span data-ttu-id="8a89f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a89f-127">OUTPUTS</span></span>

### <span data-ttu-id="8a89f-128">Microsoft. Azure. commands. AnalysisServices. Dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8a89f-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8a89f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a89f-129">NOTES</span></span>

<span data-ttu-id="8a89f-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8a89f-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8a89f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a89f-131">RELATED LINKS</span></span>
