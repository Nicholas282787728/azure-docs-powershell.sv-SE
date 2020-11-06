---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574108"
---
# <span data-ttu-id="d2529-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="d2529-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="d2529-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2529-102">SYNOPSIS</span></span>

<span data-ttu-id="d2529-103">Synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla instanser av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="d2529-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2529-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2529-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2529-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2529-105">DESCRIPTION</span></span>

<span data-ttu-id="d2529-106">Sync-AzureAnalysisServicesInstance-cmdleten synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla förekomster av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="d2529-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d2529-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2529-107">EXAMPLES</span></span>

### <span data-ttu-id="d2529-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d2529-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="d2529-109">Det här kommandot synkroniserar databasen med namnet SalesOrders i servern med namnet "contoso" i miljön westus.asazure.windows.net förutsatt att användaren har loggat in på den här enviroment med kommandot Add-AzureAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="d2529-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="d2529-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2529-110">PARAMETERS</span></span>

### <span data-ttu-id="d2529-111">-Databas</span><span class="sxs-lookup"><span data-stu-id="d2529-111">-Database</span></span>

<span data-ttu-id="d2529-112">Identitet för databasen som ska synkroniseras</span><span class="sxs-lookup"><span data-stu-id="d2529-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="d2529-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="d2529-113">-Instance</span></span>

<span data-ttu-id="d2529-114">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="d2529-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="d2529-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2529-115">-PassThru</span></span>

<span data-ttu-id="d2529-116">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="d2529-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d2529-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2529-117">-Confirm</span></span>
<span data-ttu-id="d2529-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2529-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2529-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2529-119">-WhatIf</span></span>
<span data-ttu-id="d2529-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2529-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2529-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2529-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2529-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2529-122">CommonParameters</span></span>
<span data-ttu-id="d2529-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2529-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2529-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2529-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2529-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2529-125">INPUTS</span></span>

### <span data-ttu-id="d2529-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d2529-126">System.String</span></span>
<span data-ttu-id="d2529-127">Parametrar: databas (ByValue), instans (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2529-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="d2529-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2529-128">OUTPUTS</span></span>

### <span data-ttu-id="d2529-129">Microsoft. Azure. commands. AnalysisServices. Dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="d2529-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="d2529-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2529-130">NOTES</span></span>

<span data-ttu-id="d2529-131">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="d2529-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="d2529-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2529-132">RELATED LINKS</span></span>
