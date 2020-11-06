---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 05b090de647f1c6e6abfb7f2c83e5bd0a4cf616b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582179"
---
# <span data-ttu-id="663e3-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="663e3-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="663e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="663e3-102">SYNOPSIS</span></span>
<span data-ttu-id="663e3-103">Hämtar Länkar för geo-replikering mellan en Azure SQL-databas och en resurs grupp eller SQL Server.</span><span class="sxs-lookup"><span data-stu-id="663e3-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="663e3-104">SYNTAX</span></span>

### <span data-ttu-id="663e3-105">ByDatabaseName (standard)</span><span class="sxs-lookup"><span data-stu-id="663e3-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="663e3-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="663e3-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="663e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="663e3-107">DESCRIPTION</span></span>
<span data-ttu-id="663e3-108">Cmdleten **Get-AzureRMSqlDatabaseReplicationLink** ersätter cmdleten **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="663e3-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="663e3-109">Den får alla geo-replikeringslänken-länkar mellan den angivna Azure SQL-databasen och en resurs grupp eller en AzureSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="663e3-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="663e3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="663e3-110">EXAMPLES</span></span>

## <span data-ttu-id="663e3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="663e3-111">PARAMETERS</span></span>

### <span data-ttu-id="663e3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="663e3-112">-DatabaseName</span></span>
<span data-ttu-id="663e3-113">Anger namnet på den SQL-databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="663e3-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="663e3-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663e3-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="663e3-115">Anger namnet på den resurs grupp som partnern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="663e3-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="663e3-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="663e3-116">-PartnerServerName</span></span>
<span data-ttu-id="663e3-117">Anger namnet på partnerns Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="663e3-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="663e3-119">Anger namnet på den databas som du vill hämta länkar för.</span><span class="sxs-lookup"><span data-stu-id="663e3-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="663e3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="663e3-120">-ServerName</span></span>
<span data-ttu-id="663e3-121">Anger namnet på SQL Server för databasen där länkar ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="663e3-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="663e3-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="663e3-122">-Confirm</span></span>
<span data-ttu-id="663e3-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="663e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663e3-124">-WhatIf</span></span>
<span data-ttu-id="663e3-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="663e3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="663e3-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="663e3-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663e3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663e3-127">-DefaultProfile</span></span>
<span data-ttu-id="663e3-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="663e3-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="663e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663e3-129">CommonParameters</span></span>
<span data-ttu-id="663e3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663e3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663e3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="663e3-132">INPUTS</span></span>

###  
<span data-ttu-id="663e3-133">Denna cmdlet accepterar instanser av **ReplicationLink** eller **databasobjektet** för den primära eller sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="663e3-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="663e3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="663e3-134">OUTPUTS</span></span>

###  
<span data-ttu-id="663e3-135">Denna cmdlet returnerar ett **ReplicationLink** -objekt.</span><span class="sxs-lookup"><span data-stu-id="663e3-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="663e3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="663e3-136">NOTES</span></span>

## <span data-ttu-id="663e3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="663e3-137">RELATED LINKS</span></span>

[<span data-ttu-id="663e3-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="663e3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
