---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755572"
---
# <span data-ttu-id="ce13d-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ce13d-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="ce13d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce13d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce13d-103">Ändrar automatisk körnings status för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="ce13d-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce13d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce13d-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce13d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce13d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce13d-106">Cmdleten **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** ändrar egenskapen autoexecuting för en Azure SQL-databas rådgivare.</span><span class="sxs-lookup"><span data-stu-id="ce13d-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="ce13d-107">För närvarande har denna cmdlet stöd för värdena Enabled, disabled och default.</span><span class="sxs-lookup"><span data-stu-id="ce13d-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="ce13d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce13d-108">EXAMPLES</span></span>

### <span data-ttu-id="ce13d-109">Exempel 1: Aktivera automatisk körning för en rådgivare</span><span class="sxs-lookup"><span data-stu-id="ce13d-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="ce13d-110">Det här kommandot ändrar status för automatisk körning för en rådgivare med namnet CreateIndex till Enabled.</span><span class="sxs-lookup"><span data-stu-id="ce13d-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="ce13d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce13d-111">PARAMETERS</span></span>

### <span data-ttu-id="ce13d-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ce13d-112">-AdvisorName</span></span>
<span data-ttu-id="ce13d-113">Anger namnet på den rådgivare för vilken denna cmdlet ändrar status.</span><span class="sxs-lookup"><span data-stu-id="ce13d-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13d-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="ce13d-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="ce13d-115">Anger värdet för status.</span><span class="sxs-lookup"><span data-stu-id="ce13d-115">Specifies the value for the status.</span></span>
<span data-ttu-id="ce13d-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ce13d-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce13d-117">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="ce13d-117">Enabled</span></span> 
- <span data-ttu-id="ce13d-118">Aktiv</span><span class="sxs-lookup"><span data-stu-id="ce13d-118">Disabled</span></span> 
- <span data-ttu-id="ce13d-119">Vis</span><span class="sxs-lookup"><span data-stu-id="ce13d-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce13d-120">-DatabaseName</span></span>
<span data-ttu-id="ce13d-121">Anger namnet på den databas som denna cmdlet ändrar status för.</span><span class="sxs-lookup"><span data-stu-id="ce13d-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce13d-122">-DefaultProfile</span></span>
<span data-ttu-id="ce13d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ce13d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce13d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce13d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce13d-125">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="ce13d-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="ce13d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce13d-126">-ServerName</span></span>
<span data-ttu-id="ce13d-127">Anger namnet på servern för databasen.</span><span class="sxs-lookup"><span data-stu-id="ce13d-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce13d-128">-Confirm</span></span>
<span data-ttu-id="ce13d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce13d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce13d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce13d-130">-WhatIf</span></span>
<span data-ttu-id="ce13d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce13d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce13d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce13d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce13d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce13d-133">CommonParameters</span></span>
<span data-ttu-id="ce13d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce13d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce13d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce13d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce13d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce13d-136">INPUTS</span></span>

### <span data-ttu-id="ce13d-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce13d-137">None</span></span>
<span data-ttu-id="ce13d-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ce13d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce13d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce13d-139">OUTPUTS</span></span>

### <span data-ttu-id="ce13d-140">Microsoft. Azure. commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="ce13d-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="ce13d-141">Denna cmdlet returnerar ett **AzureSqlDatabaseAdvisorModel** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ce13d-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="ce13d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce13d-142">NOTES</span></span>

## <span data-ttu-id="ce13d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce13d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ce13d-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="ce13d-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="ce13d-145">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ce13d-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

