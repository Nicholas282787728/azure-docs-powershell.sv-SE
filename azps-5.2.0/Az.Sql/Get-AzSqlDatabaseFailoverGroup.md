---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394275"
---
# <span data-ttu-id="c8654-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c8654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8654-102">SYNOPSIS</span></span>
<span data-ttu-id="c8654-103">Hämtar eller visar failover-grupper för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c8654-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="c8654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8654-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8654-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8654-105">DESCRIPTION</span></span>
<span data-ttu-id="c8654-106">Hämtar en specifik failover-grupp för Azure SQL-databasen eller listar failover-grupperna på en server.</span><span class="sxs-lookup"><span data-stu-id="c8654-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="c8654-107">Antingen kan server i gruppen failover användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="c8654-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="c8654-108">De returnerade värdena reflekterar statusen för den angivna servern med avseende på failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="c8654-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="c8654-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8654-109">EXAMPLES</span></span>

### <span data-ttu-id="c8654-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8654-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="c8654-111">Visar alla failover-grupper på en server.</span><span class="sxs-lookup"><span data-stu-id="c8654-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="c8654-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c8654-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="c8654-113">Skaffa en specifik failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="c8654-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="c8654-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c8654-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="c8654-115">Få alla failover-grupper på en server som börjar med "FG".</span><span class="sxs-lookup"><span data-stu-id="c8654-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="c8654-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8654-116">PARAMETERS</span></span>

### <span data-ttu-id="c8654-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8654-117">-DefaultProfile</span></span>
<span data-ttu-id="c8654-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8654-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8654-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c8654-119">-FailoverGroupName</span></span>
<span data-ttu-id="c8654-120">Namnet på den failover-grupp i Azure SQL-databasen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="c8654-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8654-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8654-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8654-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c8654-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8654-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8654-123">-ServerName</span></span>
<span data-ttu-id="c8654-124">Namnet på den Azure SQL Database-Server som du vill hämta failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="c8654-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="c8654-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8654-125">CommonParameters</span></span>
<span data-ttu-id="c8654-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8654-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8654-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8654-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8654-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8654-128">INPUTS</span></span>

### <span data-ttu-id="c8654-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c8654-129">System.String</span></span>

## <span data-ttu-id="c8654-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8654-130">OUTPUTS</span></span>

### <span data-ttu-id="c8654-131">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c8654-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c8654-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8654-132">NOTES</span></span>

## <span data-ttu-id="c8654-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8654-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8654-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c8654-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c8654-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c8654-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c8654-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c8654-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c8654-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c8654-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c8654-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
