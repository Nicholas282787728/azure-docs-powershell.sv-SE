---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090195"
---
# <span data-ttu-id="c59bc-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c59bc-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="c59bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c59bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c59bc-103">Skapar en ny återställnings punkt från vilken en SQL-databas kan återställas.</span><span class="sxs-lookup"><span data-stu-id="c59bc-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="c59bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c59bc-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c59bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c59bc-105">DESCRIPTION</span></span>
<span data-ttu-id="c59bc-106">Cmdleten **New-AzSqlDatabaseRestorePoint** skapar en ny återställnings punkt som ett Azure SQL data-lager kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="c59bc-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="c59bc-107">Denna cmdlet stöds för närvarande för Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="c59bc-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="c59bc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c59bc-108">EXAMPLES</span></span>

### <span data-ttu-id="c59bc-109">Exempel 1: skapa en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="c59bc-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="c59bc-110">Det här kommandot skapar en återställnings punkt för Azure SQL Data Warehouse och returnerar information om återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="c59bc-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="c59bc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c59bc-111">PARAMETERS</span></span>

### <span data-ttu-id="c59bc-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c59bc-112">-DatabaseName</span></span>
<span data-ttu-id="c59bc-113">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="c59bc-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="c59bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59bc-114">-DefaultProfile</span></span>
<span data-ttu-id="c59bc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c59bc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c59bc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59bc-116">-ResourceGroupName</span></span>
<span data-ttu-id="c59bc-117">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c59bc-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="c59bc-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="c59bc-118">-RestorePointLabel</span></span>
<span data-ttu-id="c59bc-119">Anger etiketten för återställnings punkten så att den blir lätt att identifiera.</span><span class="sxs-lookup"><span data-stu-id="c59bc-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="c59bc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c59bc-120">-ServerName</span></span>
<span data-ttu-id="c59bc-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="c59bc-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="c59bc-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c59bc-122">-Confirm</span></span>
<span data-ttu-id="c59bc-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c59bc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59bc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59bc-124">-WhatIf</span></span>
<span data-ttu-id="c59bc-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c59bc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59bc-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c59bc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59bc-127">CommonParameters</span></span>
<span data-ttu-id="c59bc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59bc-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c59bc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59bc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c59bc-130">INPUTS</span></span>

### <span data-ttu-id="c59bc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c59bc-131">System.String</span></span>

## <span data-ttu-id="c59bc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c59bc-132">OUTPUTS</span></span>

### <span data-ttu-id="c59bc-133">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="c59bc-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="c59bc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c59bc-134">NOTES</span></span>

## <span data-ttu-id="c59bc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c59bc-135">RELATED LINKS</span></span>
