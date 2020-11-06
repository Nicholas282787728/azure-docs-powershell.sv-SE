---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 5ceee1509ed5c47611f68645a6cf1665b9df8408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576015"
---
# <span data-ttu-id="56523-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="56523-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56523-102">SYNOPSIS</span></span>
<span data-ttu-id="56523-103">Avbryter en SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="56523-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56523-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56523-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56523-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56523-105">DESCRIPTION</span></span>
<span data-ttu-id="56523-106">Cmdleten **suspend-AzureRmSqlDatabase** inaktive ras en Azure SQL Data Warehouse-databas.</span><span class="sxs-lookup"><span data-stu-id="56523-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="56523-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56523-107">EXAMPLES</span></span>

### <span data-ttu-id="56523-108">Exempel 1: inaktiverar en Azure SQL Data Warehouse-databas</span><span class="sxs-lookup"><span data-stu-id="56523-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="56523-109">Det här kommandot gör att en Active Azure SQL Data Warehouse-databas stoppas.</span><span class="sxs-lookup"><span data-stu-id="56523-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="56523-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56523-110">PARAMETERS</span></span>

### <span data-ttu-id="56523-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56523-111">-AsJob</span></span>
<span data-ttu-id="56523-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="56523-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56523-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56523-113">-DatabaseName</span></span>
<span data-ttu-id="56523-114">Anger namnet på den databas som denna cmdlet gör paus för.</span><span class="sxs-lookup"><span data-stu-id="56523-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="56523-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56523-115">-DefaultProfile</span></span>
<span data-ttu-id="56523-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="56523-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56523-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56523-117">-ResourceGroupName</span></span>
<span data-ttu-id="56523-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="56523-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="56523-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56523-119">-ServerName</span></span>
<span data-ttu-id="56523-120">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="56523-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="56523-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56523-121">-Confirm</span></span>
<span data-ttu-id="56523-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56523-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56523-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56523-123">-WhatIf</span></span>
<span data-ttu-id="56523-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56523-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56523-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56523-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56523-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56523-126">CommonParameters</span></span>
<span data-ttu-id="56523-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56523-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56523-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56523-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56523-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56523-129">INPUTS</span></span>

### <span data-ttu-id="56523-130">System. String</span><span class="sxs-lookup"><span data-stu-id="56523-130">System.String</span></span>

## <span data-ttu-id="56523-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56523-131">OUTPUTS</span></span>

### <span data-ttu-id="56523-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="56523-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="56523-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56523-133">NOTES</span></span>
* <span data-ttu-id="56523-134">Cmdleten **suspend-AzureRmSqlDatabase** fungerar bara i Azure SQL Data Warehouse-databaser.</span><span class="sxs-lookup"><span data-stu-id="56523-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="56523-135">Den här åtgärden stöds inte i SQL-databaserna Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="56523-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="56523-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56523-136">RELATED LINKS</span></span>

[<span data-ttu-id="56523-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="56523-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="56523-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="56523-140">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="56523-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="56523-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="56523-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="56523-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


