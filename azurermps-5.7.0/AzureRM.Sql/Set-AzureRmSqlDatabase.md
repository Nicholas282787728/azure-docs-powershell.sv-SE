---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575451"
---
# <span data-ttu-id="308eb-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="308eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="308eb-102">SYNOPSIS</span></span>
<span data-ttu-id="308eb-103">Anger egenskaper för en databas eller flyttar en befintlig databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="308eb-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="308eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="308eb-104">SYNTAX</span></span>

### <span data-ttu-id="308eb-105">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="308eb-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308eb-106">Byta namn på</span><span class="sxs-lookup"><span data-stu-id="308eb-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="308eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="308eb-107">DESCRIPTION</span></span>
<span data-ttu-id="308eb-108">Cmdleten **set-AzureRmSqlDatabase** anger egenskaper för en databas i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="308eb-109">Denna cmdlet kan ändra tjänst nivån ( *utgåvan* ), Performance Level ( *RequestedServiceObjectiveName* ) och *MaxSizeBytes* (Storage maximum size) för databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="308eb-110">Dessutom kan du ange parametern *ElasticPoolName* om du vill flytta en databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="308eb-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="308eb-111">Om en databas redan finns i en elastisk pool kan du använda parametern *RequestedServiceObjectiveName* för att flytta databasen från en elastisk pool och till en prestanda nivå för enskilda databaser.</span><span class="sxs-lookup"><span data-stu-id="308eb-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="308eb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="308eb-112">EXAMPLES</span></span>

### <span data-ttu-id="308eb-113">Exempel 1: uppdatera en databas till en vanlig S2-databas</span><span class="sxs-lookup"><span data-stu-id="308eb-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="308eb-114">Det här kommandot uppdaterar en databas som heter Database01 till en vanlig S2-databas på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="308eb-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="308eb-115">Exempel 2: lägga till en databas i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="308eb-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="308eb-116">Det här kommandot lägger till en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 som finns på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="308eb-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="308eb-117">Exempel 3: ändra Max storleken på en databas</span><span class="sxs-lookup"><span data-stu-id="308eb-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="308eb-118">Det här kommandot uppdaterar en databas med namnet Database01 för att ange max storleken till 1 TB.</span><span class="sxs-lookup"><span data-stu-id="308eb-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="308eb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="308eb-119">PARAMETERS</span></span>

### <span data-ttu-id="308eb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308eb-120">-AsJob</span></span>
<span data-ttu-id="308eb-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="308eb-121">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="308eb-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="308eb-122">-DatabaseName</span></span>
<span data-ttu-id="308eb-123">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="308eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308eb-124">-DefaultProfile</span></span>
<span data-ttu-id="308eb-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="308eb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="308eb-126">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="308eb-126">-Edition</span></span>
<span data-ttu-id="308eb-127">Anger versionen för databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="308eb-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="308eb-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="308eb-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="308eb-129">None</span></span>
- <span data-ttu-id="308eb-130">Beta</span><span class="sxs-lookup"><span data-stu-id="308eb-130">Premium</span></span>
- <span data-ttu-id="308eb-131">Basisk</span><span class="sxs-lookup"><span data-stu-id="308eb-131">Basic</span></span>
- <span data-ttu-id="308eb-132">Standar</span><span class="sxs-lookup"><span data-stu-id="308eb-132">Standard</span></span>
- <span data-ttu-id="308eb-133">Warehouse</span><span class="sxs-lookup"><span data-stu-id="308eb-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="308eb-134">-ElasticPoolName</span></span>
<span data-ttu-id="308eb-135">Anger namnet på den Elastic pool som databasen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="308eb-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="308eb-136">-MaxSizeBytes</span></span>
<span data-ttu-id="308eb-137">Maximal storlek för Azure SQL-databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="308eb-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="308eb-138">-NewName</span></span>
<span data-ttu-id="308eb-139">Det nya namnet för att byta namn på databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="308eb-140">-ReadScale</span></span>
<span data-ttu-id="308eb-141">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="308eb-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="308eb-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="308eb-143">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="308eb-144">Information om tjänst mål finns i [Azure SQL Database Service tieres and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="308eb-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308eb-145">-ResourceGroupName</span></span>
<span data-ttu-id="308eb-146">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="308eb-146">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="308eb-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="308eb-147">-ServerName</span></span>
<span data-ttu-id="308eb-148">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="308eb-148">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="308eb-149">-Taggar</span><span class="sxs-lookup"><span data-stu-id="308eb-149">-Tags</span></span>
<span data-ttu-id="308eb-150">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="308eb-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="308eb-151">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="308eb-151">For example:</span></span>

<span data-ttu-id="308eb-152">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="308eb-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="308eb-153">-ZoneRedundant</span></span>
<span data-ttu-id="308eb-154">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="308eb-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308eb-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="308eb-155">-Confirm</span></span>
<span data-ttu-id="308eb-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="308eb-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308eb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308eb-157">-WhatIf</span></span>
<span data-ttu-id="308eb-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="308eb-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308eb-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="308eb-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308eb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308eb-160">CommonParameters</span></span>
<span data-ttu-id="308eb-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308eb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308eb-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308eb-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308eb-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="308eb-163">INPUTS</span></span>

### <span data-ttu-id="308eb-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="308eb-164">None</span></span>
<span data-ttu-id="308eb-165">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="308eb-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="308eb-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="308eb-166">OUTPUTS</span></span>

### <span data-ttu-id="308eb-167">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="308eb-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="308eb-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="308eb-168">NOTES</span></span>

## <span data-ttu-id="308eb-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="308eb-169">RELATED LINKS</span></span>

[<span data-ttu-id="308eb-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="308eb-171">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="308eb-172">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="308eb-173">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="308eb-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="308eb-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="308eb-175">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="308eb-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
