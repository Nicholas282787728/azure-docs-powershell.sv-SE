---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 5b9bd64eb4d83af9ca150e5eb9ac04479c7fdf5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746664"
---
# <span data-ttu-id="0bbf8-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="0bbf8-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="0bbf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbf8-103">Hämtar tjänste mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="0bbf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bbf8-104">SYNTAX</span></span>

### <span data-ttu-id="0bbf8-105">ByLocation (standard)</span><span class="sxs-lookup"><span data-stu-id="0bbf8-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bbf8-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="0bbf8-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bbf8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bbf8-107">DESCRIPTION</span></span>
<span data-ttu-id="0bbf8-108">Cmdleten **Get-AzSqlServerServiceObjective** hämtar de tillgängliga tjänst målen för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="0bbf8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bbf8-109">EXAMPLES</span></span>

### <span data-ttu-id="0bbf8-110">Exempel 1: få service mål</span><span class="sxs-lookup"><span data-stu-id="0bbf8-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="0bbf8-111">Det här kommandot hämtar tjänst målen för servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="0bbf8-112">Exempel 2: få service mål med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="0bbf8-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="0bbf8-113">Det här kommandot får tjänst målen för servern med namnet Server01 som börjar med "system".</span><span class="sxs-lookup"><span data-stu-id="0bbf8-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="0bbf8-114">Exempel 3: få service mål för en plats</span><span class="sxs-lookup"><span data-stu-id="0bbf8-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="0bbf8-115">Med det här kommandot får du tjänst målen för angiven Azure-region.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="0bbf8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bbf8-116">PARAMETERS</span></span>

### <span data-ttu-id="0bbf8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbf8-117">-DefaultProfile</span></span>
<span data-ttu-id="0bbf8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0bbf8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bbf8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0bbf8-119">-Location</span></span>
<span data-ttu-id="0bbf8-120">Namnet på den plats där du ska få tjänstens mål.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbf8-121">-ResourceGroupName</span></span>
<span data-ttu-id="0bbf8-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0bbf8-123">Denna cmdlet hämtar tjänst mål för en SQL-databasserver som tilldelats den här resursen.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0bbf8-124">-ServerName</span></span>
<span data-ttu-id="0bbf8-125">Anger namnet på en SQL-databasserver i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf8-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0bbf8-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="0bbf8-127">Anger namnet på ett tjänst mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="0bbf8-128">De acceptabla värdena för den här parametern är: Basic, S0, S1, S2, P1, P2 och P3.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0bbf8-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bbf8-129">-Confirm</span></span>
<span data-ttu-id="0bbf8-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bbf8-131">-WhatIf</span></span>
<span data-ttu-id="0bbf8-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bbf8-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbf8-134">CommonParameters</span></span>
<span data-ttu-id="0bbf8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bbf8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbf8-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bbf8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbf8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bbf8-137">INPUTS</span></span>

### <span data-ttu-id="0bbf8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0bbf8-138">System.String</span></span>

## <span data-ttu-id="0bbf8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bbf8-139">OUTPUTS</span></span>

### <span data-ttu-id="0bbf8-140">Microsoft. Azure. commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="0bbf8-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="0bbf8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bbf8-141">NOTES</span></span>

## <span data-ttu-id="0bbf8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bbf8-142">RELATED LINKS</span></span>

[<span data-ttu-id="0bbf8-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0bbf8-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


