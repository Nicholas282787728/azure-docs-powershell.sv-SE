---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: d1f1ae44cf1b6d1b6d3afffa3e13ea34c1ffeb51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916805"
---
# <span data-ttu-id="e6fd2-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e6fd2-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="e6fd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fd2-103">Skapar ett nytt projekt för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="e6fd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6fd2-104">SYNTAX</span></span>

### <span data-ttu-id="e6fd2-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e6fd2-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fd2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fd2-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fd2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fd2-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6fd2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6fd2-108">DESCRIPTION</span></span>
<span data-ttu-id="e6fd2-109">New-AzDataMigrationProject-cmdleten skapar ett nytt projekt för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="e6fd2-110">Denna cmdlet tar upp alla nödvändiga parametrar, till exempel namnet på Azure Resource-gruppen, namnet på Azure Data Migration-tjänsten där nya projekt skapas, det område där projektet ska skapas, det unika namnet på det nya projektet, käll-och mål anslutnings objekt samt mål typs objekt, som indata för listan över databaser som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="e6fd2-111">Använd New-AzDataMigrationConnectionInfo cmdlet för att skapa ett nytt ConnectionInfo-objekt för både käll-och mål anslutningar.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="e6fd2-112">Listan över Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo förväntas för de valda databaserna; Du kan skapa det här objektet med hjälp av New-AzDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="e6fd2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6fd2-113">EXAMPLES</span></span>

### <span data-ttu-id="e6fd2-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6fd2-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="e6fd2-115">Det här exemplet visar hur du skapar ett nytt projekt med namnet MyDMSProject i området Central region under tjänsten Azure Database migration service instans med namnet TestService.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="e6fd2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6fd2-116">PARAMETERS</span></span>

### <span data-ttu-id="e6fd2-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="e6fd2-117">-DatabaseInfo</span></span>
<span data-ttu-id="e6fd2-118">Databas information.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fd2-119">-DefaultProfile</span></span>
<span data-ttu-id="e6fd2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6fd2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6fd2-121">-InputObject</span></span>
<span data-ttu-id="e6fd2-122">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="e6fd2-123">-Location</span></span>
<span data-ttu-id="e6fd2-124">Platsen för Azure Database migration service-instans.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="e6fd2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6fd2-125">-Name</span></span>
<span data-ttu-id="e6fd2-126">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fd2-127">-ResourceGroupName</span></span>
<span data-ttu-id="e6fd2-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6fd2-129">-ResourceId</span></span>
<span data-ttu-id="e6fd2-130">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e6fd2-131">-ServiceName</span></span>
<span data-ttu-id="e6fd2-132">Namnet på instansen för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="e6fd2-133">-SourceConnection</span></span>
<span data-ttu-id="e6fd2-134">Källans anslutnings information.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e6fd2-135">-SourceType</span></span>
<span data-ttu-id="e6fd2-136">Käll plattforms typ för Project.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="e6fd2-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="e6fd2-137">-TargetConnection</span></span>
<span data-ttu-id="e6fd2-138">Mål anslutnings information.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fd2-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="e6fd2-139">-TargetType</span></span>
<span data-ttu-id="e6fd2-140">Mål plattforms typ för Project.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="e6fd2-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6fd2-141">-Confirm</span></span>
<span data-ttu-id="e6fd2-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fd2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fd2-143">-WhatIf</span></span>
<span data-ttu-id="e6fd2-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6fd2-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fd2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fd2-146">CommonParameters</span></span>
<span data-ttu-id="e6fd2-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6fd2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fd2-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fd2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fd2-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6fd2-149">INPUTS</span></span>

### <span data-ttu-id="e6fd2-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e6fd2-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e6fd2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e6fd2-151">System.String</span></span>

## <span data-ttu-id="e6fd2-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6fd2-152">OUTPUTS</span></span>

### <span data-ttu-id="e6fd2-153">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="e6fd2-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="e6fd2-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6fd2-154">NOTES</span></span>

## <span data-ttu-id="e6fd2-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6fd2-155">RELATED LINKS</span></span>