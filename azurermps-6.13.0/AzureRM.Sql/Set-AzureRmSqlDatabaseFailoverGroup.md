---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 98a6ceafed2c7c62301c63ff1c8b3028c46e1201
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575079"
---
# <span data-ttu-id="79f1e-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="79f1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="79f1e-103">Ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79f1e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79f1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="79f1e-106">Det här kommandot ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="79f1e-107">Gruppens primära server bör användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="79f1e-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="79f1e-108">Använd "Add-AzureRmSqlDatabaseToFailoverGroup" och "Remove-AzureRmSqlDatabaseFromFailoverGroup" i stället för att styra uppsättningen av databaser i gruppen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="79f1e-109">Under för hands versionen av funktionen failover Groups kan bara värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="79f1e-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="79f1e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="79f1e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79f1e-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="79f1e-112">Ställer in failover-principen för en failover till "Automatic".</span><span class="sxs-lookup"><span data-stu-id="79f1e-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="79f1e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="79f1e-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="79f1e-114">Ställer in en failover-princip för redundansväxling till "Manual" i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="79f1e-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="79f1e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79f1e-115">PARAMETERS</span></span>

### <span data-ttu-id="79f1e-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="79f1e-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="79f1e-117">Om avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="79f1e-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="79f1e-118">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="79f1e-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="79f1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f1e-119">-DefaultProfile</span></span>
<span data-ttu-id="79f1e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="79f1e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f1e-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="79f1e-121">-FailoverGroupName</span></span>
<span data-ttu-id="79f1e-122">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="79f1e-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="79f1e-123">-FailoverPolicy</span></span>
<span data-ttu-id="79f1e-124">Failover-principen för failover-gruppen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="79f1e-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="79f1e-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="79f1e-126">Intervallet innan automatisk redundans initieras om ett avbrott inträffar på den primära servern.</span><span class="sxs-lookup"><span data-stu-id="79f1e-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="79f1e-127">Detta indikerar att Azure SQL Database inte initierar automatisk redundans innan respittiden förfaller.</span><span class="sxs-lookup"><span data-stu-id="79f1e-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="79f1e-128">Observera att Redundansåtgärden med AllowDataLoss-alternativet kan orsaka data förlust på grund av asynkron synkronisering.</span><span class="sxs-lookup"><span data-stu-id="79f1e-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="79f1e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f1e-129">-ResourceGroupName</span></span>
<span data-ttu-id="79f1e-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79f1e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="79f1e-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79f1e-131">-ServerName</span></span>
<span data-ttu-id="79f1e-132">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="79f1e-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="79f1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f1e-133">CommonParameters</span></span>
<span data-ttu-id="79f1e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f1e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f1e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f1e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79f1e-136">INPUTS</span></span>

### <span data-ttu-id="79f1e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79f1e-137">System.String</span></span>

## <span data-ttu-id="79f1e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79f1e-138">OUTPUTS</span></span>

### <span data-ttu-id="79f1e-139">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="79f1e-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="79f1e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79f1e-140">NOTES</span></span>

## <span data-ttu-id="79f1e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79f1e-141">RELATED LINKS</span></span>

[<span data-ttu-id="79f1e-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79f1e-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79f1e-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="79f1e-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="79f1e-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79f1e-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79f1e-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79f1e-148">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="79f1e-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
