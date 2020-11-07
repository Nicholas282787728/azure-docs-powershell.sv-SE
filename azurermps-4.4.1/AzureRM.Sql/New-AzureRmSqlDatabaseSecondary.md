---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755420"
---
# <span data-ttu-id="e4218-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e4218-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="e4218-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4218-102">SYNOPSIS</span></span>
<span data-ttu-id="e4218-103">Skapar en sekundär databas för en befintlig databas och startar datareplikering.</span><span class="sxs-lookup"><span data-stu-id="e4218-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4218-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4218-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4218-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4218-105">DESCRIPTION</span></span>
<span data-ttu-id="e4218-106">**New-AzureRMSqlDatabaseSecondary** cmdlet ersätter Start-AzureSqlDatabaseCopy cmdlet när den används för att konfigurera geo-replikering för en databas.</span><span class="sxs-lookup"><span data-stu-id="e4218-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="e4218-107">Det returnerar det geo-replikeringslänk som är länkat till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e4218-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="e4218-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4218-108">EXAMPLES</span></span>

### <span data-ttu-id="e4218-109">1: etablera Active Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="e4218-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="e4218-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4218-110">PARAMETERS</span></span>

### <span data-ttu-id="e4218-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="e4218-111">-AllowConnections</span></span>
<span data-ttu-id="e4218-112">Anger det alternativa Azure SQL-databasens Läs metod.</span><span class="sxs-lookup"><span data-stu-id="e4218-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="e4218-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e4218-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4218-114">Nej</span><span class="sxs-lookup"><span data-stu-id="e4218-114">No</span></span>
- <span data-ttu-id="e4218-115">Alla</span><span class="sxs-lookup"><span data-stu-id="e4218-115">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases: 
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4218-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4218-116">-DatabaseName</span></span>
<span data-ttu-id="e4218-117">Anger namnet på databasen som ska fungera som primärt.</span><span class="sxs-lookup"><span data-stu-id="e4218-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="e4218-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4218-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e4218-119">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e4218-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4218-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e4218-120">-PartnerServerName</span></span>
<span data-ttu-id="e4218-121">Anger namnet på den databas server för Azure SQL som ska fungera som sekundär.</span><span class="sxs-lookup"><span data-stu-id="e4218-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4218-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4218-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4218-123">Anger namnet på den Azure Resource-grupp som den här cmdleten tilldelar den primära databasen.</span><span class="sxs-lookup"><span data-stu-id="e4218-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="e4218-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e4218-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="e4218-125">Anger namnet på den elastiska pool som den sekundära databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="e4218-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="e4218-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e4218-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="e4218-127">Anger namnet på det tjänst mål som ska kopplas till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="e4218-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="e4218-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4218-128">-ServerName</span></span>
<span data-ttu-id="e4218-129">Anger namnet på SQL-servern för den primära SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e4218-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="e4218-130">-Taggar</span><span class="sxs-lookup"><span data-stu-id="e4218-130">-Tags</span></span>
<span data-ttu-id="e4218-131">Anger de viktigaste par i formen av en hash-tabell som ska kopplas till länken för SQL-databasfilen.</span><span class="sxs-lookup"><span data-stu-id="e4218-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="e4218-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e4218-132">For example:</span></span>

<span data-ttu-id="e4218-133">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e4218-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4218-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4218-134">-Confirm</span></span>
<span data-ttu-id="e4218-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4218-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4218-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4218-136">-WhatIf</span></span>
<span data-ttu-id="e4218-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4218-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4218-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4218-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4218-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4218-139">-DefaultProfile</span></span>
<span data-ttu-id="e4218-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4218-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4218-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4218-141">CommonParameters</span></span>
<span data-ttu-id="e4218-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4218-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4218-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4218-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4218-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4218-144">INPUTS</span></span>

## <span data-ttu-id="e4218-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4218-145">OUTPUTS</span></span>

### <span data-ttu-id="e4218-146">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e4218-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="e4218-147">Denna cmdlet returnerar **ReplicationLink** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e4218-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="e4218-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4218-148">NOTES</span></span>

## <span data-ttu-id="e4218-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4218-149">RELATED LINKS</span></span>

[<span data-ttu-id="e4218-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e4218-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="e4218-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e4218-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="e4218-152">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e4218-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
