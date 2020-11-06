---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583735"
---
# <span data-ttu-id="5c55b-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="5c55b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c55b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c55b-103">Avbryter en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="5c55b-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c55b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c55b-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c55b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c55b-105">DESCRIPTION</span></span>
<span data-ttu-id="5c55b-106">Cmdleten **suspend-AzureRmSqlDatabase** inaktive ras en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="5c55b-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="5c55b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c55b-107">EXAMPLES</span></span>

### <span data-ttu-id="5c55b-108">Exempel 1: inaktiverar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="5c55b-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5c55b-109">Det här kommandot gör att en Active Azure SQL Data Warehouse-databas stoppas.</span><span class="sxs-lookup"><span data-stu-id="5c55b-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="5c55b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c55b-110">PARAMETERS</span></span>

### <span data-ttu-id="5c55b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c55b-111">-DatabaseName</span></span>
<span data-ttu-id="5c55b-112">Anger namnet på den databas som denna cmdlet gör paus för.</span><span class="sxs-lookup"><span data-stu-id="5c55b-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="5c55b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c55b-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c55b-114">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="5c55b-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5c55b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c55b-115">-ServerName</span></span>
<span data-ttu-id="5c55b-116">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="5c55b-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="5c55b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c55b-117">-Confirm</span></span>
<span data-ttu-id="5c55b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c55b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c55b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c55b-119">-WhatIf</span></span>
<span data-ttu-id="5c55b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c55b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c55b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c55b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c55b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c55b-122">-DefaultProfile</span></span>
<span data-ttu-id="5c55b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c55b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c55b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c55b-124">CommonParameters</span></span>
<span data-ttu-id="5c55b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c55b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c55b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c55b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c55b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c55b-127">INPUTS</span></span>

### <span data-ttu-id="5c55b-128">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5c55b-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5c55b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c55b-129">OUTPUTS</span></span>

### <span data-ttu-id="5c55b-130">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5c55b-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5c55b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c55b-131">NOTES</span></span>
* <span data-ttu-id="5c55b-132">Cmdleten **suspend-AzureRmSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="5c55b-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="5c55b-133">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="5c55b-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="5c55b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c55b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c55b-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c55b-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c55b-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c55b-138">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c55b-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c55b-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c55b-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5c55b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


