---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: e37a825a2da5f922a9a8a31bcc7f15a78f7cc38b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574771"
---
# <span data-ttu-id="6a204-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6a204-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="6a204-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a204-102">SYNOPSIS</span></span>
<span data-ttu-id="6a204-103">Ändrar automatisk körnings status för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="6a204-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a204-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a204-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a204-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a204-105">DESCRIPTION</span></span>
<span data-ttu-id="6a204-106">Cmdleten **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** ändrar egenskapen autoexecuting för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="6a204-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="6a204-107">För närvarande har denna cmdlet stöd för värdena Enabled, disabled och default.</span><span class="sxs-lookup"><span data-stu-id="6a204-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="6a204-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a204-108">EXAMPLES</span></span>

### <span data-ttu-id="6a204-109">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="6a204-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="6a204-110">Det här kommandot ändrar status för automatisk körning för en rådgivare med namnet CreateIndex till Enabled.</span><span class="sxs-lookup"><span data-stu-id="6a204-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="6a204-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a204-111">PARAMETERS</span></span>

### <span data-ttu-id="6a204-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6a204-112">-AdvisorName</span></span>
<span data-ttu-id="6a204-113">Anger namnet på den rådgivare för vilken denna cmdlet ändrar status.</span><span class="sxs-lookup"><span data-stu-id="6a204-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="6a204-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6a204-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="6a204-115">Anger värdet för status.</span><span class="sxs-lookup"><span data-stu-id="6a204-115">Specifies the value for the status.</span></span>
<span data-ttu-id="6a204-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6a204-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a204-117">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="6a204-117">Enabled</span></span> 
- <span data-ttu-id="6a204-118">Aktiv</span><span class="sxs-lookup"><span data-stu-id="6a204-118">Disabled</span></span> 
- <span data-ttu-id="6a204-119">Vis</span><span class="sxs-lookup"><span data-stu-id="6a204-119">Default</span></span>

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

### <span data-ttu-id="6a204-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a204-120">-DatabaseName</span></span>
<span data-ttu-id="6a204-121">Anger namnet på den databas som denna cmdlet ändrar status för.</span><span class="sxs-lookup"><span data-stu-id="6a204-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="6a204-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a204-122">-DefaultProfile</span></span>
<span data-ttu-id="6a204-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6a204-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a204-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a204-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a204-125">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="6a204-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="6a204-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a204-126">-ServerName</span></span>
<span data-ttu-id="6a204-127">Anger namnet på servern för databasen.</span><span class="sxs-lookup"><span data-stu-id="6a204-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="6a204-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a204-128">-Confirm</span></span>
<span data-ttu-id="6a204-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a204-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a204-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a204-130">-WhatIf</span></span>
<span data-ttu-id="6a204-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a204-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a204-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a204-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a204-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a204-133">CommonParameters</span></span>
<span data-ttu-id="6a204-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a204-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a204-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a204-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a204-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a204-136">INPUTS</span></span>

### <span data-ttu-id="6a204-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6a204-137">System.String</span></span>

### <span data-ttu-id="6a204-138">Microsoft. Azure. commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="6a204-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="6a204-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a204-139">OUTPUTS</span></span>

### <span data-ttu-id="6a204-140">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="6a204-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="6a204-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a204-141">NOTES</span></span>

## <span data-ttu-id="6a204-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a204-142">RELATED LINKS</span></span>

[<span data-ttu-id="6a204-143">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="6a204-143">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="6a204-144">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6a204-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

