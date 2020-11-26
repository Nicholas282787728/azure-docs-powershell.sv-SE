---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262908"
---
# <span data-ttu-id="85964-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="85964-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="85964-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85964-102">SYNOPSIS</span></span>
<span data-ttu-id="85964-103">Cmdleten **set-AzSqlInstanceDatabaseLongTermRetentionBackup** anger en bevarad bevarande princip för en hanterad databas.</span><span class="sxs-lookup"><span data-stu-id="85964-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="85964-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85964-104">SYNTAX</span></span>

### <span data-ttu-id="85964-105">WeeklyRetentionRequired (standard)</span><span class="sxs-lookup"><span data-stu-id="85964-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85964-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="85964-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85964-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="85964-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85964-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="85964-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85964-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85964-109">DESCRIPTION</span></span>
<span data-ttu-id="85964-110">Cmdleten **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** anger den långsiktiga bevarande principen för den här hanterade databasen.</span><span class="sxs-lookup"><span data-stu-id="85964-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="85964-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85964-111">EXAMPLES</span></span>

### <span data-ttu-id="85964-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85964-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="85964-113">Konfigurerar vecko principen för långsiktigt bevarande av en veckodag till en vecka.</span><span class="sxs-lookup"><span data-stu-id="85964-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="85964-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="85964-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="85964-115">Det här kommandot tar bort den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="85964-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="85964-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="85964-116">Example 3</span></span>

<span data-ttu-id="85964-117">Den Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdleten ställer in en beställnings princip för en hanterad databas.</span><span class="sxs-lookup"><span data-stu-id="85964-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="85964-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="85964-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="85964-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85964-119">PARAMETERS</span></span>

### <span data-ttu-id="85964-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="85964-120">-DatabaseName</span></span>
<span data-ttu-id="85964-121">Namnet på den Azure-hanterade databasen som ska användas.</span><span class="sxs-lookup"><span data-stu-id="85964-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="85964-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85964-122">-DefaultProfile</span></span>
<span data-ttu-id="85964-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85964-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85964-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="85964-124">-InstanceName</span></span>
<span data-ttu-id="85964-125">Namnet på den Azure-hanterade instans databasen tillhör.</span><span class="sxs-lookup"><span data-stu-id="85964-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="85964-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="85964-126">-MonthlyRetention</span></span>
<span data-ttu-id="85964-127">Månads kvarhållande.</span><span class="sxs-lookup"><span data-stu-id="85964-127">The Monthly Retention.</span></span>
<span data-ttu-id="85964-128">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="85964-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="85964-129">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="85964-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85964-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="85964-130">-RemovePolicy</span></span>
<span data-ttu-id="85964-131">Om det finns en princip för databasen rensas den.</span><span class="sxs-lookup"><span data-stu-id="85964-131">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85964-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85964-132">-ResourceGroupName</span></span>
<span data-ttu-id="85964-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="85964-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="85964-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="85964-134">-WeeklyRetention</span></span>
<span data-ttu-id="85964-135">Vecko kvarhållandet.</span><span class="sxs-lookup"><span data-stu-id="85964-135">The Weekly Retention.</span></span>
<span data-ttu-id="85964-136">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="85964-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="85964-137">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="85964-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85964-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="85964-138">-WeekOfYear</span></span>
<span data-ttu-id="85964-139">Veckan på året, 1 till 52, för att spara årligt bevarande.</span><span class="sxs-lookup"><span data-stu-id="85964-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85964-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="85964-140">-YearlyRetention</span></span>
<span data-ttu-id="85964-141">Årlig bevarande.</span><span class="sxs-lookup"><span data-stu-id="85964-141">The Yearly Retention.</span></span>
<span data-ttu-id="85964-142">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="85964-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="85964-143">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="85964-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85964-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85964-144">-Confirm</span></span>
<span data-ttu-id="85964-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85964-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85964-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85964-146">-WhatIf</span></span>
<span data-ttu-id="85964-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85964-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85964-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85964-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85964-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85964-149">CommonParameters</span></span>
<span data-ttu-id="85964-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85964-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85964-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85964-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85964-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85964-152">INPUTS</span></span>

### <span data-ttu-id="85964-153">System. String</span><span class="sxs-lookup"><span data-stu-id="85964-153">System.String</span></span>

### <span data-ttu-id="85964-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="85964-154">System.Int32</span></span>

## <span data-ttu-id="85964-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85964-155">OUTPUTS</span></span>

### <span data-ttu-id="85964-156">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="85964-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="85964-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85964-157">NOTES</span></span>

## <span data-ttu-id="85964-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85964-158">RELATED LINKS</span></span>

[<span data-ttu-id="85964-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="85964-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="85964-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="85964-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="85964-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="85964-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="85964-162">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="85964-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)