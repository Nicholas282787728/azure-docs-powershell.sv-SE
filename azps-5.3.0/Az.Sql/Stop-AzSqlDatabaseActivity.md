---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522768"
---
# <span data-ttu-id="f4d9a-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="f4d9a-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="f4d9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d9a-103">Avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="f4d9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4d9a-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d9a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d9a-106">Cmdleten **Stop-AzSqlDatabaseActivity** avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="f4d9a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d9a-108">Exempel 1: Avbryt den asynkrona uppdateringen i databasen</span><span class="sxs-lookup"><span data-stu-id="f4d9a-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="f4d9a-109">Det här kommandot avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="f4d9a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d9a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4d9a-111">-DatabaseName</span></span>
<span data-ttu-id="f4d9a-112">Anger namnet på den databas där denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="f4d9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d9a-113">-DefaultProfile</span></span>
<span data-ttu-id="f4d9a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d9a-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f4d9a-115">-ElasticPoolName</span></span>
<span data-ttu-id="f4d9a-116">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="f4d9a-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f4d9a-117">-OperationId</span></span>
<span data-ttu-id="f4d9a-118">Anger ID för den operation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4d9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4d9a-120">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f4d9a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4d9a-121">-ServerName</span></span>
<span data-ttu-id="f4d9a-122">Anger namnet på den Microsoft SQL Server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="f4d9a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4d9a-123">-Confirm</span></span>
<span data-ttu-id="f4d9a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d9a-125">-WhatIf</span></span>
<span data-ttu-id="f4d9a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d9a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d9a-128">CommonParameters</span></span>
<span data-ttu-id="f4d9a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d9a-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4d9a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d9a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4d9a-131">INPUTS</span></span>

### <span data-ttu-id="f4d9a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d9a-132">System.String</span></span>

### <span data-ttu-id="f4d9a-133">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4d9a-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4d9a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4d9a-134">OUTPUTS</span></span>

### <span data-ttu-id="f4d9a-135">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="f4d9a-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="f4d9a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4d9a-136">NOTES</span></span>

## <span data-ttu-id="f4d9a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4d9a-137">RELATED LINKS</span></span>
