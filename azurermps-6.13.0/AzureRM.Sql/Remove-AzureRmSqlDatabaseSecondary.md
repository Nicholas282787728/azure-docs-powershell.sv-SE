---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: f1bc8fcc019f25b4337dc88ac55965b8d988e753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579907"
---
# <span data-ttu-id="6b843-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6b843-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="6b843-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b843-102">SYNOPSIS</span></span>
<span data-ttu-id="6b843-103">Avbryter datareplikeringen mellan en SQL-databas och den angivna sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="6b843-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b843-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b843-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b843-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b843-105">DESCRIPTION</span></span>
<span data-ttu-id="6b843-106">Cmdleten **Remove-AzureRmSqlDatabaseSecondary** tvingar fram en geo-replikeringslänk.</span><span class="sxs-lookup"><span data-stu-id="6b843-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="6b843-107">Denna cmdlet ersätter Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b843-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="6b843-108">Det finns ingen replikerings-synkronisering före uppsägning.</span><span class="sxs-lookup"><span data-stu-id="6b843-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="6b843-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b843-109">EXAMPLES</span></span>

## <span data-ttu-id="6b843-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b843-110">PARAMETERS</span></span>

### <span data-ttu-id="6b843-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b843-111">-DatabaseName</span></span>
<span data-ttu-id="6b843-112">Anger namnet på den primära Azure SQL-databas som innehåller replikeringslänken som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="6b843-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b843-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b843-113">-DefaultProfile</span></span>
<span data-ttu-id="6b843-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6b843-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b843-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b843-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6b843-116">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6b843-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="6b843-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="6b843-117">-PartnerServerName</span></span>
<span data-ttu-id="6b843-118">Anger namnet på partner-SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="6b843-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="6b843-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b843-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b843-120">Anger namnet på den resurs grupp som är kopplad till replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6b843-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="6b843-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b843-121">-ServerName</span></span>
<span data-ttu-id="6b843-122">Anger namnet på den SQL Server som innehåller replikeringslänken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6b843-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="6b843-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b843-123">-Confirm</span></span>
<span data-ttu-id="6b843-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b843-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b843-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b843-125">-WhatIf</span></span>
<span data-ttu-id="6b843-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b843-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b843-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b843-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b843-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b843-128">CommonParameters</span></span>
<span data-ttu-id="6b843-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b843-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b843-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b843-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b843-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b843-131">INPUTS</span></span>

### <span data-ttu-id="6b843-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6b843-132">System.String</span></span>

## <span data-ttu-id="6b843-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b843-133">OUTPUTS</span></span>

### <span data-ttu-id="6b843-134">Microsoft. Azure. commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="6b843-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="6b843-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b843-135">NOTES</span></span>

## <span data-ttu-id="6b843-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b843-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b843-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6b843-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6b843-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6b843-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6b843-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6b843-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
