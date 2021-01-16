---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401539"
---
# <span data-ttu-id="f8ded-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="f8ded-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="f8ded-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8ded-102">SYNOPSIS</span></span>

<span data-ttu-id="f8ded-103">Synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla instanser av den aktuella inloggade miljön enligt vad som anges i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="f8ded-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f8ded-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8ded-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ded-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8ded-105">DESCRIPTION</span></span>

<span data-ttu-id="f8ded-106">Sync-AzAnalysisServicesInstance-cmdleten synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla förekomster av den aktuella inloggade miljön enligt vad som anges i Add-AzAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="f8ded-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f8ded-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8ded-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ded-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8ded-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="f8ded-109">Det här kommandot synkroniserar databasen med namnet SalesOrders i servern med namnet "contoso" i miljön westus.asazure.windows.net förutsatt att användaren har loggat in på den här miljön med kommandot Add-AzAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="f8ded-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="f8ded-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8ded-110">PARAMETERS</span></span>

### <span data-ttu-id="f8ded-111">-Databas</span><span class="sxs-lookup"><span data-stu-id="f8ded-111">-Database</span></span>

<span data-ttu-id="f8ded-112">Identitet för databasen som ska synkroniseras</span><span class="sxs-lookup"><span data-stu-id="f8ded-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="f8ded-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="f8ded-113">-Instance</span></span>

<span data-ttu-id="f8ded-114">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="f8ded-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="f8ded-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8ded-115">-PassThru</span></span>

<span data-ttu-id="f8ded-116">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="f8ded-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f8ded-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8ded-117">-Confirm</span></span>
<span data-ttu-id="f8ded-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8ded-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ded-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ded-119">-WhatIf</span></span>
<span data-ttu-id="f8ded-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8ded-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8ded-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8ded-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ded-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ded-122">CommonParameters</span></span>
<span data-ttu-id="f8ded-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ded-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ded-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ded-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ded-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8ded-125">INPUTS</span></span>

### <span data-ttu-id="f8ded-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8ded-126">System.String</span></span>

## <span data-ttu-id="f8ded-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8ded-127">OUTPUTS</span></span>

### <span data-ttu-id="f8ded-128">Microsoft. Azure. commands. AnalysisServices. Dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="f8ded-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="f8ded-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8ded-129">NOTES</span></span>

<span data-ttu-id="f8ded-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="f8ded-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="f8ded-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8ded-131">RELATED LINKS</span></span>
