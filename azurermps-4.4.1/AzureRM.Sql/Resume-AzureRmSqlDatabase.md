---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586152"
---
# <span data-ttu-id="09730-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="09730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09730-102">SYNOPSIS</span></span>
<span data-ttu-id="09730-103">Återupptar en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="09730-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09730-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09730-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09730-105">DESCRIPTION</span></span>
<span data-ttu-id="09730-106">Cmdleten **Resume-AzureRmSqlDatabase** återupptar en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="09730-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="09730-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09730-107">EXAMPLES</span></span>

### <span data-ttu-id="09730-108">Exempel 1: återupptar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="09730-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="09730-109">Det här kommandot återupptar en upplåst Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="09730-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="09730-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09730-110">PARAMETERS</span></span>

### <span data-ttu-id="09730-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09730-111">-DatabaseName</span></span>
<span data-ttu-id="09730-112">Anger namnet på den databas som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="09730-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="09730-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09730-113">-ResourceGroupName</span></span>
<span data-ttu-id="09730-114">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="09730-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="09730-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09730-115">-ServerName</span></span>
<span data-ttu-id="09730-116">Anger namnet på den server som är värd för databasen som denna cmdlet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="09730-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="09730-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09730-117">-Confirm</span></span>
<span data-ttu-id="09730-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09730-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09730-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09730-119">-WhatIf</span></span>
<span data-ttu-id="09730-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09730-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09730-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09730-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09730-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09730-122">-DefaultProfile</span></span>
<span data-ttu-id="09730-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09730-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09730-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09730-124">CommonParameters</span></span>
<span data-ttu-id="09730-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09730-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09730-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09730-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09730-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09730-127">INPUTS</span></span>

### <span data-ttu-id="09730-128">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="09730-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="09730-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09730-129">OUTPUTS</span></span>

### <span data-ttu-id="09730-130">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="09730-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="09730-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09730-131">NOTES</span></span>
* <span data-ttu-id="09730-132">Cmdleten **Resume-AzureRmSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="09730-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="09730-133">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="09730-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="09730-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09730-134">RELATED LINKS</span></span>

[<span data-ttu-id="09730-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="09730-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="09730-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="09730-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="09730-139">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09730-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="09730-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="09730-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


