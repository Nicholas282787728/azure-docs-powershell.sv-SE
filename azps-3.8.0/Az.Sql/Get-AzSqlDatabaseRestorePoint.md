---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089353"
---
# <span data-ttu-id="b7d8f-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b7d8f-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="b7d8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d8f-103">Hämtar de distinkta återställnings punkter från vilka ett SQL-datalager kan återställas.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="b7d8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7d8f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d8f-106">Cmdleten **Get-AzSqlDatabaseRestorePoint** hämtar de distinkta återställnings punkter som ett Azure SQL data-lager kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="b7d8f-107">För en Azure SQL-databas är återställnings fönstret kontinuerligt.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="b7d8f-108">Det innebär att alla tidpunkter i databasens bevarande period kan användas som återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="b7d8f-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b7d8f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7d8f-110">EXAMPLES</span></span>

### <span data-ttu-id="b7d8f-111">Exempel 1: Hämta alla återställnings punkter</span><span class="sxs-lookup"><span data-stu-id="b7d8f-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="b7d8f-112">Det här kommandot returnerar alla tillgängliga återställnings punkter för den Azure SQL-databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="b7d8f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="b7d8f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7d8f-114">-DatabaseName</span></span>
<span data-ttu-id="b7d8f-115">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="b7d8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d8f-116">-DefaultProfile</span></span>
<span data-ttu-id="b7d8f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7d8f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7d8f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d8f-118">-ResourceGroupName</span></span>
<span data-ttu-id="b7d8f-119">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b7d8f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7d8f-120">-ServerName</span></span>
<span data-ttu-id="b7d8f-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="b7d8f-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7d8f-122">-Confirm</span></span>
<span data-ttu-id="b7d8f-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d8f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d8f-124">-WhatIf</span></span>
<span data-ttu-id="b7d8f-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d8f-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d8f-127">CommonParameters</span></span>
<span data-ttu-id="b7d8f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d8f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7d8f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d8f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7d8f-130">INPUTS</span></span>

### <span data-ttu-id="b7d8f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b7d8f-131">System.String</span></span>

## <span data-ttu-id="b7d8f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7d8f-132">OUTPUTS</span></span>

### <span data-ttu-id="b7d8f-133">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="b7d8f-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="b7d8f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7d8f-134">NOTES</span></span>

## <span data-ttu-id="b7d8f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7d8f-135">RELATED LINKS</span></span>
