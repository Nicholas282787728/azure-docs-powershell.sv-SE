---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757176"
---
# <span data-ttu-id="fb144-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="fb144-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="fb144-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb144-102">SYNOPSIS</span></span>
<span data-ttu-id="fb144-103">Returnerar information om SQL Server-databaser som är länkade av en synkroniseringsklient.</span><span class="sxs-lookup"><span data-stu-id="fb144-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb144-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb144-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb144-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb144-105">DESCRIPTION</span></span>
<span data-ttu-id="fb144-106">Cmdleten **Get-AzureRmSqlSyncAgentLinkedDatabases** returnerar information om SQL Server-databaser som är länkade av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="fb144-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="fb144-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb144-107">EXAMPLES</span></span>

### <span data-ttu-id="fb144-108">Exempel 1: Hämta de länkade SQL Server-databaserna för en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="fb144-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="fb144-109">Det här kommandot returnerar de länkade SQL Server-databaserna som är länkade av en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="fb144-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="fb144-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb144-110">PARAMETERS</span></span>

### <span data-ttu-id="fb144-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb144-111">-DefaultProfile</span></span>
<span data-ttu-id="fb144-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb144-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb144-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb144-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb144-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fb144-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb144-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb144-115">-ServerName</span></span>
<span data-ttu-id="fb144-116">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="fb144-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="fb144-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="fb144-117">-SyncAgentName</span></span>
<span data-ttu-id="fb144-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="fb144-118">The sync agent name.</span></span>

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

### <span data-ttu-id="fb144-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb144-119">CommonParameters</span></span>
<span data-ttu-id="fb144-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb144-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb144-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb144-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb144-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb144-122">INPUTS</span></span>

### <span data-ttu-id="fb144-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="fb144-123">None</span></span>
<span data-ttu-id="fb144-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fb144-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb144-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb144-125">OUTPUTS</span></span>

### <span data-ttu-id="fb144-126">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fb144-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="fb144-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb144-127">NOTES</span></span>

## <span data-ttu-id="fb144-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb144-128">RELATED LINKS</span></span>