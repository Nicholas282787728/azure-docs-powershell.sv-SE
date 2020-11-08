---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090292"
---
# <span data-ttu-id="11786-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="11786-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="11786-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11786-102">SYNOPSIS</span></span>
<span data-ttu-id="11786-103">Skapar ett nytt kommando som ska utföras på en befintlig DMS-uppgift.</span><span class="sxs-lookup"><span data-stu-id="11786-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="11786-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11786-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="11786-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11786-105">DESCRIPTION</span></span>
<span data-ttu-id="11786-106">Invoke-AzDataMigrationCommand-cmdleten skapar en ny kommando aktivitet som ska köras på en befintlig migrering.</span><span class="sxs-lookup"><span data-stu-id="11786-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="11786-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11786-107">EXAMPLES</span></span>

### <span data-ttu-id="11786-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11786-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="11786-109">I exemplen ovan används Invoke-AzDataMigrationCommand cmdlet för att skapa ett kommando för en befintlig tjänst, projekt och aktivitet</span><span class="sxs-lookup"><span data-stu-id="11786-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="11786-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11786-110">PARAMETERS</span></span>

### <span data-ttu-id="11786-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="11786-111">-CommandType</span></span>
<span data-ttu-id="11786-112">Kommando typ.</span><span class="sxs-lookup"><span data-stu-id="11786-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11786-113">-DefaultProfile</span></span>
<span data-ttu-id="11786-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11786-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11786-115">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="11786-115">-ProjectName</span></span>
<span data-ttu-id="11786-116">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="11786-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11786-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11786-117">-ResourceGroupName</span></span>
<span data-ttu-id="11786-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="11786-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11786-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11786-119">-ServiceName</span></span>
<span data-ttu-id="11786-120">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="11786-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11786-121">-Aktivitets namn</span><span class="sxs-lookup"><span data-stu-id="11786-121">-TaskName</span></span>
<span data-ttu-id="11786-122">Namnet på den uppgift som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="11786-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="11786-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="11786-123">-ObjectName</span></span>
<span data-ttu-id="11786-124">Namnet på det databas objekt som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="11786-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="11786-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11786-125">-Confirm</span></span>
<span data-ttu-id="11786-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11786-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11786-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11786-127">-WhatIf</span></span>
<span data-ttu-id="11786-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11786-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11786-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11786-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11786-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11786-130">CommonParameters</span></span>
<span data-ttu-id="11786-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11786-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11786-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11786-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11786-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11786-133">INPUTS</span></span>

### <span data-ttu-id="11786-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11786-134">System.String</span></span>

## <span data-ttu-id="11786-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11786-135">OUTPUTS</span></span>

### <span data-ttu-id="11786-136">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="11786-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="11786-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11786-137">NOTES</span></span>

## <span data-ttu-id="11786-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11786-138">RELATED LINKS</span></span>