---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583191"
---
# <span data-ttu-id="39f1c-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="39f1c-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="39f1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="39f1c-103">Hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="39f1c-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39f1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39f1c-104">SYNTAX</span></span>

### <span data-ttu-id="39f1c-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="39f1c-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="39f1c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f1c-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="39f1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f1c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="39f1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39f1c-108">DESCRIPTION</span></span>
<span data-ttu-id="39f1c-109">Get-AzureRmDataMigrationProject cmdlet hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="39f1c-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="39f1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39f1c-110">EXAMPLES</span></span>

### <span data-ttu-id="39f1c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39f1c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="39f1c-112">Exemplet ovan hämtar ett Azure Database migration-projekt med namnet TestProject i resurs gruppen som heter testResourceGroup och under tjänst heter testService</span><span class="sxs-lookup"><span data-stu-id="39f1c-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="39f1c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="39f1c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="39f1c-114">Exemplet ovan hämtar Azure Database migration Project baserat på PSProject-indataparameter som skickades.</span><span class="sxs-lookup"><span data-stu-id="39f1c-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="39f1c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39f1c-115">PARAMETERS</span></span>

### <span data-ttu-id="39f1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f1c-116">-DefaultProfile</span></span>
<span data-ttu-id="39f1c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39f1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39f1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39f1c-118">-InputObject</span></span>
<span data-ttu-id="39f1c-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="39f1c-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f1c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="39f1c-120">-Name</span></span>
<span data-ttu-id="39f1c-121">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="39f1c-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="39f1c-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="39f1c-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f1c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f1c-124">-ResourceId</span></span>
<span data-ttu-id="39f1c-125">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="39f1c-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f1c-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="39f1c-126">-ServiceName</span></span>
<span data-ttu-id="39f1c-127">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="39f1c-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="39f1c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39f1c-128">INPUTS</span></span>

### <span data-ttu-id="39f1c-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="39f1c-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="39f1c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39f1c-130">System.String</span></span>


## <span data-ttu-id="39f1c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39f1c-131">OUTPUTS</span></span>

### <span data-ttu-id="39f1c-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataMigration. Models. PSProject, Microsoft. Azure. commands. DataMigration, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="39f1c-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="39f1c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39f1c-133">NOTES</span></span>

## <span data-ttu-id="39f1c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39f1c-134">RELATED LINKS</span></span>

