---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090920"
---
# <span data-ttu-id="4dbcb-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4dbcb-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4dbcb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dbcb-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbcb-103">Avbryter datareplikeringen mellan en SQL-databas och den angivna sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="4dbcb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dbcb-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dbcb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dbcb-105">DESCRIPTION</span></span>
<span data-ttu-id="4dbcb-106">Cmdleten **Remove-AzSqlDatabaseSecondary** tvingar fram en geo-replikeringslänk.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="4dbcb-107">Denna cmdlet ersätter Stop-AzSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="4dbcb-108">Det finns ingen replikerings-synkronisering före uppsägning.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="4dbcb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dbcb-109">EXAMPLES</span></span>

## <span data-ttu-id="4dbcb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dbcb-110">PARAMETERS</span></span>

### <span data-ttu-id="4dbcb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4dbcb-111">-DatabaseName</span></span>
<span data-ttu-id="4dbcb-112">Anger namnet på den primära Azure SQL-databas som innehåller replikeringslänken som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4dbcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbcb-113">-DefaultProfile</span></span>
<span data-ttu-id="4dbcb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4dbcb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dbcb-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbcb-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4dbcb-116">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="4dbcb-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="4dbcb-117">-PartnerServerName</span></span>
<span data-ttu-id="4dbcb-118">Anger namnet på partner-SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="4dbcb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbcb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4dbcb-120">Anger namnet på den resurs grupp som är kopplad till replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="4dbcb-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4dbcb-121">-ServerName</span></span>
<span data-ttu-id="4dbcb-122">Anger namnet på den SQL Server som innehåller replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="4dbcb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dbcb-123">-Confirm</span></span>
<span data-ttu-id="4dbcb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbcb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dbcb-125">-WhatIf</span></span>
<span data-ttu-id="4dbcb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dbcb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbcb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbcb-128">CommonParameters</span></span>
<span data-ttu-id="4dbcb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dbcb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbcb-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dbcb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbcb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dbcb-131">INPUTS</span></span>

### <span data-ttu-id="4dbcb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4dbcb-132">System.String</span></span>

## <span data-ttu-id="4dbcb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dbcb-133">OUTPUTS</span></span>

### <span data-ttu-id="4dbcb-134">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4dbcb-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4dbcb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dbcb-135">NOTES</span></span>

## <span data-ttu-id="4dbcb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dbcb-136">RELATED LINKS</span></span>

[<span data-ttu-id="4dbcb-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4dbcb-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4dbcb-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4dbcb-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4dbcb-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4dbcb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)