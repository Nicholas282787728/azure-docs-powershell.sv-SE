---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260020"
---
# <span data-ttu-id="182a0-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="182a0-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="182a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="182a0-102">SYNOPSIS</span></span>
<span data-ttu-id="182a0-103">Skapar ett nytt kommando som ska utföras på en befintlig DMS-uppgift.</span><span class="sxs-lookup"><span data-stu-id="182a0-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="182a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="182a0-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="182a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="182a0-105">DESCRIPTION</span></span>
<span data-ttu-id="182a0-106">Invoke-AzDataMigrationCommand-cmdleten skapar en ny kommando aktivitet som ska köras på en befintlig migrering.</span><span class="sxs-lookup"><span data-stu-id="182a0-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="182a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="182a0-107">EXAMPLES</span></span>

### <span data-ttu-id="182a0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="182a0-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="182a0-109">I exemplen ovan används Invoke-AzDataMigrationCommand cmdlet för att skapa ett kommando för en befintlig tjänst, projekt och aktivitet</span><span class="sxs-lookup"><span data-stu-id="182a0-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="182a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="182a0-110">PARAMETERS</span></span>

### <span data-ttu-id="182a0-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="182a0-111">-CommandType</span></span>
<span data-ttu-id="182a0-112">Kommando typ.</span><span class="sxs-lookup"><span data-stu-id="182a0-112">Command Type.</span></span>

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

### <span data-ttu-id="182a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182a0-113">-DefaultProfile</span></span>
<span data-ttu-id="182a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="182a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="182a0-115">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="182a0-115">-ProjectName</span></span>
<span data-ttu-id="182a0-116">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="182a0-116">The name of the project.</span></span>

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

### <span data-ttu-id="182a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="182a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="182a0-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="182a0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="182a0-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="182a0-119">-ServiceName</span></span>
<span data-ttu-id="182a0-120">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="182a0-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="182a0-121">-Aktivitets namn</span><span class="sxs-lookup"><span data-stu-id="182a0-121">-TaskName</span></span>
<span data-ttu-id="182a0-122">Namnet på den uppgift som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="182a0-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="182a0-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="182a0-123">-ObjectName</span></span>
<span data-ttu-id="182a0-124">Namnet på det databas objekt som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="182a0-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="182a0-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="182a0-125">-Confirm</span></span>
<span data-ttu-id="182a0-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="182a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="182a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="182a0-127">-WhatIf</span></span>
<span data-ttu-id="182a0-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="182a0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="182a0-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="182a0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="182a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182a0-130">CommonParameters</span></span>
<span data-ttu-id="182a0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="182a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182a0-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182a0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182a0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="182a0-133">INPUTS</span></span>

### <span data-ttu-id="182a0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="182a0-134">System.String</span></span>

## <span data-ttu-id="182a0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="182a0-135">OUTPUTS</span></span>

### <span data-ttu-id="182a0-136">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="182a0-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="182a0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="182a0-137">NOTES</span></span>

## <span data-ttu-id="182a0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="182a0-138">RELATED LINKS</span></span>
