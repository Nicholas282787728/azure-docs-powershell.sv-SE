---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523005"
---
# <span data-ttu-id="f9609-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9609-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f9609-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9609-102">SYNOPSIS</span></span>
<span data-ttu-id="f9609-103">Hämtar en bevarad databas för den långsiktiga tids perioden</span><span class="sxs-lookup"><span data-stu-id="f9609-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="f9609-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9609-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9609-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9609-105">DESCRIPTION</span></span>
<span data-ttu-id="f9609-106">Cmdleten **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för den här hanterade databasen.</span><span class="sxs-lookup"><span data-stu-id="f9609-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="f9609-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="f9609-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="f9609-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9609-108">EXAMPLES</span></span>

### <span data-ttu-id="f9609-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9609-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="f9609-110">Hämtar den aktuella versionen av principen för långsiktigt bevarande för databasen</span><span class="sxs-lookup"><span data-stu-id="f9609-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="f9609-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9609-111">PARAMETERS</span></span>

### <span data-ttu-id="f9609-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9609-112">-DatabaseName</span></span>
<span data-ttu-id="f9609-113">Namnet på den Azure-hanterade databasen som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f9609-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="f9609-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9609-114">-DefaultProfile</span></span>
<span data-ttu-id="f9609-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9609-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9609-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f9609-116">-InstanceName</span></span>
<span data-ttu-id="f9609-117">Namnet på den Azure-hanterade instans databasen tillhör.</span><span class="sxs-lookup"><span data-stu-id="f9609-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="f9609-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9609-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9609-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9609-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9609-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9609-120">-Confirm</span></span>
<span data-ttu-id="f9609-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9609-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9609-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9609-122">-WhatIf</span></span>
<span data-ttu-id="f9609-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9609-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9609-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9609-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9609-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9609-125">CommonParameters</span></span>
<span data-ttu-id="f9609-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9609-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9609-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9609-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9609-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9609-128">INPUTS</span></span>

### <span data-ttu-id="f9609-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f9609-129">System.String</span></span>

## <span data-ttu-id="f9609-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9609-130">OUTPUTS</span></span>

### <span data-ttu-id="f9609-131">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f9609-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f9609-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9609-132">NOTES</span></span>

## <span data-ttu-id="f9609-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9609-133">RELATED LINKS</span></span>

[<span data-ttu-id="f9609-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f9609-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f9609-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f9609-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f9609-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9609-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f9609-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f9609-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)