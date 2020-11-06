---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583423"
---
# <span data-ttu-id="c68d5-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c68d5-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="c68d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c68d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c68d5-103">Tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="c68d5-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c68d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c68d5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c68d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c68d5-105">DESCRIPTION</span></span>
<span data-ttu-id="c68d5-106">Cmdleten **Remove-AzureRmSqlSyncAgent** tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="c68d5-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c68d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c68d5-107">EXAMPLES</span></span>

### <span data-ttu-id="c68d5-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="c68d5-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="c68d5-109">Det här kommandot tar bort Azure SQL Sync-agenten med namnet syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="c68d5-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="c68d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c68d5-110">PARAMETERS</span></span>

### <span data-ttu-id="c68d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68d5-111">-DefaultProfile</span></span>
<span data-ttu-id="c68d5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c68d5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c68d5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c68d5-113">-Force</span></span>
<span data-ttu-id="c68d5-114">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="c68d5-114">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68d5-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c68d5-115">-Name</span></span>
<span data-ttu-id="c68d5-116">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c68d5-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c68d5-117">-PassThru</span></span>
<span data-ttu-id="c68d5-118">Definierar om returnera den borttagna synkroniseringsresursen</span><span class="sxs-lookup"><span data-stu-id="c68d5-118">Defines Whether return the removed sync agent</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="c68d5-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c68d5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c68d5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c68d5-121">-ServerName</span></span>
<span data-ttu-id="c68d5-122">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="c68d5-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c68d5-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c68d5-123">-Confirm</span></span>
<span data-ttu-id="c68d5-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c68d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68d5-125">-WhatIf</span></span>
<span data-ttu-id="c68d5-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c68d5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68d5-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c68d5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68d5-128">CommonParameters</span></span>
<span data-ttu-id="c68d5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68d5-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68d5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68d5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c68d5-131">INPUTS</span></span>

### <span data-ttu-id="c68d5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c68d5-132">System.String</span></span>

## <span data-ttu-id="c68d5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c68d5-133">OUTPUTS</span></span>

### <span data-ttu-id="c68d5-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="c68d5-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c68d5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c68d5-135">NOTES</span></span>

## <span data-ttu-id="c68d5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c68d5-136">RELATED LINKS</span></span>

[<span data-ttu-id="c68d5-137">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c68d5-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="c68d5-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c68d5-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

