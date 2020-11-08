---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b893805fbf4ae9bc7ff77a3a63a97154e879a01e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088493"
---
# <span data-ttu-id="3df7c-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="3df7c-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="3df7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3df7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3df7c-103">Returnerar information om SQL Server-databaser som är länkade av en synkroniseringsklient.</span><span class="sxs-lookup"><span data-stu-id="3df7c-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="3df7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3df7c-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3df7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3df7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3df7c-106">Cmdleten **Get-AzSqlSyncAgentLinkedDatabases** returnerar information om SQL Server-databaser som är länkade av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="3df7c-106">The **Get-AzSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="3df7c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3df7c-107">EXAMPLES</span></span>

### <span data-ttu-id="3df7c-108">Exempel 1: Hämta de länkade SQL Server-databaserna för en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="3df7c-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="3df7c-109">Det här kommandot returnerar de länkade SQL Server-databaserna som är länkade av en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="3df7c-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="3df7c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3df7c-110">PARAMETERS</span></span>

### <span data-ttu-id="3df7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df7c-111">-DefaultProfile</span></span>
<span data-ttu-id="3df7c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3df7c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3df7c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df7c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3df7c-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3df7c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="3df7c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3df7c-115">-ServerName</span></span>
<span data-ttu-id="3df7c-116">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="3df7c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="3df7c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3df7c-117">-SyncAgentName</span></span>
<span data-ttu-id="3df7c-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="3df7c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="3df7c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df7c-119">CommonParameters</span></span>
<span data-ttu-id="3df7c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df7c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df7c-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df7c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df7c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3df7c-122">INPUTS</span></span>

### <span data-ttu-id="3df7c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3df7c-123">System.String</span></span>

## <span data-ttu-id="3df7c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3df7c-124">OUTPUTS</span></span>

### <span data-ttu-id="3df7c-125">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3df7c-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="3df7c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3df7c-126">NOTES</span></span>

## <span data-ttu-id="3df7c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3df7c-127">RELATED LINKS</span></span>
