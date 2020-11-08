---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090922"
---
# <span data-ttu-id="e563c-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e563c-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="e563c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e563c-102">SYNOPSIS</span></span>
<span data-ttu-id="e563c-103">Tar bort en given återställnings punkt från en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e563c-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="e563c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e563c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e563c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e563c-105">DESCRIPTION</span></span>
<span data-ttu-id="e563c-106">Cmdleten **Remove-AzSqlDatabaseRestorePoint** tar bort en återställnings punkt från en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e563c-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="e563c-107">Denna cmdlet stöds för närvarande av SQL Server DataWarehouse-tjänsten i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e563c-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="e563c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e563c-108">EXAMPLES</span></span>

### <span data-ttu-id="e563c-109">Exempel 1: tar bort en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="e563c-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="e563c-110">Det här kommandot tar bort en återställnings punkt för en Azure SQL-databas skapad.</span><span class="sxs-lookup"><span data-stu-id="e563c-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="e563c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e563c-111">PARAMETERS</span></span>

### <span data-ttu-id="e563c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e563c-112">-DatabaseName</span></span>
<span data-ttu-id="e563c-113">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e563c-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e563c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e563c-114">-DefaultProfile</span></span>
<span data-ttu-id="e563c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e563c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e563c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e563c-116">-PassThru</span></span>
<span data-ttu-id="e563c-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e563c-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e563c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e563c-118">-ResourceGroupName</span></span>
<span data-ttu-id="e563c-119">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="e563c-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="e563c-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="e563c-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="e563c-121">Anger det datum då återställnings punkten skapades.</span><span class="sxs-lookup"><span data-stu-id="e563c-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e563c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e563c-122">-ServerName</span></span>
<span data-ttu-id="e563c-123">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="e563c-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e563c-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e563c-124">-Confirm</span></span>
<span data-ttu-id="e563c-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e563c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e563c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e563c-126">-WhatIf</span></span>
<span data-ttu-id="e563c-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e563c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e563c-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e563c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e563c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e563c-129">CommonParameters</span></span>
<span data-ttu-id="e563c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e563c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e563c-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e563c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e563c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e563c-132">INPUTS</span></span>

### <span data-ttu-id="e563c-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e563c-133">System.DateTime</span></span>

### <span data-ttu-id="e563c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e563c-134">System.String</span></span>

## <span data-ttu-id="e563c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e563c-135">OUTPUTS</span></span>

### <span data-ttu-id="e563c-136">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="e563c-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="e563c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e563c-137">NOTES</span></span>

## <span data-ttu-id="e563c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e563c-138">RELATED LINKS</span></span>
