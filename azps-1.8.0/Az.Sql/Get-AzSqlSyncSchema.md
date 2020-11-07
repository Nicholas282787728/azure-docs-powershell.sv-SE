---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7e6e060b2ad9e05a0a2789202e74f093f0366749
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746638"
---
# <span data-ttu-id="7a247-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="7a247-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="7a247-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a247-102">SYNOPSIS</span></span>
<span data-ttu-id="7a247-103">Returnerar information om synkroniseringsschemat för en medlems databas eller en nav-databas.</span><span class="sxs-lookup"><span data-stu-id="7a247-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="7a247-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a247-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a247-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a247-105">DESCRIPTION</span></span>
<span data-ttu-id="7a247-106">Cmdleten **Get-AzSqlSyncSchema** returnerar information om synkroniseringsschemat för en medlems databas eller en nav-databas.</span><span class="sxs-lookup"><span data-stu-id="7a247-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="7a247-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a247-107">EXAMPLES</span></span>

### <span data-ttu-id="7a247-108">Exempel 1,1: Hämta synkroniseringsschemat för en nav-databas</span><span class="sxs-lookup"><span data-stu-id="7a247-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="7a247-109">Det här kommandot hämtar synkroniseringsschemat för NAV databasen i Sync-gruppsyncGroup01et.</span><span class="sxs-lookup"><span data-stu-id="7a247-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="7a247-110">Exempel 1,2: Hämta synkroniseringsschemat för en nav-databas och expandera tabeller</span><span class="sxs-lookup"><span data-stu-id="7a247-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="7a247-111">Det här kommandot får synkroniseringsschemat för NAV databasen i metabasegenskapen Sync Group syncGroup01 och Expanding Table.</span><span class="sxs-lookup"><span data-stu-id="7a247-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="7a247-112">Exempel 2: Hämta synkroniseringsschemat för en medlems databas</span><span class="sxs-lookup"><span data-stu-id="7a247-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="7a247-113">Det här kommandot hämtar synkroniseringsschemat för medlems databasen i syncMember01.</span><span class="sxs-lookup"><span data-stu-id="7a247-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="7a247-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a247-114">PARAMETERS</span></span>

### <span data-ttu-id="7a247-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a247-115">-DatabaseName</span></span>
<span data-ttu-id="7a247-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="7a247-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7a247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a247-117">-DefaultProfile</span></span>
<span data-ttu-id="7a247-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a247-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a247-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a247-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a247-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7a247-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a247-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a247-121">-ServerName</span></span>
<span data-ttu-id="7a247-122">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7a247-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7a247-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7a247-123">-SyncGroupName</span></span>
<span data-ttu-id="7a247-124">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="7a247-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a247-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="7a247-125">-SyncMemberName</span></span>
<span data-ttu-id="7a247-126">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="7a247-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a247-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a247-127">CommonParameters</span></span>
<span data-ttu-id="7a247-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a247-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a247-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a247-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a247-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a247-130">INPUTS</span></span>

### <span data-ttu-id="7a247-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7a247-131">System.String</span></span>

## <span data-ttu-id="7a247-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a247-132">OUTPUTS</span></span>

### <span data-ttu-id="7a247-133">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="7a247-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="7a247-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a247-134">NOTES</span></span>

## <span data-ttu-id="7a247-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a247-135">RELATED LINKS</span></span>
