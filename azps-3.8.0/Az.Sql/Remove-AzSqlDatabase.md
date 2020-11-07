---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926378"
---
# <span data-ttu-id="1c777-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="1c777-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c777-102">SYNOPSIS</span></span>
<span data-ttu-id="1c777-103">Tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1c777-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="1c777-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c777-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c777-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c777-105">DESCRIPTION</span></span>
<span data-ttu-id="1c777-106">Cmdleten **Remove-AzSqlDatabase** tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1c777-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="1c777-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="1c777-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1c777-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c777-108">EXAMPLES</span></span>

### <span data-ttu-id="1c777-109">Exempel 1: ta bort en databas från en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="1c777-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1c777-110">Det här kommandot tar bort databasen som heter Database01 från Server Server01.</span><span class="sxs-lookup"><span data-stu-id="1c777-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="1c777-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c777-111">PARAMETERS</span></span>

### <span data-ttu-id="1c777-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c777-112">-DatabaseName</span></span>
<span data-ttu-id="1c777-113">Anger namnet på den databas som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1c777-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c777-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c777-114">-DefaultProfile</span></span>
<span data-ttu-id="1c777-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c777-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c777-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1c777-116">-Force</span></span>
<span data-ttu-id="1c777-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1c777-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c777-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c777-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c777-119">Anger namnet på den Azure Resource-grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="1c777-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1c777-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c777-120">-ServerName</span></span>
<span data-ttu-id="1c777-121">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="1c777-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1c777-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c777-122">-Confirm</span></span>
<span data-ttu-id="1c777-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c777-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c777-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c777-124">-WhatIf</span></span>
<span data-ttu-id="1c777-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c777-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c777-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c777-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c777-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c777-127">CommonParameters</span></span>
<span data-ttu-id="1c777-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c777-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c777-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c777-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c777-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c777-130">INPUTS</span></span>

### <span data-ttu-id="1c777-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c777-131">System.String</span></span>

## <span data-ttu-id="1c777-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c777-132">OUTPUTS</span></span>

### <span data-ttu-id="1c777-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1c777-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1c777-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c777-134">NOTES</span></span>

## <span data-ttu-id="1c777-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c777-135">RELATED LINKS</span></span>

[<span data-ttu-id="1c777-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1c777-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="1c777-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1c777-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1c777-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1c777-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1c777-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1c777-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


