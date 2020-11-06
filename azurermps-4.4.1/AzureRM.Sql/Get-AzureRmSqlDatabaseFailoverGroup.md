---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 0e07ce9eb3f3368e17c20a339c65a410b5f1d553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575786"
---
# <span data-ttu-id="7c988-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="7c988-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c988-102">SYNOPSIS</span></span>
<span data-ttu-id="7c988-103">Hämtar eller visar failover-grupper för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7c988-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c988-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c988-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c988-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c988-105">DESCRIPTION</span></span>
<span data-ttu-id="7c988-106">Hämtar en specifik failover-grupp för Azure SQL-databasen eller listar failover-grupperna på en server.</span><span class="sxs-lookup"><span data-stu-id="7c988-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="7c988-107">Antingen kan server i gruppen failover användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="7c988-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="7c988-108">De returnerade värdena reflekterar statusen för den angivna servern med avseende på failover-gruppen.</span><span class="sxs-lookup"><span data-stu-id="7c988-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="7c988-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c988-109">EXAMPLES</span></span>

### <span data-ttu-id="7c988-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c988-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="7c988-111">Visar alla failover-grupper på en server.</span><span class="sxs-lookup"><span data-stu-id="7c988-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="7c988-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7c988-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="7c988-113">Skaffa en specifik failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="7c988-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="7c988-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c988-114">PARAMETERS</span></span>

### <span data-ttu-id="7c988-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="7c988-115">-FailoverGroupName</span></span>
<span data-ttu-id="7c988-116">Namnet på den failover-grupp i Azure SQL-databasen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7c988-116">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="7c988-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c988-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c988-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7c988-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c988-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c988-119">-ServerName</span></span>
<span data-ttu-id="7c988-120">Namnet på den Azure SQL Database-Server som du vill hämta failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="7c988-120">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="7c988-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c988-121">-DefaultProfile</span></span>
<span data-ttu-id="7c988-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c988-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c988-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c988-123">CommonParameters</span></span>
<span data-ttu-id="7c988-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c988-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c988-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c988-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c988-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c988-126">INPUTS</span></span>

### <span data-ttu-id="7c988-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7c988-127">System.String</span></span>

## <span data-ttu-id="7c988-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c988-128">OUTPUTS</span></span>

### <span data-ttu-id="7c988-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="7c988-129">System.Object</span></span>

## <span data-ttu-id="7c988-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c988-130">NOTES</span></span>

## <span data-ttu-id="7c988-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c988-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c988-132">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7c988-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7c988-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="7c988-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="7c988-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7c988-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7c988-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7c988-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7c988-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
