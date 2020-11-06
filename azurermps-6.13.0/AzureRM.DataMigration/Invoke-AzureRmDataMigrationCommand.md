---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580120"
---
# <span data-ttu-id="2ab2c-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="2ab2c-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="2ab2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ab2c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab2c-103">Skapar ett nytt kommando som ska utföras på en befintlig DMS-uppgift.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ab2c-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ab2c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab2c-106">New-AzureRmDataMigrationCommand-cmdleten skapar en ny kommando aktivitet som ska köras på en befintlig migrering.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="2ab2c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ab2c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab2c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ab2c-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="2ab2c-109">I exemplen ovan används New-AzureRmDmsCommand cmdlet för att skapa ett kommando för en befintlig tjänst, projekt och aktivitet</span><span class="sxs-lookup"><span data-stu-id="2ab2c-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="2ab2c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ab2c-110">PARAMETERS</span></span>

### <span data-ttu-id="2ab2c-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="2ab2c-111">-CommandType</span></span>
<span data-ttu-id="2ab2c-112">Kommando typ.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-112">Command Type.</span></span>

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

### <span data-ttu-id="2ab2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab2c-113">-DefaultProfile</span></span>
<span data-ttu-id="2ab2c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab2c-115">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="2ab2c-115">-ProjectName</span></span>
<span data-ttu-id="2ab2c-116">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-116">The name of the project.</span></span>

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

### <span data-ttu-id="2ab2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2ab2c-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ab2c-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2ab2c-119">-ServiceName</span></span>
<span data-ttu-id="2ab2c-120">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2ab2c-121">-Aktivitets namn</span><span class="sxs-lookup"><span data-stu-id="2ab2c-121">-TaskName</span></span>
<span data-ttu-id="2ab2c-122">Namnet på den uppgift som kommandot körs på.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="2ab2c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ab2c-123">-Confirm</span></span>
<span data-ttu-id="2ab2c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ab2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab2c-125">-WhatIf</span></span>
<span data-ttu-id="2ab2c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ab2c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ab2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab2c-128">CommonParameters</span></span>
<span data-ttu-id="2ab2c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab2c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab2c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab2c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ab2c-131">INPUTS</span></span>

### <span data-ttu-id="2ab2c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ab2c-132">System.String</span></span>

## <span data-ttu-id="2ab2c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ab2c-133">OUTPUTS</span></span>

### <span data-ttu-id="2ab2c-134">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="2ab2c-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="2ab2c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ab2c-135">NOTES</span></span>

## <span data-ttu-id="2ab2c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ab2c-136">RELATED LINKS</span></span>
