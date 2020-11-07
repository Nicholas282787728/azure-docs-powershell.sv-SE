---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746460"
---
# <span data-ttu-id="7df35-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="7df35-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="7df35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7df35-102">SYNOPSIS</span></span>
<span data-ttu-id="7df35-103">Avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="7df35-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7df35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7df35-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df35-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7df35-105">DESCRIPTION</span></span>
<span data-ttu-id="7df35-106">Cmdleten **Stop-AzSqlDatabaseActivity** avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="7df35-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7df35-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7df35-107">EXAMPLES</span></span>

### <span data-ttu-id="7df35-108">Exempel 1: Avbryt den asynkrona uppdateringen i databasen</span><span class="sxs-lookup"><span data-stu-id="7df35-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="7df35-109">Det här kommandot avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="7df35-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7df35-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7df35-110">PARAMETERS</span></span>

### <span data-ttu-id="7df35-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7df35-111">-DatabaseName</span></span>
<span data-ttu-id="7df35-112">Anger namnet på den databas där denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="7df35-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="7df35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df35-113">-DefaultProfile</span></span>
<span data-ttu-id="7df35-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7df35-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7df35-115">-ElasticPoolName</span></span>
<span data-ttu-id="7df35-116">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="7df35-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7df35-117">-OperationId</span></span>
<span data-ttu-id="7df35-118">Anger ID för den operation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="7df35-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df35-119">-ResourceGroupName</span></span>
<span data-ttu-id="7df35-120">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="7df35-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7df35-121">-ServerName</span></span>
<span data-ttu-id="7df35-122">Anger namnet på den Microsoft SQL Server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="7df35-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7df35-123">-Confirm</span></span>
<span data-ttu-id="7df35-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7df35-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df35-125">-WhatIf</span></span>
<span data-ttu-id="7df35-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7df35-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df35-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7df35-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df35-128">CommonParameters</span></span>
<span data-ttu-id="7df35-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df35-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df35-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df35-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7df35-131">INPUTS</span></span>

### <span data-ttu-id="7df35-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7df35-132">System.String</span></span>

### <span data-ttu-id="7df35-133">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7df35-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7df35-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7df35-134">OUTPUTS</span></span>

### <span data-ttu-id="7df35-135">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="7df35-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="7df35-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7df35-136">NOTES</span></span>

## <span data-ttu-id="7df35-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7df35-137">RELATED LINKS</span></span>
