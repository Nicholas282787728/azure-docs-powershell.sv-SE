---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927170"
---
# <span data-ttu-id="c5e27-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c5e27-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c5e27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5e27-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e27-103">Cmdleten **set-AzSqlInstanceDatabaseLongTermRetentionBackup** anger en bevarad bevarande princip för en hanterad databas.</span><span class="sxs-lookup"><span data-stu-id="c5e27-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="c5e27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5e27-104">SYNTAX</span></span>

### <span data-ttu-id="c5e27-105">WeeklyRetentionRequired (standard)</span><span class="sxs-lookup"><span data-stu-id="c5e27-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e27-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c5e27-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e27-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c5e27-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e27-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c5e27-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e27-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5e27-109">DESCRIPTION</span></span>
<span data-ttu-id="c5e27-110">Cmdleten **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** anger den långsiktiga bevarande principen för den här hanterade databasen.</span><span class="sxs-lookup"><span data-stu-id="c5e27-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="c5e27-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5e27-111">EXAMPLES</span></span>

### <span data-ttu-id="c5e27-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c5e27-112">Example 1</span></span>
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

<span data-ttu-id="c5e27-113">Konfigurerar vecko principen för långsiktigt bevarande av en veckodag till en vecka.</span><span class="sxs-lookup"><span data-stu-id="c5e27-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="c5e27-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c5e27-114">Example 2</span></span>
```
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


<span data-ttu-id="c5e27-115">Det här kommandot tar bort den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="c5e27-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="c5e27-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5e27-116">PARAMETERS</span></span>

### <span data-ttu-id="c5e27-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5e27-117">-DatabaseName</span></span>
<span data-ttu-id="c5e27-118">Namnet på den Azure-hanterade databasen som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c5e27-118">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e27-119">-DefaultProfile</span></span>
<span data-ttu-id="c5e27-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e27-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c5e27-121">-InstanceName</span></span>
<span data-ttu-id="c5e27-122">Namnet på den Azure-hanterade instans databasen tillhör.</span><span class="sxs-lookup"><span data-stu-id="c5e27-122">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="c5e27-123">-MonthlyRetention</span></span>
<span data-ttu-id="c5e27-124">Månads kvarhållande.</span><span class="sxs-lookup"><span data-stu-id="c5e27-124">The Monthly Retention.</span></span>
<span data-ttu-id="c5e27-125">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="c5e27-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c5e27-126">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="c5e27-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c5e27-127">-RemovePolicy</span></span>
<span data-ttu-id="c5e27-128">Om det finns en princip för databasen rensas den.</span><span class="sxs-lookup"><span data-stu-id="c5e27-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e27-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5e27-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c5e27-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="c5e27-131">-WeeklyRetention</span></span>
<span data-ttu-id="c5e27-132">Vecko kvarhållandet.</span><span class="sxs-lookup"><span data-stu-id="c5e27-132">The Weekly Retention.</span></span>
<span data-ttu-id="c5e27-133">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="c5e27-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c5e27-134">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="c5e27-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="c5e27-135">-WeekOfYear</span></span>
<span data-ttu-id="c5e27-136">Veckan på året, 1 till 52, för att spara årligt bevarande.</span><span class="sxs-lookup"><span data-stu-id="c5e27-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="c5e27-137">-YearlyRetention</span></span>
<span data-ttu-id="c5e27-138">Årlig bevarande.</span><span class="sxs-lookup"><span data-stu-id="c5e27-138">The Yearly Retention.</span></span>
<span data-ttu-id="c5e27-139">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="c5e27-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c5e27-140">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="c5e27-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5e27-141">-Confirm</span></span>
<span data-ttu-id="c5e27-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5e27-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e27-143">-WhatIf</span></span>
<span data-ttu-id="c5e27-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5e27-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e27-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5e27-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e27-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e27-146">CommonParameters</span></span>
<span data-ttu-id="c5e27-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e27-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e27-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5e27-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e27-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5e27-149">INPUTS</span></span>

### <span data-ttu-id="c5e27-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e27-150">System.String</span></span>

### <span data-ttu-id="c5e27-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c5e27-151">System.Int32</span></span>

## <span data-ttu-id="c5e27-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5e27-152">OUTPUTS</span></span>

### <span data-ttu-id="c5e27-153">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c5e27-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c5e27-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5e27-154">NOTES</span></span>

## <span data-ttu-id="c5e27-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5e27-155">RELATED LINKS</span></span>

[<span data-ttu-id="c5e27-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c5e27-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c5e27-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c5e27-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c5e27-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c5e27-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c5e27-159">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c5e27-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)