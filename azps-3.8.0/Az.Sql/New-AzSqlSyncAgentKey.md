---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927954"
---
# <span data-ttu-id="6192b-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="6192b-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="6192b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6192b-102">SYNOPSIS</span></span>
<span data-ttu-id="6192b-103">Skapar en Azure SQL Sync-agenttjänsten.</span><span class="sxs-lookup"><span data-stu-id="6192b-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="6192b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6192b-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6192b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6192b-105">DESCRIPTION</span></span>
<span data-ttu-id="6192b-106">Cmdleten **New-AzSqlSyncAgentKey** skapar en Azure SQL Sync-agenttjänsten.</span><span class="sxs-lookup"><span data-stu-id="6192b-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="6192b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6192b-107">EXAMPLES</span></span>

### <span data-ttu-id="6192b-108">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-synkroniseringsklient.</span><span class="sxs-lookup"><span data-stu-id="6192b-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="6192b-109">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="6192b-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="6192b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6192b-110">PARAMETERS</span></span>

### <span data-ttu-id="6192b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6192b-111">-DefaultProfile</span></span>
<span data-ttu-id="6192b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6192b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6192b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6192b-113">-ResourceGroupName</span></span>
<span data-ttu-id="6192b-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6192b-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="6192b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6192b-115">-ServerName</span></span>
<span data-ttu-id="6192b-116">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="6192b-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="6192b-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="6192b-117">-SyncAgentName</span></span>
<span data-ttu-id="6192b-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="6192b-118">The sync agent name.</span></span>

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

### <span data-ttu-id="6192b-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6192b-119">-Confirm</span></span>
<span data-ttu-id="6192b-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6192b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6192b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6192b-121">-WhatIf</span></span>
<span data-ttu-id="6192b-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6192b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6192b-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6192b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6192b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6192b-124">CommonParameters</span></span>
<span data-ttu-id="6192b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6192b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6192b-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6192b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6192b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6192b-127">INPUTS</span></span>

### <span data-ttu-id="6192b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6192b-128">System.String</span></span>

## <span data-ttu-id="6192b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6192b-129">OUTPUTS</span></span>

### <span data-ttu-id="6192b-130">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="6192b-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="6192b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6192b-131">NOTES</span></span>

## <span data-ttu-id="6192b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6192b-132">RELATED LINKS</span></span>