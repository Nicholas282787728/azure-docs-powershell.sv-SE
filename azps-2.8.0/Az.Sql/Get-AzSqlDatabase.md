---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: bcaa1c5d57fea979e227fa8890cac6ac0b3f8a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920241"
---
# <span data-ttu-id="7963e-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="7963e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7963e-102">SYNOPSIS</span></span>
<span data-ttu-id="7963e-103">Hämtar en eller flera databaser.</span><span class="sxs-lookup"><span data-stu-id="7963e-103">Gets one or more databases.</span></span>

## <span data-ttu-id="7963e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7963e-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7963e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7963e-105">DESCRIPTION</span></span>
<span data-ttu-id="7963e-106">Cmdleten **Get-AzSqlDatabase** hämtar en eller flera Azure SQL-databaser från en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="7963e-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="7963e-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="7963e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7963e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7963e-108">EXAMPLES</span></span>

### <span data-ttu-id="7963e-109">Exempel 1: Hämta alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="7963e-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="7963e-110">Det här kommandot får alla databaser på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="7963e-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="7963e-111">Exempel 2: Hämta en databas med namn på en server</span><span class="sxs-lookup"><span data-stu-id="7963e-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="7963e-112">Det här kommandot får en databas som heter Database02 från en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="7963e-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="7963e-113">Exempel 3: Hämta alla databaser på en server med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="7963e-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="7963e-114">Det här kommandot får alla databaser på servern med namnet Server01 som börjar med "databas".</span><span class="sxs-lookup"><span data-stu-id="7963e-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="7963e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7963e-115">PARAMETERS</span></span>

### <span data-ttu-id="7963e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7963e-116">-DatabaseName</span></span>
<span data-ttu-id="7963e-117">Anger namnet på den databas som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7963e-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7963e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7963e-118">-DefaultProfile</span></span>
<span data-ttu-id="7963e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7963e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7963e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7963e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7963e-121">Anger namnet på den resurs grupp som databas servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7963e-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="7963e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7963e-122">-ServerName</span></span>
<span data-ttu-id="7963e-123">Anger namnet på den server som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="7963e-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="7963e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7963e-124">-Confirm</span></span>
<span data-ttu-id="7963e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7963e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7963e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7963e-126">-WhatIf</span></span>
<span data-ttu-id="7963e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7963e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7963e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7963e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7963e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7963e-129">CommonParameters</span></span>
<span data-ttu-id="7963e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7963e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7963e-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7963e-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7963e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7963e-132">INPUTS</span></span>

### <span data-ttu-id="7963e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7963e-133">System.String</span></span>

## <span data-ttu-id="7963e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7963e-134">OUTPUTS</span></span>

### <span data-ttu-id="7963e-135">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7963e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7963e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7963e-136">NOTES</span></span>

## <span data-ttu-id="7963e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7963e-137">RELATED LINKS</span></span>

[<span data-ttu-id="7963e-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="7963e-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="7963e-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="7963e-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="7963e-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7963e-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

