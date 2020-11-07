---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755907"
---
# <span data-ttu-id="55340-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="55340-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55340-102">SYNOPSIS</span></span>
<span data-ttu-id="55340-103">Anger egenskaper för en databas eller flyttar en befintlig databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="55340-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55340-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55340-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55340-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55340-105">DESCRIPTION</span></span>
<span data-ttu-id="55340-106">Cmdleten **set-AzureRmSqlDatabase** anger egenskaper för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="55340-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="55340-107">Dessutom kan du ange parametern *ElasticPoolName* om du vill flytta en databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="55340-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="55340-108">Om en databas redan finns i en elastisk pool kan du använda parametern *RequestedServiceObjectiveName* för att tilldela en prestanda nivå.</span><span class="sxs-lookup"><span data-stu-id="55340-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="55340-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55340-109">EXAMPLES</span></span>

### <span data-ttu-id="55340-110">Exempel 1: uppdatera en databas till en vanlig S2-databas</span><span class="sxs-lookup"><span data-stu-id="55340-110">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="55340-111">Det här kommandot uppdaterar en databas som heter Database01 till en vanlig S2-databas på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="55340-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="55340-112">Exempel 2: lägga till en databas i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="55340-112">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="55340-113">Det här kommandot lägger till en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 som finns på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="55340-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="55340-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55340-114">PARAMETERS</span></span>

### <span data-ttu-id="55340-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55340-115">-DatabaseName</span></span>
<span data-ttu-id="55340-116">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="55340-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55340-117">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="55340-117">-Edition</span></span>
<span data-ttu-id="55340-118">Anger versionen för databasen.</span><span class="sxs-lookup"><span data-stu-id="55340-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="55340-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="55340-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55340-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="55340-120">None</span></span>
- <span data-ttu-id="55340-121">Beta</span><span class="sxs-lookup"><span data-stu-id="55340-121">Premium</span></span>
- <span data-ttu-id="55340-122">Basisk</span><span class="sxs-lookup"><span data-stu-id="55340-122">Basic</span></span>
- <span data-ttu-id="55340-123">Standar</span><span class="sxs-lookup"><span data-stu-id="55340-123">Standard</span></span>
- <span data-ttu-id="55340-124">Warehouse</span><span class="sxs-lookup"><span data-stu-id="55340-124">DataWarehouse</span></span>
- <span data-ttu-id="55340-125">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="55340-125">Free</span></span>

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

### <span data-ttu-id="55340-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="55340-126">-ElasticPoolName</span></span>
<span data-ttu-id="55340-127">Anger namnet på den Elastic pool som databasen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="55340-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="55340-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="55340-128">-MaxSizeBytes</span></span>
<span data-ttu-id="55340-129">Anger den nya maximala storleken för databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="55340-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="55340-130">Du kan ange antingen den här parametern eller *MaxSizeGB*.</span><span class="sxs-lookup"><span data-stu-id="55340-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="55340-131">Se *MaxSizeGB* -parametern för acceptabla värden per utgåva.</span><span class="sxs-lookup"><span data-stu-id="55340-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="55340-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="55340-132">-ReadScale</span></span>
<span data-ttu-id="55340-133">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="55340-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="55340-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="55340-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="55340-135">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="55340-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="55340-136">Information om tjänst mål finns i [Azure SQL Database Service tieres and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="55340-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="55340-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55340-137">-ResourceGroupName</span></span>
<span data-ttu-id="55340-138">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="55340-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="55340-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55340-139">-ServerName</span></span>
<span data-ttu-id="55340-140">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="55340-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="55340-141">-Taggar</span><span class="sxs-lookup"><span data-stu-id="55340-141">-Tags</span></span>
<span data-ttu-id="55340-142">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="55340-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55340-143">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="55340-143">For example:</span></span>

<span data-ttu-id="55340-144">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="55340-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55340-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55340-145">-Confirm</span></span>
<span data-ttu-id="55340-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55340-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55340-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55340-147">-WhatIf</span></span>
<span data-ttu-id="55340-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55340-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55340-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55340-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55340-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55340-150">-DefaultProfile</span></span>
<span data-ttu-id="55340-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55340-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55340-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55340-152">CommonParameters</span></span>
<span data-ttu-id="55340-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55340-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55340-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55340-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55340-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55340-155">INPUTS</span></span>

## <span data-ttu-id="55340-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55340-156">OUTPUTS</span></span>

### <span data-ttu-id="55340-157">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="55340-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="55340-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55340-158">NOTES</span></span>

## <span data-ttu-id="55340-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55340-159">RELATED LINKS</span></span>

[<span data-ttu-id="55340-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="55340-161">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="55340-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="55340-163">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="55340-164">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55340-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="55340-165">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="55340-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
