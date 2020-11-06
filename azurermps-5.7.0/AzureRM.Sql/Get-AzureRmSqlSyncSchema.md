---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 7947b7639678487777c534820656dc0cb3137295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580955"
---
# <span data-ttu-id="2453c-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="2453c-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="2453c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2453c-102">SYNOPSIS</span></span>
<span data-ttu-id="2453c-103">Returnerar information om synkroniseringsschemat för en medlems databas eller en nav-databas.</span><span class="sxs-lookup"><span data-stu-id="2453c-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2453c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2453c-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2453c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2453c-105">DESCRIPTION</span></span>
<span data-ttu-id="2453c-106">Cmdleten **Get-AzureRmSqlSyncSchema** returnerar information om synkroniseringsschemat för en medlems databas eller en nav-databas.</span><span class="sxs-lookup"><span data-stu-id="2453c-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="2453c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2453c-107">EXAMPLES</span></span>

### <span data-ttu-id="2453c-108">Exempel 1,1: Hämta synkroniseringsschemat för en nav-databas</span><span class="sxs-lookup"><span data-stu-id="2453c-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="2453c-109">Det här kommandot hämtar synkroniseringsschemat för NAV databasen i Sync-gruppsyncGroup01et.</span><span class="sxs-lookup"><span data-stu-id="2453c-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="2453c-110">Exempel 1,2: Hämta synkroniseringsschemat för en nav-databas och expandera tabeller</span><span class="sxs-lookup"><span data-stu-id="2453c-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="2453c-111">Det här kommandot får synkroniseringsschemat för NAV databasen i metabasegenskapen Sync Group syncGroup01 och Expanding Table.</span><span class="sxs-lookup"><span data-stu-id="2453c-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="2453c-112">Exempel 2: Hämta synkroniseringsschemat för en medlems databas</span><span class="sxs-lookup"><span data-stu-id="2453c-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="2453c-113">Det här kommandot hämtar synkroniseringsschemat för medlems databasen i syncMember01.</span><span class="sxs-lookup"><span data-stu-id="2453c-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="2453c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2453c-114">PARAMETERS</span></span>

### <span data-ttu-id="2453c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2453c-115">-DatabaseName</span></span>
<span data-ttu-id="2453c-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="2453c-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2453c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2453c-117">-DefaultProfile</span></span>
<span data-ttu-id="2453c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2453c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2453c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2453c-119">-ResourceGroupName</span></span>
<span data-ttu-id="2453c-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2453c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2453c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2453c-121">-ServerName</span></span>
<span data-ttu-id="2453c-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2453c-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2453c-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2453c-123">-SyncGroupName</span></span>
<span data-ttu-id="2453c-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="2453c-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2453c-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="2453c-125">-SyncMemberName</span></span>
<span data-ttu-id="2453c-126">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="2453c-126">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2453c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2453c-127">CommonParameters</span></span>
<span data-ttu-id="2453c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2453c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2453c-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2453c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2453c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2453c-130">INPUTS</span></span>

### <span data-ttu-id="2453c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="2453c-131">None</span></span>
<span data-ttu-id="2453c-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2453c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2453c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2453c-133">OUTPUTS</span></span>

### <span data-ttu-id="2453c-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="2453c-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="2453c-135">Tabeller: Microsoft. Azure. kommandon. SQL. DataSync. Model. AzureSqlSyncFullSchemaTableModel</span><span class="sxs-lookup"><span data-stu-id="2453c-135">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="2453c-136">Kolumner: Microsoft. Azure. kommandon. SQL. DataSync. Model. AzureSqlSyncFullSchemaColumnModel</span><span class="sxs-lookup"><span data-stu-id="2453c-136">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="2453c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2453c-137">NOTES</span></span>

## <span data-ttu-id="2453c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2453c-138">RELATED LINKS</span></span>
