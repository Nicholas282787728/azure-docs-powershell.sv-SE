---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413259"
---
# <span data-ttu-id="ce547-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="ce547-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="ce547-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce547-102">SYNOPSIS</span></span>
<span data-ttu-id="ce547-103">Returnerar loggarna för en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="ce547-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ce547-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce547-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce547-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce547-105">DESCRIPTION</span></span>
<span data-ttu-id="ce547-106">Cmdleten **Get-AzSqlSyncGroupLog** returnerar loggarna för en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="ce547-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ce547-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce547-107">EXAMPLES</span></span>

### <span data-ttu-id="ce547-108">Exempel 1: Hämta loggarna för en Azure SQL Sync-grupp</span><span class="sxs-lookup"><span data-stu-id="ce547-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="ce547-109">Det här kommandot hämtar loggarna för en Azure SQL Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="ce547-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="ce547-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce547-110">PARAMETERS</span></span>

### <span data-ttu-id="ce547-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce547-111">-DatabaseName</span></span>
<span data-ttu-id="ce547-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ce547-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ce547-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce547-113">-DefaultProfile</span></span>
<span data-ttu-id="ce547-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ce547-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce547-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="ce547-115">-EndTime</span></span>
<span data-ttu-id="ce547-116">Slut tiden för loggarna.</span><span class="sxs-lookup"><span data-stu-id="ce547-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="ce547-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="ce547-117">-LogLevel</span></span>
<span data-ttu-id="ce547-118">Typen för de loggar som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="ce547-118">The type of the logs to query.</span></span>
<span data-ttu-id="ce547-119">Giltiga värden är: "fel", "varning", "lyckades" och "alla".</span><span class="sxs-lookup"><span data-stu-id="ce547-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="ce547-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce547-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce547-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ce547-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce547-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce547-122">-ServerName</span></span>
<span data-ttu-id="ce547-123">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce547-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ce547-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce547-124">-StartTime</span></span>
<span data-ttu-id="ce547-125">Start tiden för loggarna.</span><span class="sxs-lookup"><span data-stu-id="ce547-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="ce547-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ce547-126">-SyncGroupName</span></span>
<span data-ttu-id="ce547-127">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="ce547-127">The sync group name.</span></span>

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

### <span data-ttu-id="ce547-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce547-128">CommonParameters</span></span>
<span data-ttu-id="ce547-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce547-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce547-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce547-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce547-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce547-131">INPUTS</span></span>

### <span data-ttu-id="ce547-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ce547-132">System.String</span></span>

## <span data-ttu-id="ce547-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce547-133">OUTPUTS</span></span>

### <span data-ttu-id="ce547-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="ce547-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="ce547-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce547-135">NOTES</span></span>

## <span data-ttu-id="ce547-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce547-136">RELATED LINKS</span></span>
