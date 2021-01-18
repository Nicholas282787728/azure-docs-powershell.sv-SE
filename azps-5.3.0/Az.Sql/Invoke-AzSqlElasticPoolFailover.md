---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525361"
---
# <span data-ttu-id="2a255-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="2a255-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="2a255-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a255-102">SYNOPSIS</span></span>
<span data-ttu-id="2a255-103">Redundansväxlas en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="2a255-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="2a255-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a255-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a255-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a255-105">DESCRIPTION</span></span>
<span data-ttu-id="2a255-106">Invoke-AzSqlElasticPoolFailover cmdlet redundans en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="2a255-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="2a255-107">Failover sker i alla databaser i den elastiska poolen när denna cmdlet har körts.</span><span class="sxs-lookup"><span data-stu-id="2a255-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="2a255-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a255-108">EXAMPLES</span></span>

### <span data-ttu-id="2a255-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a255-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2a255-110">Det här kommandot kommer att redundansväxla den elastiska poolen med namnet "ElasticPool01" på servern med namnet "Server01".</span><span class="sxs-lookup"><span data-stu-id="2a255-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="2a255-111">Det innebär att failover sker i alla databaser i den elastiska poolen med namnet "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="2a255-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="2a255-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a255-112">PARAMETERS</span></span>

### <span data-ttu-id="2a255-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a255-113">-AsJob</span></span>
<span data-ttu-id="2a255-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2a255-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a255-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a255-115">-DefaultProfile</span></span>
<span data-ttu-id="2a255-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a255-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a255-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2a255-117">-ElasticPoolName</span></span>
<span data-ttu-id="2a255-118">Namnet på den Elastic Azure SQL-poolen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2a255-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a255-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2a255-119">-Force</span></span>
<span data-ttu-id="2a255-120">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="2a255-120">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a255-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a255-121">-PassThru</span></span>
<span data-ttu-id="2a255-122">Returnerar true när den körs.</span><span class="sxs-lookup"><span data-stu-id="2a255-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="2a255-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2a255-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a255-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a255-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a255-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2a255-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a255-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2a255-126">-ServerName</span></span>
<span data-ttu-id="2a255-127">Namnet på den Azure SQL Server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="2a255-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="2a255-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a255-128">-Confirm</span></span>
<span data-ttu-id="2a255-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a255-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a255-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a255-130">-WhatIf</span></span>
<span data-ttu-id="2a255-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a255-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a255-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a255-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a255-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a255-133">CommonParameters</span></span>
<span data-ttu-id="2a255-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a255-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a255-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a255-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a255-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a255-136">INPUTS</span></span>

### <span data-ttu-id="2a255-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2a255-137">System.String</span></span>

## <span data-ttu-id="2a255-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a255-138">OUTPUTS</span></span>

## <span data-ttu-id="2a255-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a255-139">NOTES</span></span>

## <span data-ttu-id="2a255-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a255-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a255-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a255-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2a255-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2a255-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="2a255-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2a255-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2a255-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="2a255-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="2a255-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a255-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2a255-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a255-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2a255-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a255-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="2a255-148">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="2a255-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)