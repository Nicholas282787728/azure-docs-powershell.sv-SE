---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: 254f2def5a1be57840ea195f326534ce883870df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577392"
---
# <span data-ttu-id="c3cff-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="c3cff-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="c3cff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3cff-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cff-103">Skapar en Azure SQL Sync-agenttjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3cff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3cff-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3cff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3cff-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cff-106">Cmdleten **New-AzureRmSqlSyncAgentKey** skapar en Azure SQL Sync-agenttjänsten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="c3cff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3cff-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cff-108">Exempel 1: skapa en synkroniseringsresurs för en Azure SQL-synkroniseringsklient.</span><span class="sxs-lookup"><span data-stu-id="c3cff-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="c3cff-109">Det här kommandot skapar en synkroniseringsresurs för en Azure SQL-synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="c3cff-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c3cff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3cff-110">PARAMETERS</span></span>

### <span data-ttu-id="c3cff-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3cff-111">-Confirm</span></span>
<span data-ttu-id="c3cff-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3cff-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cff-113">-ResourceGroupName</span></span>
<span data-ttu-id="c3cff-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3cff-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c3cff-115">-ServerName</span></span>
<span data-ttu-id="c3cff-116">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="c3cff-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c3cff-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c3cff-117">-SyncAgentName</span></span>
<span data-ttu-id="c3cff-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c3cff-118">The sync agent name.</span></span>

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

### <span data-ttu-id="c3cff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cff-119">-WhatIf</span></span>
<span data-ttu-id="c3cff-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3cff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3cff-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3cff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cff-122">-DefaultProfile</span></span>
<span data-ttu-id="c3cff-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3cff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cff-124">CommonParameters</span></span>
<span data-ttu-id="c3cff-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cff-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cff-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3cff-127">INPUTS</span></span>

## <span data-ttu-id="c3cff-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3cff-128">OUTPUTS</span></span>

### <span data-ttu-id="c3cff-129">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="c3cff-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="c3cff-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3cff-130">NOTES</span></span>

## <span data-ttu-id="c3cff-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3cff-131">RELATED LINKS</span></span>

