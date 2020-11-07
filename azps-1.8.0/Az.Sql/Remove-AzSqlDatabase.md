---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 200e53ef1f23c4b829380a2c8b7ca663443e5f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746590"
---
# <span data-ttu-id="00188-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="00188-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00188-102">SYNOPSIS</span></span>
<span data-ttu-id="00188-103">Tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="00188-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="00188-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00188-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00188-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00188-105">DESCRIPTION</span></span>
<span data-ttu-id="00188-106">Cmdleten **Remove-AzSqlDatabase** tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="00188-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="00188-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="00188-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="00188-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00188-108">EXAMPLES</span></span>

### <span data-ttu-id="00188-109">Exempel 1: ta bort en databas från en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="00188-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="00188-110">Det här kommandot tar bort databasen som heter Database01 från Server Server01.</span><span class="sxs-lookup"><span data-stu-id="00188-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="00188-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00188-111">PARAMETERS</span></span>

### <span data-ttu-id="00188-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00188-112">-DatabaseName</span></span>
<span data-ttu-id="00188-113">Anger namnet på den databas som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="00188-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00188-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00188-114">-DefaultProfile</span></span>
<span data-ttu-id="00188-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00188-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00188-116">-Force</span><span class="sxs-lookup"><span data-stu-id="00188-116">-Force</span></span>
<span data-ttu-id="00188-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="00188-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00188-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00188-118">-ResourceGroupName</span></span>
<span data-ttu-id="00188-119">Anger namnet på den Azure Resource-grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="00188-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="00188-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="00188-120">-ServerName</span></span>
<span data-ttu-id="00188-121">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="00188-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="00188-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00188-122">-Confirm</span></span>
<span data-ttu-id="00188-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00188-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00188-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00188-124">-WhatIf</span></span>
<span data-ttu-id="00188-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00188-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00188-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00188-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00188-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00188-127">CommonParameters</span></span>
<span data-ttu-id="00188-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00188-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00188-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00188-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00188-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00188-130">INPUTS</span></span>

### <span data-ttu-id="00188-131">System. String</span><span class="sxs-lookup"><span data-stu-id="00188-131">System.String</span></span>

## <span data-ttu-id="00188-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00188-132">OUTPUTS</span></span>

### <span data-ttu-id="00188-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="00188-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="00188-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00188-134">NOTES</span></span>

## <span data-ttu-id="00188-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00188-135">RELATED LINKS</span></span>

[<span data-ttu-id="00188-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="00188-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="00188-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="00188-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="00188-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00188-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="00188-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="00188-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

