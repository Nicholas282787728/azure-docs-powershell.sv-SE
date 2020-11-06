---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c5dd678a851e663b04746bb4a5780624ea4c5f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583432"
---
# <span data-ttu-id="eb592-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="eb592-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb592-102">SYNOPSIS</span></span>
<span data-ttu-id="eb592-103">Det här kommandot skapar en ny failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="eb592-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb592-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb592-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb592-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb592-105">DESCRIPTION</span></span>
<span data-ttu-id="eb592-106">Skapar en ny failover-grupp för Azure SQL-databasen för de angivna servrarna.</span><span class="sxs-lookup"><span data-stu-id="eb592-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="eb592-107">Två slut punkter för Azure SQL Database TDS skapas på FailoverGroupName. SqlDatabaseDnsSuffix (till exempel FailoverGroupName.database.windows.net) och FailoverGroupName. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="eb592-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="eb592-108">Dessa slut punkter kan användas för att ansluta till den primära och sekundära servern i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="eb592-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="eb592-109">Om den primära servern påverkas av ett avbrott utlöses automatisk redundans för slut punkterna och databaserna som styrs av failover-gruppens failover-princip och Grace-period.</span><span class="sxs-lookup"><span data-stu-id="eb592-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="eb592-110">Nyskapade failover-grupper innehåller inte några databaser.</span><span class="sxs-lookup"><span data-stu-id="eb592-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="eb592-111">Om du vill styra uppsättningen databaser i en failover-grupp använder du cmdletarna Add-AzureRmSqlDatabaseToFailoverGroup och Remove-AzureRmSqlDatabaseFromFailoverGroup.</span><span class="sxs-lookup"><span data-stu-id="eb592-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="eb592-112">Under för hands versionen av funktionen failover Groups kan bara värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="eb592-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="eb592-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb592-113">EXAMPLES</span></span>

### <span data-ttu-id="eb592-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb592-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="eb592-115">Det här kommandot skapar en ny failover-grupp med växlings principen "automatisk" för två servrar i samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eb592-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="eb592-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="eb592-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="eb592-117">Det här kommandot skapar en ny failover-grupp med fjärråtkomstprincipen "Manual" för två servrar i olika resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="eb592-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="eb592-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb592-118">PARAMETERS</span></span>

### <span data-ttu-id="eb592-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="eb592-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="eb592-120">Om ett avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="eb592-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="eb592-121">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="eb592-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="eb592-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb592-122">-DefaultProfile</span></span>
<span data-ttu-id="eb592-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eb592-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb592-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="eb592-124">-FailoverGroupName</span></span>
<span data-ttu-id="eb592-125">Namnet på den failover-grupp i Azure SQL-databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="eb592-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb592-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="eb592-126">-FailoverPolicy</span></span>
<span data-ttu-id="eb592-127">Failover-principen för failover-gruppen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="eb592-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="eb592-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="eb592-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="eb592-129">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="eb592-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="eb592-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb592-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="eb592-131">Namnet på den sekundära resurs gruppen i failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="eb592-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb592-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="eb592-132">-PartnerServerName</span></span>
<span data-ttu-id="eb592-133">Namnet på den sekundära servern i gruppen failover för Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="eb592-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb592-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb592-134">-ResourceGroupName</span></span>
<span data-ttu-id="eb592-135">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb592-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb592-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb592-136">-ServerName</span></span>
<span data-ttu-id="eb592-137">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="eb592-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="eb592-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb592-138">CommonParameters</span></span>
<span data-ttu-id="eb592-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb592-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb592-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb592-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb592-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb592-141">INPUTS</span></span>

### <span data-ttu-id="eb592-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb592-142">System.String</span></span>

## <span data-ttu-id="eb592-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb592-143">OUTPUTS</span></span>

### <span data-ttu-id="eb592-144">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="eb592-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="eb592-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb592-145">NOTES</span></span>

## <span data-ttu-id="eb592-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb592-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb592-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="eb592-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="eb592-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="eb592-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="eb592-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="eb592-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="eb592-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="eb592-153">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="eb592-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
