---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584352"
---
# <span data-ttu-id="3f7d8-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3f7d8-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="3f7d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7d8-103">Skapar ett nytt projekt för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f7d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f7d8-104">SYNTAX</span></span>

### <span data-ttu-id="3f7d8-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f7d8-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3f7d8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f7d8-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3f7d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f7d8-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3f7d8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f7d8-108">DESCRIPTION</span></span>
<span data-ttu-id="3f7d8-109">New-AzureRmDataMigrationProject-cmdleten skapar ett nytt projekt för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="3f7d8-110">Denna cmdlet tar upp alla nödvändiga parametrar, till exempel namnet på Azure Resource-gruppen, namnet på Azure Data Migration-tjänsten där nya projekt skapas, det område där projektet ska skapas, det unika namnet på det nya projektet, käll-och mål anslutnings objekt samt mål typs objekt, som indata för listan över databaser som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="3f7d8-111">Använd New-AzureRmDataMigrationConnectionInfo cmdlet för att skapa ett nytt ConnectionInfo-objekt för både käll-och mål anslutningar.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="3f7d8-112">Listan över Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo förväntas för de valda databaserna; Du kan skapa det här objektet med hjälp av New-AzureRmDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="3f7d8-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f7d8-113">EXAMPLES</span></span>

### <span data-ttu-id="3f7d8-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f7d8-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="3f7d8-115">Det här exemplet visar hur du skapar ett nytt projekt med namnet MyDMSProject i området Central region under tjänsten Azure Database migration service instans med namnet TestService.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="3f7d8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f7d8-116">PARAMETERS</span></span>

### <span data-ttu-id="3f7d8-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f7d8-117">-Confirm</span></span>
<span data-ttu-id="3f7d8-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7d8-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="3f7d8-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="3f7d8-120">Databas information</span><span class="sxs-lookup"><span data-stu-id="3f7d8-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7d8-121">-DefaultProfile</span></span>
<span data-ttu-id="3f7d8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f7d8-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="3f7d8-123">-Location</span></span>
<span data-ttu-id="3f7d8-124">Platsen för Azure Database migration service-instans.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-125">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="3f7d8-125">-ProjectName</span></span>
<span data-ttu-id="3f7d8-126">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f7d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f7d8-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f7d8-129">-ServiceName</span></span>
<span data-ttu-id="3f7d8-130">Namnet på instansen för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="3f7d8-131">-SourceConnection</span></span>
<span data-ttu-id="3f7d8-132">Källans anslutnings information.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="3f7d8-133">-SourceType</span></span>
<span data-ttu-id="3f7d8-134">Käll plattforms typ för Project.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="3f7d8-135">-TargetConnection</span></span>
<span data-ttu-id="3f7d8-136">Mål anslutnings information.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7d8-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="3f7d8-137">-TargetType</span></span>
<span data-ttu-id="3f7d8-138">Mål plattforms typ för Project.</span><span class="sxs-lookup"><span data-stu-id="3f7d8-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="3f7d8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f7d8-139">OUTPUTS</span></span>

### <span data-ttu-id="3f7d8-140">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="3f7d8-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="3f7d8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f7d8-141">NOTES</span></span>

## <span data-ttu-id="3f7d8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f7d8-142">RELATED LINKS</span></span>

