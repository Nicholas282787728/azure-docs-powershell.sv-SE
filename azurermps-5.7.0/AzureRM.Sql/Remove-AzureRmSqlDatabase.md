---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579284"
---
# <span data-ttu-id="08ad8-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="08ad8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="08ad8-103">Tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="08ad8-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08ad8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08ad8-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08ad8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="08ad8-106">Cmdleten **Remove-AzureRmSqlDatabase** tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="08ad8-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="08ad8-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="08ad8-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="08ad8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08ad8-108">EXAMPLES</span></span>

### <span data-ttu-id="08ad8-109">Exempel 1: ta bort en databas från en Azure SQL-Server</span><span class="sxs-lookup"><span data-stu-id="08ad8-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="08ad8-110">Det här kommandot tar bort databasen som heter Database01 från Server Server01.</span><span class="sxs-lookup"><span data-stu-id="08ad8-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="08ad8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08ad8-111">PARAMETERS</span></span>

### <span data-ttu-id="08ad8-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08ad8-112">-DatabaseName</span></span>
<span data-ttu-id="08ad8-113">Anger namnet på den databas som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="08ad8-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ad8-114">-DefaultProfile</span></span>
<span data-ttu-id="08ad8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="08ad8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="08ad8-116">-Force</span></span>
<span data-ttu-id="08ad8-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="08ad8-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ad8-118">-ResourceGroupName</span></span>
<span data-ttu-id="08ad8-119">Anger namnet på den Azure Resource-grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="08ad8-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08ad8-120">-ServerName</span></span>
<span data-ttu-id="08ad8-121">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="08ad8-121">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08ad8-122">-Confirm</span></span>
<span data-ttu-id="08ad8-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08ad8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ad8-124">-WhatIf</span></span>
<span data-ttu-id="08ad8-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08ad8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ad8-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08ad8-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ad8-127">CommonParameters</span></span>
<span data-ttu-id="08ad8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ad8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ad8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ad8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08ad8-130">INPUTS</span></span>

### <span data-ttu-id="08ad8-131">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="08ad8-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="08ad8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08ad8-132">OUTPUTS</span></span>

### <span data-ttu-id="08ad8-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="08ad8-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="08ad8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08ad8-134">NOTES</span></span>

## <span data-ttu-id="08ad8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08ad8-135">RELATED LINKS</span></span>

[<span data-ttu-id="08ad8-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="08ad8-137">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="08ad8-138">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="08ad8-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="08ad8-140">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08ad8-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="08ad8-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="08ad8-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


