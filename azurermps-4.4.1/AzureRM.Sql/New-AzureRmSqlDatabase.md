---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574488"
---
# <span data-ttu-id="0611e-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="0611e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0611e-102">SYNOPSIS</span></span>
<span data-ttu-id="0611e-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="0611e-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0611e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0611e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0611e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0611e-105">DESCRIPTION</span></span>
<span data-ttu-id="0611e-106">Cmdleten **New-AzureRmSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0611e-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="0611e-107">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="0611e-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0611e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0611e-108">EXAMPLES</span></span>

### <span data-ttu-id="0611e-109">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="0611e-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
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

<span data-ttu-id="0611e-110">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="0611e-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="0611e-111">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="0611e-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="0611e-112">Det här kommandot skapar en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="0611e-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="0611e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0611e-113">PARAMETERS</span></span>

### <span data-ttu-id="0611e-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="0611e-114">-CatalogCollation</span></span>
<span data-ttu-id="0611e-115">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="0611e-115">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="0611e-116">-CollationName</span></span>
<span data-ttu-id="0611e-117">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-117">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0611e-118">-DatabaseName</span></span>
<span data-ttu-id="0611e-119">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-119">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-120">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="0611e-120">-Edition</span></span>
<span data-ttu-id="0611e-121">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="0611e-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0611e-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0611e-123">Vis</span><span class="sxs-lookup"><span data-stu-id="0611e-123">Default</span></span>
- <span data-ttu-id="0611e-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="0611e-124">None</span></span>
- <span data-ttu-id="0611e-125">Beta</span><span class="sxs-lookup"><span data-stu-id="0611e-125">Premium</span></span>
- <span data-ttu-id="0611e-126">Basisk</span><span class="sxs-lookup"><span data-stu-id="0611e-126">Basic</span></span>
- <span data-ttu-id="0611e-127">Standar</span><span class="sxs-lookup"><span data-stu-id="0611e-127">Standard</span></span>
- <span data-ttu-id="0611e-128">Warehouse</span><span class="sxs-lookup"><span data-stu-id="0611e-128">DataWarehouse</span></span>
- <span data-ttu-id="0611e-129">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="0611e-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0611e-130">-ElasticPoolName</span></span>
<span data-ttu-id="0611e-131">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="0611e-131">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0611e-132">-MaxSizeBytes</span></span>
<span data-ttu-id="0611e-133">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="0611e-133">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="0611e-134">-ReadScale</span></span>
<span data-ttu-id="0611e-135">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="0611e-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0611e-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="0611e-137">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-137">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0611e-138">-ResourceGroupName</span></span>
<span data-ttu-id="0611e-139">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="0611e-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0611e-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="0611e-140">-SampleName</span></span>
<span data-ttu-id="0611e-141">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="0611e-141">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0611e-142">-ServerName</span></span>
<span data-ttu-id="0611e-143">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0611e-144">-Taggar</span><span class="sxs-lookup"><span data-stu-id="0611e-144">-Tags</span></span>
<span data-ttu-id="0611e-145">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="0611e-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="0611e-146">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="0611e-146">For example:</span></span>

<span data-ttu-id="0611e-147">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="0611e-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0611e-148">-Confirm</span></span>
<span data-ttu-id="0611e-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0611e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0611e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0611e-150">-WhatIf</span></span>
<span data-ttu-id="0611e-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0611e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0611e-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0611e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0611e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0611e-153">-DefaultProfile</span></span>
<span data-ttu-id="0611e-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0611e-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0611e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0611e-155">CommonParameters</span></span>
<span data-ttu-id="0611e-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0611e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0611e-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0611e-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0611e-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0611e-158">INPUTS</span></span>

## <span data-ttu-id="0611e-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0611e-159">OUTPUTS</span></span>

### <span data-ttu-id="0611e-160">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0611e-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0611e-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0611e-161">NOTES</span></span>

## <span data-ttu-id="0611e-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0611e-162">RELATED LINKS</span></span>

[<span data-ttu-id="0611e-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="0611e-164">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0611e-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="0611e-165">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0611e-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="0611e-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="0611e-167">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="0611e-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="0611e-169">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0611e-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="0611e-170">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0611e-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
