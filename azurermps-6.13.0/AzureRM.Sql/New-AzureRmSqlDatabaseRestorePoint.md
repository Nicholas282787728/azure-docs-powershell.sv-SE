---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: dad714b617f6b3c493d19b2275dcf7eeef14a2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578772"
---
# <span data-ttu-id="b49c2-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b49c2-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="b49c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b49c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b49c2-103">Skapar en ny återställnings punkt från vilken en SQL-databas kan återställas.</span><span class="sxs-lookup"><span data-stu-id="b49c2-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b49c2-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b49c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b49c2-105">DESCRIPTION</span></span>
<span data-ttu-id="b49c2-106">Cmdleten **New-AzureRmSqlDatabaseRestorePoint** skapar en ny återställnings punkt som ett Azure SQL data-lager kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="b49c2-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="b49c2-107">Denna cmdlet stöds för närvarande för Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="b49c2-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="b49c2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b49c2-108">EXAMPLES</span></span>

### <span data-ttu-id="b49c2-109">Exempel 1: skapa en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="b49c2-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="b49c2-110">Det här kommandot skapar en återställnings punkt för Azure SQL Data Warehouse och returnerar information om återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="b49c2-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="b49c2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b49c2-111">PARAMETERS</span></span>

### <span data-ttu-id="b49c2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b49c2-112">-DatabaseName</span></span>
<span data-ttu-id="b49c2-113">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b49c2-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="b49c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49c2-114">-DefaultProfile</span></span>
<span data-ttu-id="b49c2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b49c2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b49c2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49c2-116">-ResourceGroupName</span></span>
<span data-ttu-id="b49c2-117">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="b49c2-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b49c2-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="b49c2-118">-RestorePointLabel</span></span>
<span data-ttu-id="b49c2-119">Anger etiketten för återställnings punkten så att den blir lätt att identifiera.</span><span class="sxs-lookup"><span data-stu-id="b49c2-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="b49c2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b49c2-120">-ServerName</span></span>
<span data-ttu-id="b49c2-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="b49c2-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="b49c2-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b49c2-122">-Confirm</span></span>
<span data-ttu-id="b49c2-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b49c2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49c2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49c2-124">-WhatIf</span></span>
<span data-ttu-id="b49c2-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b49c2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49c2-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b49c2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b49c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49c2-127">CommonParameters</span></span>
<span data-ttu-id="b49c2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49c2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49c2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b49c2-130">INPUTS</span></span>

### <span data-ttu-id="b49c2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b49c2-131">System.String</span></span>

## <span data-ttu-id="b49c2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b49c2-132">OUTPUTS</span></span>

### <span data-ttu-id="b49c2-133">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="b49c2-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="b49c2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b49c2-134">NOTES</span></span>

## <span data-ttu-id="b49c2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b49c2-135">RELATED LINKS</span></span>