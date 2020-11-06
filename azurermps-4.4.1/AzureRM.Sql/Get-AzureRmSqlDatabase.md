---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 9ae96035a4257826ac92dc6dbae75282debf08a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585291"
---
# <span data-ttu-id="d3347-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="d3347-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3347-102">SYNOPSIS</span></span>
<span data-ttu-id="d3347-103">Hämtar en eller flera databaser.</span><span class="sxs-lookup"><span data-stu-id="d3347-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3347-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3347-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3347-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3347-105">DESCRIPTION</span></span>
<span data-ttu-id="d3347-106">Cmdleten **Get-AzureRmSqlDatabase** hämtar en eller flera Azure SQL-databaser från en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="d3347-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="d3347-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="d3347-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d3347-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3347-108">EXAMPLES</span></span>

### <span data-ttu-id="d3347-109">Exempel 1: Hämta alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="d3347-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="d3347-110">Det här kommandot får alla databaser på servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="d3347-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="d3347-111">Exempel 2: Hämta en databas med namn på en server</span><span class="sxs-lookup"><span data-stu-id="d3347-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="d3347-112">Det här kommandot får en databas som heter Database02 från en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="d3347-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="d3347-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3347-113">PARAMETERS</span></span>

### <span data-ttu-id="d3347-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3347-114">-DatabaseName</span></span>
<span data-ttu-id="d3347-115">Anger namnet på den databas som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="d3347-115">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3347-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3347-116">-ResourceGroupName</span></span>
<span data-ttu-id="d3347-117">Anger namnet på den resurs grupp som databas servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="d3347-117">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="d3347-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3347-118">-ServerName</span></span>
<span data-ttu-id="d3347-119">Anger namnet på den server som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d3347-119">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="d3347-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3347-120">-Confirm</span></span>
<span data-ttu-id="d3347-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3347-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3347-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3347-122">-WhatIf</span></span>
<span data-ttu-id="d3347-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3347-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3347-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3347-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3347-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3347-125">-DefaultProfile</span></span>
<span data-ttu-id="d3347-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3347-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3347-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3347-127">CommonParameters</span></span>
<span data-ttu-id="d3347-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3347-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3347-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3347-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3347-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3347-130">INPUTS</span></span>

## <span data-ttu-id="d3347-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3347-131">OUTPUTS</span></span>

### <span data-ttu-id="d3347-132">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d3347-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d3347-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3347-133">NOTES</span></span>

## <span data-ttu-id="d3347-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3347-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3347-135">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-135">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="d3347-136">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-136">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="d3347-137">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-137">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="d3347-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="d3347-139">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d3347-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


