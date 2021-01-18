---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520484"
---
# <span data-ttu-id="3e1e3-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="3e1e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1e3-103">Ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="3e1e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e1e3-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e1e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e1e3-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1e3-106">Det här kommandot ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="3e1e3-107">Gruppens primära server bör användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="3e1e3-108">Använd "Add-AzSqlDatabaseToFailoverGroup" och "Remove-AzSqlDatabaseFromFailoverGroup" i stället för att styra uppsättningen av databaser i gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="3e1e3-109">Under för hands versionen av funktionen failover Groups kan bara värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="3e1e3-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="3e1e3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e1e3-110">EXAMPLES</span></span>

### <span data-ttu-id="3e1e3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e1e3-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="3e1e3-112">Ställer in failover-principen för en failover till "Automatic".</span><span class="sxs-lookup"><span data-stu-id="3e1e3-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="3e1e3-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3e1e3-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="3e1e3-114">Ställer in en failover-princip för redundansväxling till "Manual" i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="3e1e3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e1e3-115">PARAMETERS</span></span>

### <span data-ttu-id="3e1e3-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="3e1e3-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="3e1e3-117">Om avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1e3-118">-DefaultProfile</span></span>
<span data-ttu-id="3e1e3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3e1e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1e3-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1e3-120">-FailoverGroupName</span></span>
<span data-ttu-id="3e1e3-121">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="3e1e3-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="3e1e3-122">-FailoverPolicy</span></span>
<span data-ttu-id="3e1e3-123">Failover-principen för failover-gruppen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e3-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="3e1e3-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="3e1e3-125">Intervallet innan automatisk redundans initieras om ett avbrott inträffar på den primära servern.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="3e1e3-126">Detta indikerar att Azure SQL Database inte initierar automatisk redundans innan respittiden förfaller.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="3e1e3-127">Observera att Redundansåtgärden med AllowDataLoss-alternativet kan orsaka data förlust på grund av asynkron synkronisering.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e1e3-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e1e3-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e1e3-130">-ServerName</span></span>
<span data-ttu-id="3e1e3-131">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3e1e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1e3-132">CommonParameters</span></span>
<span data-ttu-id="3e1e3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1e3-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e1e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1e3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e1e3-135">INPUTS</span></span>

### <span data-ttu-id="3e1e3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1e3-136">System.String</span></span>

## <span data-ttu-id="3e1e3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e1e3-137">OUTPUTS</span></span>

### <span data-ttu-id="3e1e3-138">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="3e1e3-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="3e1e3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e1e3-139">NOTES</span></span>

## <span data-ttu-id="3e1e3-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e1e3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e1e3-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3e1e3-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3e1e3-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="3e1e3-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="3e1e3-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3e1e3-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3e1e3-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3e1e3-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3e1e3-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
