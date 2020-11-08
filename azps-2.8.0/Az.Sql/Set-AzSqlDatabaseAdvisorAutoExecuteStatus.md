---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 11f0d2429397578c622bb894db292d0c58a74122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920250"
---
# <span data-ttu-id="a9513-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9513-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="a9513-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9513-102">SYNOPSIS</span></span>
<span data-ttu-id="a9513-103">Ändrar automatisk körnings status för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="a9513-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="a9513-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9513-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9513-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9513-105">DESCRIPTION</span></span>
<span data-ttu-id="a9513-106">Cmdleten **set-AzSqlDatabaseAdvisorAutoExecuteStatus** ändrar egenskapen autoexecuting för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="a9513-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="a9513-107">För närvarande har denna cmdlet stöd för värdena Enabled, disabled och default.</span><span class="sxs-lookup"><span data-stu-id="a9513-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="a9513-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9513-108">EXAMPLES</span></span>

### <span data-ttu-id="a9513-109">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="a9513-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="a9513-110">Det här kommandot ändrar status för automatisk körning för en rådgivare med namnet CreateIndex till Enabled.</span><span class="sxs-lookup"><span data-stu-id="a9513-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="a9513-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9513-111">PARAMETERS</span></span>

### <span data-ttu-id="a9513-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a9513-112">-AdvisorName</span></span>
<span data-ttu-id="a9513-113">Anger namnet på den rådgivare för vilken denna cmdlet ändrar status.</span><span class="sxs-lookup"><span data-stu-id="a9513-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="a9513-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9513-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="a9513-115">Anger värdet för status.</span><span class="sxs-lookup"><span data-stu-id="a9513-115">Specifies the value for the status.</span></span>
<span data-ttu-id="a9513-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a9513-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9513-117">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="a9513-117">Enabled</span></span> 
- <span data-ttu-id="a9513-118">Aktiv</span><span class="sxs-lookup"><span data-stu-id="a9513-118">Disabled</span></span> 
- <span data-ttu-id="a9513-119">Vis</span><span class="sxs-lookup"><span data-stu-id="a9513-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9513-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9513-120">-DatabaseName</span></span>
<span data-ttu-id="a9513-121">Anger namnet på den databas som denna cmdlet ändrar status för.</span><span class="sxs-lookup"><span data-stu-id="a9513-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="a9513-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9513-122">-DefaultProfile</span></span>
<span data-ttu-id="a9513-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a9513-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9513-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9513-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9513-125">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="a9513-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="a9513-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9513-126">-ServerName</span></span>
<span data-ttu-id="a9513-127">Anger namnet på servern för databasen.</span><span class="sxs-lookup"><span data-stu-id="a9513-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="a9513-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9513-128">-Confirm</span></span>
<span data-ttu-id="a9513-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9513-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9513-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9513-130">-WhatIf</span></span>
<span data-ttu-id="a9513-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9513-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9513-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9513-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9513-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9513-133">CommonParameters</span></span>
<span data-ttu-id="a9513-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9513-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9513-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9513-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9513-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9513-136">INPUTS</span></span>

### <span data-ttu-id="a9513-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a9513-137">System.String</span></span>

### <span data-ttu-id="a9513-138">Microsoft. Azure. commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9513-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="a9513-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9513-139">OUTPUTS</span></span>

### <span data-ttu-id="a9513-140">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="a9513-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="a9513-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9513-141">NOTES</span></span>

## <span data-ttu-id="a9513-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9513-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9513-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="a9513-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="a9513-144">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a9513-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
