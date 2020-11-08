---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088490"
---
# <span data-ttu-id="1a166-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="1a166-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="1a166-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a166-102">SYNOPSIS</span></span>
<span data-ttu-id="1a166-103">Returnerar loggarna för en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="1a166-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1a166-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a166-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a166-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a166-105">DESCRIPTION</span></span>
<span data-ttu-id="1a166-106">Cmdleten **Get-AzSqlSyncGroupLog** returnerar loggarna för en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="1a166-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1a166-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a166-107">EXAMPLES</span></span>

### <span data-ttu-id="1a166-108">Exempel 1: Hämta loggarna för en Azure SQL Sync-grupp</span><span class="sxs-lookup"><span data-stu-id="1a166-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="1a166-109">Det här kommandot hämtar loggarna för en Azure SQL Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="1a166-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="1a166-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a166-110">PARAMETERS</span></span>

### <span data-ttu-id="1a166-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a166-111">-DatabaseName</span></span>
<span data-ttu-id="1a166-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="1a166-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1a166-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a166-113">-DefaultProfile</span></span>
<span data-ttu-id="1a166-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1a166-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a166-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="1a166-115">-EndTime</span></span>
<span data-ttu-id="1a166-116">Slut tiden för loggarna.</span><span class="sxs-lookup"><span data-stu-id="1a166-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a166-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="1a166-117">-LogLevel</span></span>
<span data-ttu-id="1a166-118">Typen för de loggar som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="1a166-118">The type of the logs to query.</span></span>
<span data-ttu-id="1a166-119">Giltiga värden är: "fel", "varning", "lyckades" och "alla".</span><span class="sxs-lookup"><span data-stu-id="1a166-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a166-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a166-120">-ResourceGroupName</span></span>
<span data-ttu-id="1a166-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a166-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a166-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a166-122">-ServerName</span></span>
<span data-ttu-id="1a166-123">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1a166-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1a166-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1a166-124">-StartTime</span></span>
<span data-ttu-id="1a166-125">Start tiden för loggarna.</span><span class="sxs-lookup"><span data-stu-id="1a166-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a166-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1a166-126">-SyncGroupName</span></span>
<span data-ttu-id="1a166-127">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="1a166-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a166-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a166-128">CommonParameters</span></span>
<span data-ttu-id="1a166-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a166-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a166-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a166-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a166-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a166-131">INPUTS</span></span>

### <span data-ttu-id="1a166-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a166-132">System.String</span></span>

## <span data-ttu-id="1a166-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a166-133">OUTPUTS</span></span>

### <span data-ttu-id="1a166-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="1a166-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="1a166-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a166-135">NOTES</span></span>

## <span data-ttu-id="1a166-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a166-136">RELATED LINKS</span></span>
