---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576684"
---
# <span data-ttu-id="257fc-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="257fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="257fc-102">SYNOPSIS</span></span>
<span data-ttu-id="257fc-103">Ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="257fc-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="257fc-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="257fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="257fc-105">DESCRIPTION</span></span>
<span data-ttu-id="257fc-106">Det här kommandot ändrar konfigurationen för en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="257fc-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="257fc-107">Gruppens primära server bör användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="257fc-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="257fc-108">Använd "Add-AzureRmSqlDatabaseToFailoverGroup" och "Remove-AzureRmSqlDatabaseFromFailoverGroup" i stället för att styra uppsättningen av databaser i gruppen.</span><span class="sxs-lookup"><span data-stu-id="257fc-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="257fc-109">Under för hands versionen av funktionen failover Groups kan bara värden som är större än eller lika med 1 timme användas för parametern "-GracePeriodWithDataLossHours".</span><span class="sxs-lookup"><span data-stu-id="257fc-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="257fc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="257fc-110">EXAMPLES</span></span>

### <span data-ttu-id="257fc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="257fc-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="257fc-112">Ställer in failover-principen för en failover till "Automatic".</span><span class="sxs-lookup"><span data-stu-id="257fc-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="257fc-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="257fc-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="257fc-114">Ställer in en failover-princip för redundansväxling till "Manual" i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="257fc-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="257fc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="257fc-115">PARAMETERS</span></span>

### <span data-ttu-id="257fc-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="257fc-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="257fc-117">Om avbrott på den sekundära servern ska utlösa automatisk redundans av den skrivskyddade slut punkten.</span><span class="sxs-lookup"><span data-stu-id="257fc-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="257fc-118">Den här funktionen stöds inte ännu.</span><span class="sxs-lookup"><span data-stu-id="257fc-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="257fc-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="257fc-119">-FailoverGroupName</span></span>
<span data-ttu-id="257fc-120">Namnet på failover-gruppen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="257fc-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="257fc-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="257fc-121">-FailoverPolicy</span></span>
<span data-ttu-id="257fc-122">Failover-principen för failover-gruppen i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="257fc-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="257fc-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="257fc-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="257fc-124">Intervallet innan automatisk redundans initieras om det uppstår ett avbrott på den primära servern och redundansväxlingen inte kan slutföras utan data förlust.</span><span class="sxs-lookup"><span data-stu-id="257fc-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="257fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="257fc-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="257fc-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="257fc-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="257fc-127">-ServerName</span></span>
<span data-ttu-id="257fc-128">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="257fc-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="257fc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257fc-129">-DefaultProfile</span></span>
<span data-ttu-id="257fc-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="257fc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="257fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257fc-131">CommonParameters</span></span>
<span data-ttu-id="257fc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257fc-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257fc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257fc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="257fc-134">INPUTS</span></span>

### <span data-ttu-id="257fc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="257fc-135">System.String</span></span>

## <span data-ttu-id="257fc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="257fc-136">OUTPUTS</span></span>

### <span data-ttu-id="257fc-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="257fc-137">System.Object</span></span>

## <span data-ttu-id="257fc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="257fc-138">NOTES</span></span>

## <span data-ttu-id="257fc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="257fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="257fc-140">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="257fc-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="257fc-142">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="257fc-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="257fc-144">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="257fc-145">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="257fc-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="257fc-146">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="257fc-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
